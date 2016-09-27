This is my Other Note :)
------------------------
Auther: Chao Wei-Chu

目錄:
---------

Note1:[Network][javascript]關於使用Ajax+jquery跨網域存取server時的Access-Control-Allow-Origin解決方式(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_Other_note.md#node1關於使用ajaxjquery跨網域存取server時的access-control-allow-origin解決方式)

Note2:[Network][CSS]撰寫CSS註解時注意事項(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_Other_note.md#node2撰寫css註解時注意事項)

Note3:[MicrosoftAPI/Studio][C/C++]Visual Studio 2013錯誤: error LNK2005 已經在xxxxx.obj中定義的問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_Other_note.md#node3visual-studio-2013錯誤-error-lnk2005-已經在xxxxxobj中定義的問題)


node1:關於使用Ajax+jquery跨網域存取server時的Access-Control-Allow-Origin解決方式
--------------------------------------------------------------------------------
所謂跨站HTTP請求(Cross-site HTTP request)是指發出請求所在網域不同於請求所指向之網域的HTTP請求，基於安全性考量，程式碼所發出的跨站HTTP請求受到相當限制，好比說用XMLHttpRequest物件所發出的請求受限於同源政策(same-origin -policy)，只能發送HTTP請求到和其所來自的相同的網域，不過開發者也希望能發展出安全的跨站請求方法來開發更好、更安全、搭配多種資源的網頁應用。

最常使用的方式:

          $(function(){
                  $.ajax({
                    type:     "POST",
                    url:    "http://example.com/test.jsp",
                    dataType:   "jsonp", 
                    success: function (data){
                            console.log("Get Json Data!");                     
                    },error: function (data){
                            console.log("Can Not Get Json Data!!!!!!");
                    }
                  });
        })

1、表單默認提交（get、post）、超鏈接訪問域外的資源，這是允許的，因為在點擊按鈕/超鏈接時，瀏覽器地址已經變了，這就是一個普通的請求，不存在跨域<br>
2、ajax(借助xmlhttprequest)跨域請求，這是被禁止的，因為ajax就是為了接受接受響應，這違背了，不允許跨域讀的原則<br>
3、jsonp屬於跨域讀且形式限制為GET方式，它利用了script標籤的特性；這是允許的。因為瀏覽器把跨域讀腳本，當作例外，類似的img、iframe的src都可以請求域外資源<br>

解決方案：[參考網站](http://blog.csdn.net/wangjun5159/article/details/49096445)
###方案1:給chrome瀏覽器添加參數, --disable-web-security
![icon](http://img.blog.csdn.net/20151013142253473?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQv/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/Center)

###方案2
a.非IE瀏覽器，利用xmlhttprequest，在request header添加origin:本域名地址，通常不需要手動添加，瀏覽器會動添加
IE瀏覽器，利用XDomainRequest發送請求，它會自動封裝header中添加origin
b. response header添加access-control-allow-origin:*

跨域演示及代碼
驗證過程，首先訪問http://本機ip:port/project_name/a.jsp,然後，a.jsp發送ajax請求，http://localhost:port/project_name/b.jsp，這樣就產生了跨域的問題。

          a.jsp
          < %@ page  language = "java" contentType = "text/html; charset=UTF-8"   
              pageEncoding = "UTF-8" % >  
          < html xmlns = "http://www.w3.org/1999/xhtml" dir = "ltr" >    
            < head >  
                < meta http-equiv = "content-type" content = "text/html; charset=UTF-8" />    
                < title > 跨域演示</ title >  
                < script type = "text/javascript" src = "jquery-1.11.2.js" > </ script >    
                < script type = "text/javascript" src = "jquery.form.js" > </ script >    
            </ head >  
          < script type = "text/javascript" >   
          $(document).ready(function() {  
              $.getJSON('http://localhost/test_maven/b.jsp', function(data) {  
                  alert("request succeed");  
              });  
          });  
          </ script >  
          

          b.jsp
          [html] view plain copy  在CODE上查看代碼片派生到我的代碼片
          < %@ page  language = "java" contentType = "text/html; charset=UTF-8"   
              pageEncoding = "UTF-8" % >  
          < %  
                response.setHeader("Access-Control-Allow-Origin", "*");  
                response.getWriter().write("hahahhaha");  
          % >  

如果註釋掉response.setHeader("Access-Control-Allow-Origin","*"),那麼就會出現access control allow origin錯誤；使用通配符*，允許所有跨域訪問，所以跨域訪問成功。

簡單來說，符合上述條件的都是"簡單請求"，除了簡單請求就是"複雜請求"。
有關簡單請求(simple request)、先導請求、HTTP回應標頭...等的詳細說明，請參考文件:[HTTP access control (CORS)-HTTP_MDN.pdf](HTTP access control (CORS) - HTTP _ MDN.pdf)

###以下是實際範例:
[php]:

        <?php 
                header("Access-Control-Allow-Origin: *");
                echo "我是PHP回傳的值"; 
        ?>

[jsp&servlet]:

        <%@ page language="java" contentType="text/html; charset=UTF-8"  
            pageEncoding="UTF-8"%>  
        <%  
                response.setHeader("Access-Control-Allow-Origin", "*");  
                response.getWriter().write("hahahhaha");  
        %>

[參考文件](Access control allow origin 简单请求和复杂请求 - wangjun5159的专栏 - 博客频道 - CSDN.pdf)

node2:撰寫CSS註解時注意事項
--------------------------------------------------------------------------------
雖然說官方文件描述CSS的註解方式可以使用

          1. "\\......"
或是

          2. "\*......*\"
這兩種任一種方式，但在實際撰寫時發現若使用第一種方式會有極大的機率造成CSS標籤誤判，導致原始效果會顯現不出來，
所以我後來撰寫CSS註解一律改成第二種方式。


node3:Visual Studio 2013錯誤: error LNK2005 已經在xxxxx.obj中定義的問題
---------------------------------------------------------------------
最近在寫WindowsSocketApi時，因為要節省步驟，所以我將client和server寫成.h檔，然後用一個main.cpp去呼叫，這樣可以直接在同一個project裡實作client和server，但我寫完compiler時一直遇到如標題的問題"error LNK2005:已經在xxxxx.obj中定義"，然後一直搞不清楚到底問題是出在哪裡，因為之前這樣寫都沒問題，
於是上網查了很多資料，大致分析此問題情況如下:

1．重复定義全域變數。可能存在兩種情況：

          I.對於一些初學者，有時候會以為需要使用全域變數的地方就可以使用"define"申明一下。其實這是錯誤的，全域變數是針對整個project的。正確的應該是
          在一個CPP文件中定義如下：int g_Test 那麼在使用的CPP文件中就應該使用：extern int g_Test即可，如果還是使用int g_Test，那麼就會產LNK2005
          錯誤，一般錯誤錯誤信息類似:error LNK2005: "int_ _cdecl ssClient(void)" (?ssClient@@YAHXZ) already defined in main.obj。切記的就是
          不能给變量賦值否則還是會有LNK2005錯誤。   
                這裏需要的是“聲明”，不是“define”！根據C++標准的規定，一個變數是聲明，必須同時滿足兩個條件，否則就是定義：   
                (1)聲明必須使用extern關鍵字；(2)不能给變量賦初值   
                所以，下面的是聲明:   
                extern int a;
                下面的是define
                int a;
                int a=0;
                extern int a=0;
          II.對於那麼編程不是那麼嚴謹的人，總是在需要使用變量的文件中隨意定義一個全域變數，並且對於變數名也不予考慮，這也往往容易造成變數名重复，
          而造成LNK2005錯誤。
          
2.頭文件的包含重复。往往需要包含的頭文件中含有變量、函數、類的定義，在其它使用的地方又不得不多次包含之，如果頭文件中沒有相關的宏等防止重复鏈接的措施，那麼就會產生LNK2005錯誤。解决辦法是在需要包含的頭文件中做類似的處理：
          
          #ifndef   MY_H_FILE       //如果沒有定義這個宏   
          #define   MY_H_FILE       //定義這個宏   
                    …….       //頭文件主體內容   
                    …….   
          #endif   

上面是使用宏來做的，也可以使用預編譯來做，在頭文件中加入：   
          
          #pragma   once      //頭文件主體   
          
3.使用第三方的庫造成的。這種情況主要是C運行期函數庫和MFC的庫沖突造成的。具體的辦法就是將那個提示出錯的庫放到另外一個庫的前面。另外選擇不同的C函數庫，可能會引起這個錯誤。微軟和C有兩種C運行期函數庫，一種是普通的函數庫：LIBC.LIB，不支持多線程。另外一種是支持多線程的：msvcrt.lib。如果一個工程裏，這兩種函數庫混合使用，可能會引起這個錯誤，一般情況下它需要MFC的庫先於C運行期函數庫被鏈接，因此建議使用支持多線程的msvcrt.lib。所以在使用第三方的庫之前首先要知道它鏈接的是什麼庫，否則就可能造成LNK2005錯誤。如果不得不使用第三方的庫，可以嘗試按下面所說的方法修改，但不能保證一定能解决問題，前兩種方法是微軟提供的：   

            A、選擇VC菜單Project->Settings->Link->Catagory選擇Input，再在Ignore   libraries   的Edit欄中填入你需要忽略的庫，如：
            Nafxcwd.lib;Libcmtd.lib。然後在Object/library   Modules的Edit欄中填入正確的庫的順序，這裏需要你能確定什麼是正確的順序，呵呵，God   
            bless   you！   
            B、選擇VC菜單Project->Settings->Link頁，然後在Project   Options的Edit欄中輸入/verbose:lib，這样就可以在編譯鏈接程序過程中在輸出窗口
            看到鏈接的順序了。   
            C、選擇VC菜單Project->Settings->C/C++頁，Catagory選擇Code   Generation後再在User   Runtime   libraray中選擇MultiThread   DLL等
            其他庫，逐一嘗試。   
            
            關於編譯器的相關處理過程，参考：   
            http://www.donews.net/xzwenlan/archive/2004/12/23/211668.aspx   
            
 4.另外在官方網站有說明還有以下幾種可能:
 
          1.符號在不同程式庫的兩個成員物件中定義不同，而這兩個成員物件都已被使用。
          2.絕對被定義了兩次，每一個定義具有不同的值。
          3.標頭檔宣告並定義變數。  可能的解決方案包括：  
                    I.在 .h 中宣告變數：extern BOOL MyBool;，然後在 .c 或 .cpp 檔案中指派給它：BOOL MyBool = FALSE;。
                    II.宣告變數 static。
                    III.宣告變數 selectany。
          如果您將 uuid.lib 與其他定義 GUID 的 .lib 檔 (例如 oledb.lib 和 adsiid.lib) 結合使用。  例如：  

                    oledb.lib(oledb_i.obj) : error LNK2005: _IID_ITransactionObject
                    
                    already defined in uuid.lib(go7.obj)
          若要修正，請將 /FORCE:MULTIPLE 加入連結器命令列選項，並確保 uuid.lib 是最先參考的程式庫。

我這次是使用第4點的第3小點的方法II解決問題的，在.h檔中要引入的韓式前面加上static。

node4:開發windows網路應用時，遇到inet_addr()函式不能使用問題
---------------------------------------------------------
有用Windows Socket API開發過Windows應用程式的人應該都知道inet_addr這個函式，我們都知道若在windows上的程式要存取網路，要利用Windows Socket API，也就是Socket函式庫，利用Socket可以建立兩種連線，分別是TCP與UDP，而Windows提供WSAStartup()動態函式庫以提供所有socket功能，利用SOCKET structure建立Socket，以及closesocket()關閉Socket，其中closesocket()會偷偷執行函式WSASendDisconnect()中斷連線，而在設定位址與port時，需用sockaddr設定，IPv4用sockaddr_in，IPv6用sockaddr_in6，而我這次遇到的問題，是在設定sockaddr_in時，有一項SOCKADDR_IN AddrServ.sin_addr.s_addr=inet_addr(IP);出錯，我很確定我沒有寫錯，而出錯的訊息如下:

          'inet_addr': Use inet_pton() or InetPton() instead or define _WINSOCK_DEPRECATED_NO_WARNINGS to disable deprecated API warnings
於是上網查了一下，發現原來原本inet_addr()有以下幾個問題:
          
          1. inet_addr()只能用在IPv4，若要通用要改成inet_pton()或inet_ntop()
          2. inet_pton()或inet_ntop()在原本的winsock2.h裡沒有阿，他x的。
          3. 有幾個winsock2.h中的函式皆因安全醒問題被淘汰，如下:
                    a. inet_aton() 原因:返回静态空间，非线程安全
                    b. inet_addr() 原因:返回的整数形式是网络字节序，因为出错时返回-1；而cp为“255.255.255.255”时也返回-1
                    c. inet_ntoa() 原因:返回静态空间，非线程安全
                    d. inet_network() 原因:返回的整数形式是主机字节序；被 inet_aton淘汰，因为出错时返回-1；而cp为“255.255.255.255”时也返回-1
          
因此查了一下官方解法，解決方式如下:
          
          法1.please make sure you define  _WINSOCK_DEPRECATED_NO_WARNINGS before all the include.
          法2.add #include <WS2tcpip.h> and use inet_pton(AF_INET, IP, buf) to instead of inet_addr(IP).
          ##另外要將VisualStadio Update至最新版本 (不愧是萬惡的微軟，連VS也要強制更新~)

