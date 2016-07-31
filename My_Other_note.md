This is my Other Note :)
------------------------
Auther: Chao Wei-Chu

目錄:
---------

Note1:[Network][javascript]關於使用Ajax+jquery跨網域存取server時的Access-Control-Allow-Origin解決方式(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_Other_note.md#node1:關於使用Ajax+jquery跨網域存取server時的Access-Control-Allow-Origin解決方式)


node1:關於使用Ajax+jquery跨網域存取server時的Access-Control-Allow-Origin解決方式
--------------------------------------------------------------------------------
所謂跨站HTTP請求(Cross-site HTTP request)是指發出請求所在網域不同於請求所指向之網域的HTTP請求，基於安全性考量，程式碼所發出的跨站HTTP請求受到相當限制，好比說用XMLHttpRequest物件所發出的請求受限於同源政策(same-origin -policy)，只能發送HTTP請求到和其所來自的相同的網域，不過開發者也希望能發展出安全的跨站請求方法來開發更好、更安全、搭配多種資源的網頁應用。

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
      
