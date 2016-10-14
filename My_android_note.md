This is my Android notes :)
=========================
Auther: Chao Wei-Chu

<link rel="stylesheet" href="http://yandex.st/highlightjs/6.2/styles/googlecode.min.css">
 
<script src="http://code.jquery.com/jquery-1.7.2.min.js"></script>
<script src="http://yandex.st/highlightjs/6.2/highlight.min.js"></script>
 
<script>hljs.initHighlightingOnLoad();</script>
<script type="text/javascript">
 $(document).ready(function(){
      $("h2,h3,h4,h5,h6").each(function(i,item){
        var tag = $(item).get(0).localName;
        $(item).attr("id","wow"+i);
        $("#category").append('<a class="new'+tag+'" href="#wow'+i+'">'+$(this).text()+'</a></br>');
        $(".newh2").css("margin-left",0);
        $(".newh3").css("margin-left",300);
        $(".newh4").css("margin-left",40);
        $(".newh5").css("margin-left",60);
        $(".newh6").css("margin-left",80);
      });
 });
</script>
<div id="category">
	<h2>目錄:</h2>
	<h5>Note1:Android最基本之問題就是沒加權限(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#note1)</h5>
	<h5>Note2:Toast功能之常遇問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#note2)</h5>
	<h5>Note3:新map物件與引入mapframe寫法不同問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node3新map物件與引入mapframe寫法不同問題)</h5>
	<h5>Note4:使用Intent創造new Activity時要在AndroidManifest.xml加入設定(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node4-使用intent創造new-activity時要在androidmanifestxml加入設定)</h5>
	<h5>Note5:GPS的三種寫法(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node5-gps的三種寫法)</h5>
	<h5>Note6:關於在androidView物件上顯示數字之注意事項(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node6-關於在androidview物件上顯示數字之注意事項)</h5>
	<h5>Note7:將view畫面以Camera取代(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node7-將view畫面以camera取代)</h5>
	<h5>Note8:AppCompatActivity與FragmentActivity問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node8appcompatactivity與fragmentactivity問題)</h5>
	<h5>Note9:Error inflating class android.support.design.widget.NavigationView問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node9error-inflating-class-androidsupportdesignwidgetnavigationview問題)</h5>
	<h5>Note10:map fragment 之意外:android.view.InflateException: Binary XML file line(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node10map-fragment-之意外androidviewinflateexception-binary-xml-file-line)</h5>
	<h5>Note11:在GoogleMap上的mark加上自訂格式樣式的注意事項(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node11在googlemap上的mark加上自訂格式樣式的注意事項)</h5>
	<h5>Note12:使用Android POST and GET Request using HttpURLConnection(https://github.com/Chao-wei-chu/GDeveloper_DOC-Save-My-Android-note-/blob/master/My_android_note.md#node12使用android-post-and-get-request-using-httpurlconnection-)</h5>
	<h5>Note13:Snackbar用法及注意事項(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node13snackbar用法及注意事項-)</h5>
	<h5>Note14:method預設大小限制64k的問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node14method預設大小限制64k的問題)</h5>
	<h5>Note15:引入gradle插件這次是github的所遇到的問題與解法(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node15引入gradle插件這次是github的所遇到的問題與解法)</h5>
	<h5>Note16:Googlemap畫線問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node16googlemap畫線問題)</h5>
	<h5>Note17:依螢幕動態調整大小問題(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node17依螢幕動態調整大小問題)</h5>
	<h5>Note18:Android 中的 Thread 與傳遞資料的方式(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node18android-中的-thread-與傳遞資料的方式)</h5>
	<h5>Note19:Android AsyncTask----Thread之外的另一選擇(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node19android-asynctask----thread之外的另一選擇)</h5>
	<h5>Note20:Android的Thread大家族(Handler、Message、Looper、MessageQueue)(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node20android的thread大家族handlermessageloopermessagequeue)</h5>
	<h5>Note21:Android AsyncTask 與 Handler Thread 的差異(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node21android-asynctask-與-handler-thread-的差異)</h5>
	<h5>Note22:Android Socket教學與程式範例(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node22android-socket教學與程式範例)</h5>
	<h5>Note23:WebSocket概觀與Android WebSocket實現(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node23websocket概觀與android-websocket實現)</h5>
	<h5>Note24:Android Studio 2.x版本常見問題(2016/10/14)(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node24android-studio-2x版本常見問題20161014)</h5>
	<h2>=============================</h2>	
</div>

note1:Android最基本之問題就是沒加權限
-----------------------------------

Android最常見之問題就是沒加權限，記得只要有使用Camera、Internat、sensor、Bluetooth、Google API、Intent等功能就要加入權限，
例如:
  使用GPS，就要加入:
  
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>  //允許利用網路定位
    
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>   //允許利用GPS定位

通常若不知道要加入甚麼權限的話，就加入常用的，如下:
    
    <uses-permission android:name="android.permission.CAMERA"></uses-permission>
    <uses-feature android:required="false" android:name="android.hardware.camera.autofocus"></uses-feature>
    <uses-feature android:required="false" android:name="android.hardware.camera.flash"></uses-feature>
    <uses-feature android:required="false" android:name="android.hardware.camera.front"></uses-feature>
    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>
    <uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE"/>
    <uses-permission android:name="com.google.android.providers.gsf.permission.READ_GSERVICES"/>
    <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
    
[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

note2:Toast功能之常遇問題
------------------------

關於Toast這項功能之問題，通常這物件是用於在視窗以提示的方式顯示訊息，通常用法如下:

    Toast.makeText(this,"hello",Toast.LENGTH_SHORT).show(); //LENGTH_SHORT是指顯示時間很短，this是指以Main(ex:MainActivitys)來使用此函式

但是有時候我們會想在函式裡使用這功能，此時通常會失敗，
ex:

     private class btnTranListener implements Button.OnClickListener{
        @Override
        public void onClick(View v){
            Toast.makeText(this,"hello",Toast.LENGTH_SHORT).show();
        }
    };

會失敗的原因在於此時Toast內的this指的不是Main，而是指btnTranListener這個類別名稱，因此會呼叫失敗；此時我們只能以別的方式實現，
解法如下:
    利用一個函式先將Toast包起來，在呼叫他即可:
    
    private class btnTranListener implements Button.OnClickListener{
        @Override
        public void onClick(View v){
            showToast("hello");
        }
    };
    
    private void showToast(String message){
        Toast.makeText(this,message,Toast.LENGTH_LONG).show();
    }
    
[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node3:(新map物件與引入mapFrame寫法不同問題)
-------------------------------------------
一般若要寫map通常都是直接創造一個新的Google map專案(像網路上大部分教學這樣)，一般的googlemap專案會看到如下東西:

    public class MapsActivity extends FragmentActivity{
          private GoogleMap mMap;
          protected void onCreate(Bundle savedInstanceState) {
                super.onCreate(savedInstanceState);
                setContentView(R.layout.activity_maps);
                mMap=((SupportMapFragment)getSupportFragmentManager().findFragmentById(R.id.map)).getMap();
                mMap.animateCamera(CameraUpdateFactory.newLatLngZoom(initalPoint,17));
          }
    }
    
但以上的程式碼要能運作的前提在於，主程式本身就為了GoogleMap創的，因此可以看到MapsActivity延伸了FragmentActivity部分，但如果我們是要
在一個Frame中展示Map功能，而其他地方要放別的物件呢?那必須改寫法，如下:

    private void BuildMapView() {
        /**MapView 地圖**/
        LayoutInflater inflater = getLayoutInflater();
        tmpView = inflater.inflate(R.layout.map_view, null);  //加入map視窗到主介面
        tmpView.setAlpha(Map_Transparency);//設定map透明度
        getWindow().addContentView(tmpView, new ViewGroup.LayoutParams(450, 450));  //可調地圖大小  調回350*350
    }
    
先將要畫map的layout檔引入進來，並以add的方式將引入的物件放在主程式的View畫框上，此時要求map功能的寫法，也就從:

    mMap=((SupportMapFragment)getSupportFragmentManager().findFragmentById(R.id.map)).getMap();
    
改寫成:

    mMap = ((MapFragment) getFragmentManager().findFragmentById(R.id.map)).getMap();
    
才能順利在附加的layout檔中使用Map功能。
(extra:layout.xml範例)

    <RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent" >
        
        <fragment
            android:id="@+id/map"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            class="com.google.android.gms.maps.MapFragment" />

    </RelativeLayout>

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node4: (使用Intent創造new Activity時要在AndroidManifest.xml加入設定)
---------------------------------------------------------------------

在Android中其實有種東西會讓人覺得很神，這東西叫Intent，Intent 一般用來跳轉Activity，關於Activity是什麼，我當初是參考"Android 6~5.x App
開發教戰手冊-使用Android Studio"這本，解說得不錯，Activity基本上可看作一個頁面，如同書本的頁面，最簡單的例子就是手機的分頁按鈕(通常在
home鍵的右邊)，按下去會看到目前正在背景執行的所有程式(又稱最近使用過的程式)，而每一個程式就是一個Activity，每個Activity有7個生命週期，
之後自己去查；舉個例子:

### 用法一 : 從A.class跳到B.class
    比喻: 某人要從 A地到B地  靠的是交通工具(Intent )
    A.class 目前的Class
    B.class 目的Class

        Intent i = new Intent();
        i.setClass(A.this,B.class)
        startActivity(i);
    or
        Intent i = new Intent(A.this,B.class);
        startActivity(i);//開始跳往要去的Activity
        
    如果要結束A.class 要加上這行
        A.this.finish();//結束目前Activity

### 用法二 :傳遞資料從A到B
    比喻: 某人要從 A地帶東西(Bundle)到B地  靠的是交通工具(Intent), 所以他把東西(Bundle) 放在 交通工具上(Intent)一起帶去

    1.Intent
      A.class(傳送資料)
      
          //new一個intent物件，並指定Activity切換的class
          Intent intent = new Intent();
          intent.setClass(A.this,B.class);
           
          intent .putExtra("name",name);//可放所有基本類別
           
          //切換Activity
          startActivity(intent);

      B.class(接收資料)
      
          Intent intent = this.getIntent();
          //取得傳遞過來的資料   
          String name = intent.getStringExtra("name");  

    2.Bundle+Intent
      用法簡介: 
      
        A.class(傳送資料)
          //new一個intent物件，並指定Activity切換的class
          Intent intent = new Intent();
          intent.setClass(A.this,B.class);
           
          //new一個Bundle物件，並將要傳遞的資料傳入
          Bundle bundle = new Bundle();
          bundle.putDouble("age",age );//傳遞Double
          bundle.putString("name",name);//傳遞String
           
          //將Bundle物件傳給intent
          intent.putExtras(bundle);
           
          //切換Activity
          startActivity(intent);

        B.class(接收資料)
        
          Bundle bundle = getIntent().getExtras();  
          String name = bundle.getString("name");
          double age = bundle.getDouble("age");

### 用法三 :從A跳到B再從B傳參數回去
    比喻: 甲拜託乙 從A地到B地買東西回來 ,靠的是交通工具(Intent), 乙回來的話東西送到甲的地址(requestCode)
    
      A.class
      
          Intent intent = new Intent(A.this,B.class);
          //requestCode(識別碼) 型別為 int ,從B傳回來的物件將會有一樣的requestCode
          startActivityForResult(intent,requestCode);

      B.class
      
          Intent intent = getIntent();
          Bundle bundle = new Bundle();
          bundle.putString("name",name);  
          intent.putExtras(bundle); 
          setResult(requestCode, intent); //requestCode需跟A.class的一樣 
          B.this.finish();
          
      然後要在A.class裡複寫onActivityResult 才能接收B傳回的值
          Intent intent = getIntent();
          @Override 
          protected void onActivityResult(int requestCode, int resultCode, Intent data) {  
              
              switch(resultCode){//resultCode是剛剛妳A切換到B時設的resultCode  
              case requestCode://當B傳回來的Intent的requestCode 等於當初A傳出去的話
                  String result = data.getExtras().getString("name");
                   
                  break;
              
              }
            
          }

### 用法四 :傳遞自定義的物件
    上面提到的方法都只能傳基本型別，如:String ,boolean ,int ,double 等等的，那要如何傳遞自定義的物件到另一個class呢?
    
        1.利用Serializable or Parcelable
        
            Bundle.putSerializable(Key,Object);
            Bundle.putParcelable(Key, Object);
            這兩種都必須時做接口
            今天講Serializable
            要利用 Serializable 傳遞物件的話 
            妳的物件必須  implements Serializable
            EX :
                public class CustomObject implements Serializable {
                          private static final long serialVersionUID = -7060210544600464481L;
                          //省略以下 為你class的內容
                }

            然後在要傳資料的B.class裡
                CustomObject co_b = new CustomObject ();
                 
                Intent i=new Intent();
                Bundle bundle=new Bundle();
                 
                bundle.putSerializable("CustomObject ", co_b);
                 
                i.putExtras(bundle);
                 
                startActivity(i);
                
            然後在需要資料的A.class裡就能使用了
                CustomObject co_a = null;
                 
                co_a = getIntent().getSerializableExtra("CustomObject ")
        2.利用全域變數 簡單使用別的class的自定義物件
            在A.class裡
                public class A extends Activity{
                   public static CustomObject co_a = null; //一定要加static 且 public
                   //以下intent從A到B的內容省略
                }

            在B.class裡
                CustomObject co_b = A.co_a;//直接使用A的static物件

但不論怎樣，一定要記得在AndroidManifest.xml檔中加入檔案設定，例如我在A主檔要跳至Bjava檔:

        Intent i = new Intent();
        i.setClass(A.this,B.class)
        startActivity(i);
        
    在AndroidManifest.xml中就要加入:
    
        <activity
            android:name="B"
            android:label="@string/app_name">
        </activity>
        
    沒加必出錯。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node5 (GPS的三種寫法)
----------------------

以下是我在學GPS時獵奇找到的三種寫法，但觀念都一樣。

###第一種:

    private GoogleMap mMap;
    private LocationManager locMgr;
    String Bestprov;
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_maps);
        mMap = ((SupportMapFragment) getSupportFragmentManager().findFragmentById(R.id.map)).getMap();
        locMgr = (LocationManager) getSystemService(LOCATION_SERVICE);
        Criteria criteria=new Criteria();
        Bestprov=locMgr.getBestProvider(criteria,true);
        if (ActivityCompat.checkSelfPermission(this, Manifest.permission.ACCESS_FINE_LOCATION) != PackageManager.PERMISSION_GRANTED && ActivityCompat.checkSelfPermission(this, Manifest.permission.ACCESS_COARSE_LOCATION) != PackageManager.PERMISSION_GRANTED) {
            // TODO: Consider calling
            //    ActivityCompat#requestPermissions
            // here to request the missing permissions, and then overriding
            //   public void onRequestPermissionsResult(int requestCode, String[] permissions,
            //                                          int[] grantResults)
            // to handle the case where the user grants the permission. See the documentation
            // for ActivityCompat#requestPermissions for more details.
            return;
        }
        Location loc = locMgr.getLastKnownLocation(LocationManager.GPS_PROVIDER);
        if(loc!=null){
            Toast.makeText(this,loc.getLatitude()+" "+loc.getLongitude(),Toast.LENGTH_LONG).show();
        }
        UpdateLocation(loc);
        locMgr.requestLocationUpdates(LocationManager.GPS_PROVIDER,2000,0,new MylocationListener());
    }
    public void UpdateLocation(Location location){
        if(location!=null){
            LatLng testpoint2=new LatLng(location.getLatitude(),location.getLongitude());
            mMap.animateCamera(CameraUpdateFactory.newLatLngZoom(testpoint2,18));
            Toast.makeText(this,location.getLatitude()+" "+location.getLongitude(),Toast.LENGTH_LONG).show();
            MarkerOptions Makops=new MarkerOptions();
            Makops.position(testpoint2);
            mMap.addMarker(Makops);
        }

    }
    public class MylocationListener implements LocationListener{

        @Override
        public void onLocationChanged(Location location) {
            UpdateLocation(location);
        }

        @Override
        public void onStatusChanged(String provider, int status, Bundle extras) {

        }

        @Override
        public void onProviderEnabled(String provider) {

        }

        @Override
        public void onProviderDisabled(String provider) {

        }
    }
    
###寫法二:
    Android初學特訓班那本教的
###寫法三:
    Android 6~5.x App開發教戰手冊這本教的(目前最有用的)

    private GoogleApiClient.OnConnectionFailedListener onConnectionFailedListener= new GoogleApiClient.OnConnectionFailedListener(){

        @Override
        public void onConnectionFailed(@NonNull ConnectionResult connectionResult) {
            Toast.makeText(MainActivity.this,"Connect failed.",Toast.LENGTH_SHORT).show();
            if(!connectionResult.hasResolution()){
                GooglePlayServicesUtil.getErrorDialog(connectionResult.getErrorCode(),MainActivity.this,0).show();
                return;
            }
            try{
                connectionResult.startResolutionForResult(MainActivity.this,1);
            }catch(IntentSender.SendIntentException e){
                Log.e("MainActivity","Exception while start resolution activity");
            }
        }
    };

    private GoogleApiClient.ConnectionCallbacks connectionCallbacks =
            new GoogleApiClient.ConnectionCallbacks() {

                @Override
                public void onConnected(@Nullable Bundle bundle) {
                    if (ActivityCompat.checkSelfPermission(MainActivity.this, Manifest.permission.ACCESS_FINE_LOCATION) != PackageManager.PERMISSION_GRANTED && ActivityCompat.checkSelfPermission(MainActivity.this, Manifest.permission.ACCESS_COARSE_LOCATION) != PackageManager.PERMISSION_GRANTED) {
                        // TODO: Consider calling
                        //    ActivityCompat#requestPermissions
                        // here to request the missing permissions, and then overriding
                        //   public void onRequestPermissionsResult(int requestCode, String[] permissions,
                        //                                          int[] grantResults)
                        // to handle the case where the user grants the permission. See the documentation
                        // for ActivityCompat#requestPermissions for more details.
                        return;
                    }
                    location = LocationServices.FusedLocationApi.getLastLocation(googleApiClient);



                    LocationRequest locationRequest=LocationRequest.create()
                            .setPriority(LocationRequest.PRIORITY_HIGH_ACCURACY)
                            .setInterval(1000)
                            .setSmallestDisplacement(1);

                    LocationServices.FusedLocationApi.requestLocationUpdates(googleApiClient,locationRequest, locationListener);

                }

                @Override
                public void onConnectionSuspended(int i) {
                    Toast.makeText(MainActivity.this,"暫時無連結",Toast.LENGTH_SHORT).show();
                }
            };

    private LocationListener locationListener=new LocationListener() {
        @Override
        public void onLocationChanged(Location location) {
            Toast.makeText(MainActivity.this,"GPS reset: "+location.getLatitude()+" "+location.getLongitude(),Toast.LENGTH_SHORT).show();
            latLng=new LatLng(location.getLatitude(),location.getLongitude());
            map.moveCamera(CameraUpdateFactory.newLatLngZoom(latLng, 16));
            MarkerOptions markerOptions = new MarkerOptions();
            markerOptions.position(latLng);
            map.addMarker(markerOptions);

        }
    };

    @Override
    protected void onResume(){
        super.onResume();
        if (googleApiClient == null) {
            googleApiClient = new GoogleApiClient.Builder(this)
                    .addApi(LocationServices.API)
                    .addConnectionCallbacks(connectionCallbacks)
                    .addOnConnectionFailedListener(onConnectionFailedListener)
                    .build();
        }
        googleApiClient.connect();
    }

    @Override
    protected void onPause(){
        super.onPause();
        if(googleApiClient!=null){
            googleApiClient.disconnect();
        }

    }

    @Override
    protected void onActivityResult(int requestCode,int resultCode,Intent data){
        super.onActivityResult(requestCode,resultCode,data);
        if(resultCode==RESULT_OK){
            if(requestCode==1){
                googleApiClient.connect();
            }
        }
    }

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node6: 關於在androidView物件上顯示數字之注意事項:
------------------------------------------------

一般會在android的View物件顯示文字以凸顯功能，但要顯示數字呢?一般人會想到這樣，ex:

     private int count=0;
     
     textView=(TextView)findViewById(R.id.tvCount);
     textView.setText(count);
     
但有經驗的人都知道，上方的作法會導致錯誤，所以要改成:

     textView=(TextView)findViewById(R.id.tvCount);
     textView.setText(String.valueOf(count));

即可。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node7: 將view畫面以Camera取代
-----------------------------
範例Code:(class1)
	
    package com.example.user.initial_ar12;

    import android.content.Context;
    import android.hardware.Camera;
    import android.util.Log;
    import android.view.SurfaceHolder;
    import android.view.SurfaceView;
    import java.util.Iterator;
    import java.util.List;
    
    /**
     * Camera鏡頭畫面擷取
     **/
    
    public class CameraSurface extends SurfaceView implements
    		SurfaceHolder.Callback {
    	MainActivity app;
    	SurfaceHolder holder;
    	Camera camera;
    
    	CameraSurface(Context context) {
    		super(context);
    
    		try {
    			app = (MainActivity) context;
    
    			holder = getHolder();
    			holder.addCallback(this);
    			holder.setType(SurfaceHolder.SURFACE_TYPE_PUSH_BUFFERS);
    		} catch (Exception ex) {
    
    		}
    	}
    
    	public void surfaceCreated(SurfaceHolder holder) {
    		try {
    			if (camera != null) {
    				try {
    					camera.stopPreview();
    				} catch (Exception ignore) {
    				}
    				try {
    					camera.release();
    				} catch (Exception ignore) {
    				}
    				camera = null;
    			}
    
    			camera = Camera.open();
    			camera.setPreviewDisplay(holder);
    		} catch (Exception ex) {
    			try {
    				if (camera != null) {
    					try {
    						camera.stopPreview();
    					} catch (Exception ignore) {
    					}
    					try {
    						camera.release();
    					} catch (Exception ignore) {
    					}
    					camera = null;
    				}
    			} catch (Exception ignore) {
    
    			}
    		}
    	}
    
    	public void surfaceDestroyed(SurfaceHolder holder) {
    		try {
    			if (camera != null) {
    				try {
    					camera.stopPreview();
    				} catch (Exception ignore) {
    				}
    				try {
    					camera.release();
    				} catch (Exception ignore) {
    				}
    				camera = null;
    			}
    		} catch (Exception ex) {
    			ex.printStackTrace();
    		}
    	}
    
    	public void surfaceChanged(SurfaceHolder holder, int format, int w, int h) {
    		try {
    			Camera.Parameters parameters = camera.getParameters();
    			try {
    				List<Camera.Size> supportedSizes = null;
    				// On older devices (<1.6) the following will fail
    				// the camera will work nevertheless
    				supportedSizes = Compatibility.getSupportedPreviewSizes(parameters);
    
    				// preview form factor
    				float ff = (float) w / h;
    				Log.d("Mixare", "Screen res: w:" + w + " h:" + h
    						+ " aspect ratio:" + ff);
    
    				// holder for the best form factor and size
    				float bff = 0;
    				int bestw = 0;
    				int besth = 0;
    				Iterator<Camera.Size> itr = supportedSizes.iterator();
    
    				// we look for the best preview size, it has to be the closest
    				// to the
    				// screen form factor, and be less wide than the screen itself
    				// the latter requirement is because the HTC Hero with update
    				// 2.1 will
    				// report camera preview sizes larger than the screen, and it
    				// will fail
    				// to initialize the camera
    				// other devices could work with previews larger than the screen
    				// though
    				while (itr.hasNext()) {
    					Camera.Size element = itr.next();
    					// current form factor
    					float cff = (float) element.width / element.height;
    					// check if the current element is a candidate to replace
    					// the best match so far
    					// current form factor should be closer to the bff
    					// preview width should be less than screen width
    					// preview width should be more than current bestw
    					// this combination will ensure that the highest resolution
    					// will win
    					Log.d("Mixare", "Candidate camera element: w:"
    							+ element.width + " h:" + element.height
    							+ " aspect ratio:" + cff);
    					if ((ff - cff <= ff - bff) && (element.width <= w)
    							&& (element.width >= bestw)) {
    						bff = cff;
    						bestw = element.width;
    						besth = element.height;
    					}
    				}
    				Log.d("Mixare", "Chosen camera element: w:" + bestw + " h:"
    						+ besth + " aspect ratio:" + bff);
    				// Some Samsung phones will end up with bestw and besth = 0
    				// because their minimum preview size is bigger then the screen
    				// size.
    				// In this case, we use the default values: 480x320
    				if ((bestw == 0) || (besth == 0)) {
    					Log.d("Mixare", "Using default camera parameters!");
    					bestw = 480;
    					besth = 320;
    				}
    				parameters.setPreviewSize(bestw, besth);
    			} catch (Exception ex) {
    				parameters.setPreviewSize(480, 320);
    			}
    
    			camera.setParameters(parameters);
    			camera.startPreview();
    		} catch (Exception ex) {
    			ex.printStackTrace();
    		}
    	}
    }
    
範例Code:(class2)

    public class Compatibility {
      	private static Method mParameters_getSupportedPreviewSizes;
      	private static Method mDefaultDisplay_getRotation;
      
      	static {
      		initCompatibility();
      	};
      
      	/** this will fail on older phones (Android version < 2.0) */
      	private static void initCompatibility() {
      		try {
      			mParameters_getSupportedPreviewSizes = Camera.Parameters.class
      					.getMethod("getSupportedPreviewSizes", new Class[] {});
      			mDefaultDisplay_getRotation = Display.class.getMethod(
      					"getRotation", new Class[] {});
      
      			/* success, this is a newer device */
      		} catch (NoSuchMethodException nsme) {
      			/* failure, must be older device */
      		}
	      }

      	/**
      	 * If it's running on a new phone, let's get the supported preview sizes,
      	 * before it was fixed to 480 x 320
      	 */
      	@SuppressWarnings("unchecked")
      	public static List<Camera.Size> getSupportedPreviewSizes(
      			Camera.Parameters params) {
      		List<Camera.Size> retList = null;
      
      		try {
      			Object retObj = mParameters_getSupportedPreviewSizes.invoke(params);
      			if (retObj != null) {
      				retList = (List<Camera.Size>) retObj;
      			}
      		} catch (InvocationTargetException ite) {
      			/* unpack original exception when possible */
      			Throwable cause = ite.getCause();
      			if (cause instanceof RuntimeException) {
      				throw (RuntimeException) cause;
      			} else if (cause instanceof Error) {
      				throw (Error) cause;
      			} else {
      				/* unexpected checked exception; wrap and re-throw */
      				throw new RuntimeException(ite);
      			}
      		} catch (IllegalAccessException ie) {
      			// System.err.println("unexpected " + ie);
      		}
      		return retList;
      	}

      	static public int getRotation(final Activity activity) {
      		int result = 1;
      		try {
      			Display display = ((WindowManager) activity
      					.getSystemService(Context.WINDOW_SERVICE))
      					.getDefaultDisplay();
      			Object retObj = mDefaultDisplay_getRotation.invoke(display);
      			if (retObj != null) {
      				result = (Integer) retObj;
      			}
      		} catch (Exception ex) {
      			// ex.printStackTrace();
      		}
      		return result;
      	}

    }
    
[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node8:AppCompatActivity與FragmentActivity問題
---------------------------------------------

若遇到以下狀況:

	Toolbar toolbar = (Toolbar) findViewById(R.id.toolbar);
        setSupportActionBar(toolbar); //not found
        ActionBar actionBar = getSupportActionBar(); //not found
        actionBar.setHomeAsUpIndicator(R.drawable.ic_menu);
        actionBar.setDisplayHomeAsUpEnabled(true);
        
代表你預設用的主題是沒有支援ActionBar的，所以要將main extend改掉:

	public class MainActivity extends FragmentActivity {
	    @Override
	    protected void onCreate(Bundle savedInstanceState) {
	        super.onCreate(savedInstanceState);
	
	    }
    	}
改成:

	public class MainActivity extends AppCompatActivity {
	    @Override
	    protected void onCreate(Bundle savedInstanceState) {
	        super.onCreate(savedInstanceState);
	    }
    	}
    	
像這種AppCompatActivity有支援ActionBar的才行。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node9:Error inflating class android.support.design.widget.NavigationView問題
----------------------------------------------------------------------------

此問題通常發生在使用DrawerBar等特殊主題套件，解法:
	
	Actually it is not the matter of the primarycolortext, upgrading or downgrading the dependencies.This problem will likely occur when the version of your appcompat library and design support library doesn't match.
	Example of matching condition
		compile 'com.android.support:appcompat-v7:23.1.1' // appcompat library
		compile 'com.android.support:design:23.1.1' //design support library

意思是指請更新library :)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node10:map fragment 之意外:android.view.InflateException: Binary XML file line
------------------------------------------------------------------------------

自從Android改版後，所有使用到Map的程式皆要在AndroidManifest.xml中的<application>加入:

		<meta-data android:name="com.google.android.geo.API_KEY" android:value="your Key"/>
		
不再只需要:

		<meta-data android:name="com.google.android.maps.v2.API_KEY" android:value="your Key"/>
		
若不加會一直出錯。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node11:在GoogleMap上的mark加上自訂格式樣式的注意事項
----------------------------------------------------

code如下:

	private class Myinfo implements GoogleMap.InfoWindowAdapter{
	        private final View infoWindow=getLayoutInflater().inflate(R.layout.user_position,null);
	        @Override
	        public View getInfoWindow(Marker marker) {
	            TextView user_title=((TextView)infoWindow.findViewById(R.id.user_title));
	            TextView user_position = ((TextView)infoWindow.findViewById(R.id.user_text1));
	            user_position.setText("coordinate: "+latLng.latitude+" "+latLng.longitude);
	            user_title.setText("Position: "+marker.getTitle());
	            return infoWindow;
	        }
	
	        @Override
	        public View getInfoContents(Marker marker) {
	            return null;
	        }
	}
	
從code中可以看到TextView user_title=((TextView)infoWindow.findViewById(R.id.user_title))這行和一般的寫法不一樣，此處須注意以下幾點:

1.貌似從Android6.0之後堅持一定要加上括號:

	TextView user_title=((TextView)infoWindow.findViewById(R.id.user_title));
	
	不可寫成:
	
	TextView user_title=(TextView)infoWindow.findViewById(R.id.user_title);

2.findViewById部分需加上所指定的layout檔設定，不然一定出錯:

	((TextView)infoWindow.findViewById(R.id.user_title))
	
	不可寫成:
	
	((TextView)findViewById(R.id.user_title))

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node12:使用Android POST and GET Request using HttpURLConnection 
---------------------------------------------------------------
相信大家都很想知道Android是如何跟後台資料庫、server溝通、交換資料的?
通常大家在網路上查到的方法都是使用apache的HttpClient實作，如下:

	import org.apache.http.HttpResponse;
	import org.apache.http.NameValuePair;
	import org.apache.http.client.ClientProtocolException;
	import org.apache.http.client.entity.UrlEncodedFormEntity;
	import org.apache.http.client.methods.HttpPost;
	import org.apache.http.impl.client.DefaultHttpClient;
	import org.apache.http.message.BasicNameValuePair;
	import org.apache.http.protocol.HTTP;
	import org.apache.http.util.EntityUtils;
	
	private String uriAPI = "http://192.168.1.3/httpPostTest.php";
	
	private String sendPostDataToInternet(String strTxt){/* 建立HTTP Post連線 */
	        HttpPost httpRequest = new HttpPost(uriAPI);
	        /*
	         * Post運作傳送變數必須用NameValuePair[]陣列儲存
	         */
	        List<NameValuePair> params = new ArrayList<NameValuePair>();
	        params.add(new BasicNameValuePair("data", strTxt));
	
	        try
	        {
	            /* 發出HTTP request */
	            httpRequest.setEntity(new UrlEncodedFormEntity(params, HTTP.UTF_8));
	            /* 取得HTTP response */
	            HttpResponse httpResponse = new DefaultHttpClient().execute(httpRequest);
	            /* 若狀態碼為200 ok */
	            if (httpResponse.getStatusLine().getStatusCode() == 200)
	            {
	                /* 取出回應字串 */
	                String strResult = EntityUtils.toString(httpResponse.getEntity());
	                // 回傳回應字串
	                return strResult;
	            }
	        } catch (ClientProtocolException e){
	            Toast.makeText(this, e.getMessage().toString(), Toast.LENGTH_SHORT).show();
	            e.printStackTrace();
	            
	        } catch (IOException e){
	            Toast.makeText(this, e.getMessage().toString(), Toast.LENGTH_SHORT).show();
	            e.printStackTrace();
	            
	        } catch (Exception e){
	            Toast.makeText(this, e.getMessage().toString(), Toast.LENGTH_SHORT).show();
	            e.printStackTrace();
	            
	        }
	        returnnull;
	}

看到這裡先別太興奮，必須告訴大家一個壞消息，就是從Android API 23之後，將不再支援(內建)apache的HttpClient函式庫(我寫這筆記時，API已經出到25...)，因為Google認為不合適，基本上具體說法如下([參考資料](http://android-developers.blogspot.nl/2011/09/androids-http-clients.html)):

	Apache HttpClient:
	"DefaultHttpClient" and its sibling "AndroidHttpClient" are extensible HTTP clients suitable for web browsers. 
	They have large and flexible APIs. Their implementation is stable and they have few bugs.But the large size of
	this API makes it difficult for us to improve it without breaking compatibility. The Android team is not 
	actively working on Apache HTTP Client.

	HttpURLConnection:
	"HttpURLConnection" is a general-purpose, lightweight HTTP client suitable for most applications. This class 
	has humble beginnings, but its focused API has made it easy for us to improve steadily.

因此Google官方在API23之後，改成使用輕量的HttpURLConnection內建函式庫來實作，不但不需要引入其他 Library, 也沒有甚麼前置作業，可說是以種新的用法。(官方說法如下)([參考資料](https://developer.android.com/training/basics/network-ops/connecting.html))

	Choose an HTTP Client
	Most network-connected Android apps use HTTP to send and receive data. The Android platform includes the 
	"HttpURLConnection" client, which supports HTTPS, streaming uploads and downloads, configurable timeouts,
	IPv6, and connection pooling.
	
來看看實際API內部Android.jar檔比較:

1.API23的內建函式庫
![know](/AndroidHTTP1.jpg)
2.API22的內建函式庫
![know](/AndroidHTTP2.jpg)
很明顯的看出Google拿掉了apache原始的http函式庫，而改用HttpURLConnection。
	
這裡就提供一個範例:
	
	import java.io.BufferedReader;
	import java.io.DataOutputStream;
	import java.io.IOException;
	import java.io.InputStreamReader;
	import java.net.HttpURLConnection;
	import java.net.MalformedURLException;
	import java.net.URL;
	import javax.net.ssl.HttpsURLConnection;
	import android.app.Activity;
	import android.app.ProgressDialog;
	import android.content.Context;
	import android.os.AsyncTask;
	import android.os.Bundle;
	import android.support.v7.app.ActionBarActivity;
	import android.view.View;
	import android.widget.TextView;
	
	public class MainActivity extends Activity {
	
	    private ProgressDialog progress;
	
	    @Override
	    protected void onCreate(Bundle savedInstanceState) {
	        super.onCreate(savedInstanceState);
	        setContentView(R.layout.activity_main);
	
	    }
	    
	    public class Web_update implements Button.OnClickListener{
	     	@Override
	     	public void onClick(View v) {
	        	 sendGetRequest();
	     	}
	    }
	
	    public void sendPostRequest(View View) {
	        new PostClass(this).execute();
	    }
	
	    public void sendGetRequest(View View) {
	        new GetClass(this).execute();
	    }
	
	    private class PostClass extends AsyncTask<String, Void, Void> {
	
	        private final Context context;
	
	        public PostClass(Context c){
	
	            this.context = c;
	//            this.error = status;
	//            this.type = t;
	        }
	
	        protected void onPreExecute(){
	            progress= new ProgressDialog(this.context);
	            progress.setMessage("Loading");
	            progress.show();
	        }
	
	        @Override
	        protected Void doInBackground(String... params) {
	            try {
	
	                final TextView outputView = (TextView) findViewById(R.id.showOutput);
	                URL url = new URL("http://requestb.in/1cs29cy1");
	
	                HttpURLConnection connection = (HttpURLConnection)url.openConnection();
	                String urlParameters = "fizz=buzz";
	                connection.setRequestMethod("POST");
	                connection.setRequestProperty("USER-AGENT", "Mozilla/5.0");
	                connection.setRequestProperty("ACCEPT-LANGUAGE", "en-US,en;0.5");
	                connection.setDoOutput(true);
	                DataOutputStream dStream = new DataOutputStream(connection.getOutputStream());
	                dStream.writeBytes(urlParameters);
	                dStream.flush();
	                dStream.close();
	                int responseCode = connection.getResponseCode();
	
	                System.out.println("\nSending 'POST' request to URL : " + url);
	                System.out.println("Post parameters : " + urlParameters);
	                System.out.println("Response Code : " + responseCode);
	
	                final StringBuilder output = new StringBuilder("Request URL " + url);
	                output.append(System.getProperty("line.separator") + "Request Parameters " + urlParameters);
	                output.append(System.getProperty("line.separator")  + "Response Code " + responseCode);
	                output.append(System.getProperty("line.separator")  + "Type " + "POST");
	                BufferedReader br = new BufferedReader(new InputStreamReader(connection.getInputStream()));
	                String line = "";
	                StringBuilder responseOutput = new StringBuilder();
	                System.out.println("output===============" + br);
	                while((line = br.readLine()) != null ) {
	                    responseOutput.append(line);
	                }
	                br.close();
	
	                output.append(System.getProperty("line.separator") + "Response " + System.getProperty("line.separator") + System.getProperty("line.separator") + responseOutput.toString());
	
	                MainActivity.this.runOnUiThread(new Runnable() {
	
	                    @Override
	                    public void run() {
	                        outputView.setText(output);
	                        progress.dismiss();
	                    }
	                });
	
	
	            } catch (MalformedURLException e) {
	                // TODO Auto-generated catch block
	                e.printStackTrace();
	            } catch (IOException e) {
	                // TODO Auto-generated catch block
	                e.printStackTrace();
	            }
	            return null;
	        }
	
	        protected void onPostExecute() {
	            progress.dismiss();
	        }
	
	    }
	
	    private class GetClass extends AsyncTask<String, Void, Void> {
	
	        private final Context context;
	
	        public GetClass(Context c){
	            this.context = c;
	        }
	
	        protected void onPreExecute(){
	            progress= new ProgressDialog(this.context);
	            progress.setMessage("Loading");
	            progress.show();
	        }
	
	        @Override
	        protected Void doInBackground(String... params) {
	            try {
	
	                final TextView outputView = (TextView) findViewById(R.id.showOutput);
	                URL url = new URL("http://requestb.in/1cs29cy1");
	
	                HttpURLConnection connection = (HttpURLConnection)url.openConnection();
	                String urlParameters = "fizz=buzz";
	                connection.setRequestMethod("GET");
	                connection.setRequestProperty("USER-AGENT", "Mozilla/5.0");
	                connection.setRequestProperty("ACCEPT-LANGUAGE", "en-US,en;0.5");
	
	                int responseCode = connection.getResponseCode();
	
	                System.out.println("\nSending 'POST' request to URL : " + url);
	                System.out.println("Post parameters : " + urlParameters);
	                System.out.println("Response Code : " + responseCode);
	
	                final StringBuilder output = new StringBuilder("Request URL " + url);
	                //output.append(System.getProperty("line.separator") + "Request Parameters " + urlParameters);
	                output.append(System.getProperty("line.separator")  + "Response Code " + responseCode);
	                output.append(System.getProperty("line.separator")  + "Type " + "GET");
	                BufferedReader br = new BufferedReader(new InputStreamReader(connection.getInputStream()));
	                String line = "";
	                StringBuilder responseOutput = new StringBuilder();
	                System.out.println("output===============" + br);
	                while((line = br.readLine()) != null ) {
	                    responseOutput.append(line);
	                }
	                br.close();
	
	                output.append(System.getProperty("line.separator") + "Response " + System.getProperty("line.separator") + System.getProperty("line.separator") + responseOutput.toString());
	
	                MainActivity.this.runOnUiThread(new Runnable() {
	
	                    @Override
	                    public void run() {
	                        outputView.setText(output);
	                        progress.dismiss();
	
	                    }
	                });
	
	
	            } catch (MalformedURLException e) {
	                // TODO Auto-generated catch block
	                e.printStackTrace();
	            } catch (IOException e) {
	                // TODO Auto-generated catch block
	                e.printStackTrace();
	            }
	            return null;
	        }
	
	//        protected void onPostExecute() {
	//            progress.dismiss();
	//        }
	
	    }
	
	
	}

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node13:Snackbar用法及注意事項 
---------------------------------------------------------------
Snackbar 使用方法是跟 Toast 一樣：

	Snackbar.make(contentView, "I am snackbar", Snackbar.LENGTH_SHORT).show();

跟 Toast 不同的是，Snackbar 是以 view 作參數，而不是以 context。這確保 Snackbar 只在有 view 顯示時才出現，不會跟 Toast 般被濫用，在背景 Service 中執行 toast.show()，引致用戶跟本不知是那個 app 在顯示通知的問題。
舉例來說:
針對FloatingActionButton存在時才顯示helloworld資訊:

	FloatingActionButton fab=(FloatingActionButton)findViewById(R.id.fab);
	Snackbar.make(fab, "helloworld", Snackbar.LENGTH_SHORT).show();
	
也就是說若現在使用者正在觀看的頁面並沒有FloatingActionButton這個View，則即使條件觸發也不會顯示helloworld.

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node14:method預設大小限制64K的問題
----------------------------------
今天遇到一個很奇特的問題，原因是我撰寫的介面本身太大，然後在燒錄到手機時被AndroidStudio擋下來，AndroidStudio表示:

	Error:The number of method references in a .dex file cannot exceed 64K. 
	Learn how to resolve this issue at https://developer.android.com/tools/building/multidex.html

簡單說明一下:在Android系統中，一個App的所有代碼都在一個Dex文件裡面。Dex是一個類似Jar、存儲了很多Java編譯過的歸檔文件。因為Android系統使用Dalvik虛擬機，所以需要把使用JavaCompiler編譯之後的class文件轉換成Dalvik能夠執行的class文件。這裡需要強調的是，Dex和Jar一樣是一個歸檔文件，裡面仍然是Java代碼對應的字節碼文件。當Android系統啟動一個應用的時候，有一步是對Dex進行優化，這個過程有一個專門的工具來處理，叫DexOpt。DexOpt的執行過程是在第一次加載Dex文件的時候執行的。這個過程會生成一個ODEX文件，即Optimised Dex。
執行ODex的效率會比直接執行Dex文件的效率要高很多。但是在早期的Android系統中，DexOpt的LinearAlloc存在著限制: Android 2.2和2.3的緩衝區只有5MB，Android 4.x提高到了8MB或16MB。當方法數量過多導致超出緩衝區大小時，會造成dexopt崩潰，導致無法安裝。

另外由於DEX文件格式限制，一個DEX文件中method個數採用使用原生類型short來索引文件中的方法，也就是4個字節共計最多表達65536個method，field/class的個數也均有此限制。對於DEX文件，則是將工程所需全部class文件合併且壓縮到一個DEX文件期間，也就是Android打包的DEX過程中， 單個DEX文件可被引用的方法總數被限制為65536（自己開發以及所引用的Android Framework和第三方類庫的代碼）。

解決方法:
1.在build.gradle(app)中加入下列設定:

	android {
	    compileSdkVersion 21
	    buildToolsVersion "21.1.0"
	    defaultConfig {
	        ...
	        minSdkVersion 14
	        targetSdkVersion 21
	        ...
	
	        // Enabling multidex support.
	        multiDexEnabled true     <---------this
	    }
	    ...
	}
	
	dependencies {
	  compile 'com.android.support:multidex:1.+'     <---------this
	}

2.在AndroidManifest中加入:

	<application
	        ...
	        android:name="android.support.multidex.MultiDexApplication">
	        ...
	</application>
	
在此要特別注意，此解決方式是針對Android版本5.0以下的手機，由官方文件可知:
	
	Multidex support for Android 5.0 and higher.

因此若燒入對象是Android5.0以上的手機，因該是不太會出現此錯誤的。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node15:引入Gradle插件(這次是github的)所遇到的問題與解法
-------------------------------------------------------
昨天晚上由於因為製作專案的需要，引入別人寫好的gradle插件，別人寫好的插件是放在gihub上，所以提供了直接compile的功能，
正當我興奮地引入插件，並等待gradle build完成時，Android Studio跳出了一個錯誤，如下:

	Error:Execution failed for task ':app:processDebugManifest'. > Manifest merger failed with multiple errors, see logs

這..這啥?不是已經是寫好的嗎?怎麼會跳出此錯誤...後來上網查，了解此錯誤會發生的原因是因為:AndroidStudio的Gradle插件默認會啟用Manifest Merger Tool，若Library項目中也定義了與主項目相同的屬性（例如默認生成的android:icon和android:theme），則此時會合並失敗，並報上面的錯誤。知道原因後，開始找解法，網上的解決方式如下:

	法1.在Manifest.xml的application標簽下添加tools:replace="android:icon, android:theme"
	（多個屬性用,隔開，並且記住在manifest根標簽上加入xmlns:tools="http://schemas.android.com/tools"，否則會找不到namespace哦）
	ex: <manifest xmlns:android="http://schemas.android.com/apk/res/android"
		    package="com.xxxx.xxxx"
		    xmlns:tools="http://schemas.android.com/tools"
		    >...
		    <application
		        android:name="com.xxxx.xxxx.xxApplication"
		        android:allowBackup="false"
		        android:icon="@drawable/ic_launcher"
		        android:label="@string/app_name"
		        android:theme="@style/Theme.Sherlock"
		        tools:replace="name,icon,label,theme">
		        ...

	法2.在build.gradle根標簽上加上 useOldManifestMerger true (非正式用法)
	
知道解法了~好開心~趕快來解決問題，結果......
我昨天晚上試了一整晚都失敗，猛跳一樣的錯誤QQ，我的天啊，怎麼試都會錯，還害我差點用壞我原本的專案，於是只好放棄去睡覺。
隔天我想說我開個新專案再來試試，這次是用一個空白的專案，結果也跳了一個錯誤，如下:
	
	Manifest merger failed : uses-sdk:minSdkVersion 15 cannot be smaller than version 19 declared in library [io.github.controlwear:virtualjoystick:0.9.9] C:\Users\user\AndroidStudioProjects\Joytest\app\build\intermediates\exploded-aar\io.github.controlwear\virtualjoystick\0.9.9\AndroidManifest.xml
	Suggestion: use tools:overrideLibrary="io.github.controlwear.virtual.joystick.android" to force usage
	
意思是說我的專案最低sdk是15不符合我引入的這個插件最低sdk是19的需求，這...這甚麼東西啊，怎麼跟我昨天遇到的不一樣(AndroidStudio常這樣)，依然找解決方法，如下:

	法1.把minSdkVersion 15改成minSdkVersion 19阿，都跟你說了最低版本不合了吼
	
	法2.在Manifest.xml添加:
		<manifest xmlns:android="http://schemas.android.com/apk/res/android"
		    package="com.xxxx.xxxx"
		    xmlns:tools="http://schemas.android.com/tools"
		    >...
		<uses-sdk  tools:overrideLibrary="io.github.controlwear.virtual.joystick.android"></uses-sdk>

我使用第2個方法，然後就很神奇地解決了，也可以放入原本的專案了......雖然不知道怎麼回事，但至少兩種問題都知道如何解決XD。

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node16:GoogleMap畫線問題
---------------------------------------
基本上畫線其實很簡單，只要找到兩個座標，用PolylineOptions設定畫線顏色，然後用Polyline將線畫在map上，只有這樣，
若要動態增加畫線，例如點擊地圖某處立即畫線，可以使用onMapClickListener監聽然後用Polyline.setpoint動態加入點，例如:

	//===================set map click mark==========================
	final List<LatLng> latLng2=new ArrayList(); //此陣列是為了將之後路線規劃所有的點存起來並用setPoints()畫出
        map.setOnMapClickListener(new GoogleMap.OnMapClickListener() { //每點擊一次map就將點擊的座標加入latLng2，並畫線
            @Override
            public void onMapClick(LatLng latLng) {
                //Toast.makeText(FollowFixPoint.this,latLng.latitude+" "+latLng.longitude,Toast.LENGTH_SHORT).show();
                latLng2.add(new LatLng(latLng.latitude,latLng.longitude));
                MarkerOptions markerOptions = new MarkerOptions();
                markerOptions.position(latLng2.get(latLng2.size()-1));
                polyline.setPoints(latLng2);
                map.addMarker(markerOptions);
            }
        });
        
今天一如往常的要加入畫線功能，然後就很神奇的我的線就是一直畫不出來，重點是compiler、AndroidStudio都沒出錯，也沒意外，
然後點擊的座標也成功的收到，但是他x的線就是不會顯示，我一直檢查到底哪裡寫錯，但是依照往常我之前成功的案例，目前寫法跟
本就沒錯啊，啊我的線勒?，我還調整線的寬度調到超大，深怕是線太細，結果還是出不來，正當我失望之際，忽然靈光乍現，光明在前
，我靈機一動，開始檢查所有與GoogleMap有關的所有我寫的code，檢查什麼?1.檢查是否有其他有關Map的觸發函式，檢查的原因在於Android
把googlemap視為一個view，但一個view的onclickListener通常只會有一個，也就是只能Override一次，也就是說若同時在一個map中同
時存在多個Onclicklistener，即使針對的是不同的物件，例如一個是針對map本身，一個是針對map中，某個mark上的button(自訂mark(自己上網查))
Android會分辨不出是哪一個事件觸發，因為都在同一個view中，通常若有遇到過的都知道，此情況如果發生，AndroidStudio也不會發
生錯誤，Android會以map本身觸發為主，而自動忽略mark的button的觸發，所以要避免此種狀況；2.檢查與之前成功的code不同之處在
哪，因為有時候問題的出現不是因為你寫錯，而是因為某些條件影響了你寫的功能，造成你的功能出現衝突，這次問題能夠解決，是因
為我苦惱了一整天，終於發現畫線出不來的問題在於，我有撰寫GPS功能，而依照GPS功能，遇到位置改變時會更新座標，因此我猜我畫
線的顯示部分，被GPS更新時重設了，因為GPScode搶走了我的map畫面的觸發事件，使的我的map畫面更新(畫線)被無視掉QQ，種之把GPS
code移除問題就解決了，至於那定位怎麼辦?可以在別的頁面先定位後，再用intent將參數傳遞過來就好了，總之問題解決了~

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node17:依螢幕動態調整大小問題
---------------------------------------
相信很多人都會遇到一個問題，就是當你寫的code燒入到螢幕大小不同的手機，會發現排版和原先的設計不一樣，此時要如何解決呢?
先給個範例:

	 //===================依照螢幕尺寸調整layout大小==================
        DisplayMetrics metrics = new DisplayMetrics();
        getWindowManager().getDefaultDisplay().getMetrics(metrics);  //先取得螢幕尺寸(pixel)
        int vWidth = metrics.widthPixels;
        int vHeight = metrics.heightPixels;
        RelativeLayout relativeLayout=(RelativeLayout) findViewById(R.id.fix_map_linear);
        relativeLayout.getLayoutParams().height=(int)(vHeight*0.7);  //針對map進行尺寸調整
        
假如我有個map要顯示，而且固定站螢幕高度70%此時就可以用上面的方式，先取出螢幕大小後，再指定對應包住mapframe的layout，動態
改變大小，是不是很簡單~

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node18:Android 中的 Thread 傳遞資料的方式
-----------------------------------------
>現代的作業系統為了講求多工，基本上皆支援多執行序，也就是MultiThread，讓一個程序在運行的同時，也能呼叫另一個程序執行，使的在同一時間可以有多個程序同時執行，而我們現在就來介紹在AndroidOS中多執行序的概念與寫法。

>在介紹Thread之前,我們必須先把Program和Process這兩個觀念作一個釐清:
>>+ Program:一群程式碼的集合,用以解決特定的問題。以物件導向的觀念來類比,相當於Class。
>>+ Process:由Program所產生的執行個體(一個正在執行的program叫process(恐龍本)),一個Program可以同時執行多次,產生多個Process。以物件導向的觀念來類比,相當於Object。每一個Process又由以下兩個東西組成:

>>>>1. 一個Memory Space。相當於Object的variable,不同Process的Memory Space也不同,彼此看不到對方的Memory Space。
>>>>2. 一個以上的Thread。Thread代表從某個起始點開始(例如main),到目前為止所有函數的呼叫路徑,以及這些呼叫路徑上所用到的區域變數。當然程式的執行狀態,除了紀錄在主記憶體外,CPU內部的暫存器(如Program Counter, Stack Pointer, Program Status Word等)也需要一起紀錄。所以Thread又由下面兩項組成:

>>>>>>- Stack:紀錄函數呼叫路徑,以及這些函數所用到的區域變數(MIPS中的$sp)
>>>>>>- 目前CPU的狀態(恐龍本)

>由上面的描述中,我們在歸納Thread的重點如下:
>>>1. 一個Process可以有多個Thread。
>>>2. 同一個Process內的Thread使用相同的Memory Space,但這些Thread各自擁有其Stack。換句話說,Thread能透過reference存取到相同的Object,但是local variable卻是各自獨立的。
>>>3. 作業系統會根據Thread的優先權以及已經用掉的CPU時間,在不同的Thread作切換,以讓各個Thread都有機會執行。

>Java以java.lang.Thread這個類別來表示Thread。Class Thread有兩個Constructor:
>>>1. Thread();
>>>2. Thread(Runnable);
>第一個Constrctor沒有參數,第二個需要一個Runnable物件當參數。
>Runnable是一個interface,定義於java.lang內,其宣告為:

	public interface Runnable {
    		public void run();
	}
	
>使用Thread()產生的Thread,其進入點為Thread裡的run();使用Thread(Runnable)產生的Thread,其進入點為Runnable物件裡的run()。
>當run()結束時,這個Thread也就結束了;這和main()結束有相同的效果。其用法以下面範例說明:

	Thread寫法:
	public class ThreadExample1 extends Thread {
	    public void run() { 						// override Thread's run()
			System.out.println("Here is the starting point of Thread.");
			for (;;) { 							// infinite loop to print message
				System.out.println("User Created Thread");
			}
	    }
	    public static void main(String[] argv) {
			Thread t = new ThreadExample1(); 				// 產生Thread物件
			t.start(); 							// 開始執行t.run()
			for (;;) {
				System.out.println("Main Thread");
			}
	    }
	}
	
>以上程式執行後,螢幕上會持續印出"User Created Thread"或"Main Thread"的字樣。
	
	Runnable寫法:
	public class ThreadExample2 implements Runnable {
	    public void run() { 						// implements Runnable run()
			System.out.println("Here is the starting point of Thread.");
			for (;;) { 							// infinite loop to print message
			    System.out.println("User Created Thread");
			}
	    }
	    public static void main(String[] argv) {
			Thread t = new Thread(new ThreadExample2()); 			// 產生Thread物件
			t.start(); 							// 開始執行Runnable.run();
			for (;;) {
			    System.out.println("Main Thread");
			}
	    }
	}


>	在Android中Android UI不是Thread Safe，所以 UI 的互動均由"Main Thread"負責，即執行Activity的那個Thread(例如預設專案中的MainActivity)，其他 Thread 均不能更新 UI，基於 UI 的親善，Main Thread不可以執行費時的工作，否則 User 會因此看到一個失能的 UI 而暴走，因此當Main Thread出現五秒以上的運算時，Android就會丟出 ANR(Application not Responsed)讓 User 可以選擇等待或離去。另外Main Thread中的onCreate()運算如果超過10秒，也會跳出ANR警告。因此有關費時的工作包括網路存取、檔案處理、資料庫讀取或僅只是費時的計算皆要利用其他thread運作。

>#####要做到背景執行，可以使用 Service、Thread 及 AsyncTask 這 3 種類別。

>既然已經知道Android(java)產生Thread的兩大方式，接下來將介紹AndroidThread的溝通方式。
>以下列出列出五種 Android Thread 之間傳遞資料的方式:
>>>1. 單向資料管道(pipe)
>>>2. 共用記憶體(ShareMemory)
>>>3. Blocking Queue: Producer-Consumer Pattern
>>>4. Message Queue
>>>5. 將任務(task)回傳給 Thread

>1.單向資料管道(pipe)
>>範例中用 PipedWrite, PipedReader 建立單向資料傳遞。worker thread 可持續讀取 UI thread 產生的文字資料。

![know](/Android Thread 溝通方式.001.png)

	public class PipeExampleActivity extends Activity {

	    PipedReader r;
	    PipedWriter w;

	    private Thread workerThread;

	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);

			r = new PipedReader();
			w = new PipedWriter();

			try {
			    	w.connect(r);
			} catch (IOException e) {
			    	e.printStackTrace();
			}

			workerThread = new Thread(new TextHandlerTask(r));
			workerThread.start();

			// w.write(); 可持續傳送字串到 TextHandlerTask 另一個讀取資料的 Thread
	    }

	    private static class TextHandlerTask implements Runnable {
			private final PipedReader reader;

			public TextHandlerTask(PipedReader reader){
			    	this.reader = reader;
			}
			@Override
			public void run() {
				    while(!Thread.currentThread().isInterrupted()){
						try {
							    int i;
							    while((i = reader.read()) != -1){
									char c = (char) i;
									//ADD TEXT PROCESSING LOGIC HERE
									Log.d(TAG, "char = " + c);
							    }

						} catch (IOException e) {
						    	e.printStackTrace();
						}
				    }
			}
	    }
	}

>2.共用記憶體(ShareMemory)

![know](/Android Thread 溝通方式.002.png)

>>如果物件屬於以下這幾種，就會被儲存在共用記憶體中，物件的 reference 會儲存在執行緒的 stack:
>>>>1. 實例成員變數
>>>>2. 類別成員變數
>>>>3. 方法中宣告的物件
>>執行緒的信號通知機制:

![Know](/Thread message info.jpg)

>3.Blocking Queue: Producer-Consumer Pattern

![know](/Android Thread 溝通方式.003.png)

	public class ConsumerProducer {
	    private final int LIMIT=10;
	    private BlockingQueue<Integer> blockingQueue = new LinkedBlockingQueue<Integer>(LIMIT);

	    private void produce throws InterruptedException {
			int value=0;
			while(true) {
			    	blockingQueue.put(value);
			}
	    }

	    public void consume throws InterruptedException {
			while(true) {
			    	int value = blockingQueue.take();
			}
	    }
	}

>4.Message Queue
>>Message Queue 是最適合用在 Android APP 的溝通機制。

![know](/Android Thread 溝通方式.004.png)

>>>>1. Insert: 利用連接到 consumer thread 的 Handler，producer thread 將訊息插入 queue
>>>>2. Get: consumer thread 會執行 Looper，從 queue 裡面取得訊息
>>>>3. Deliver: Handler 負責處理 consumer thread 的訊息。Thread 可以有多個 Handler instance 來處理訊息，Looper 可確保訊息被送到正確的 Handler。

>>UI thread 是唯一預設就與 Looper 相關連的執行緒，UI Looper跟其他 Looper 有些差異:
>>>>1. 它可以在任何地方被存取: Looper.getMainLooper() 
>>>>2. 不能被終止： Looper.quit 會丟出 RuntimeException 
>>>>3. 執行時，透過 Looper.prepareMainLooper() 把 Looper 關聯到 UI thread，每個 APP 都只能做一次

>>基本的訊息發送範例:

	public class LooperActivity extends Activity {

	    LooperThread mLooperThread;

	    // 定義 worker thread
	    private static class LooperThread extends Thread {

			public Handler mHandler;

			public void run() {
				    // 將 Looper 與 worker thread 連結在一起
				    Looper.prepare();
				    // 設定 Handler，讓 producer 可以插入訊息
				    mHandler = new Handler() {
						// 當訊息被送到 worker thread 時的 callback
						public void handleMessage(Message msg) {
							    if(msg.what == 0) {
									doLongRunningOperation();
							    }
						}
				    };
				    // blocking 呼叫，讓 message queue 可發送訊息給 consumer thread
				    Looper.loop();
			}

			private void doLongRunningOperation() {
			    	// Add long running operation here.
			}
	    }

	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_looper);
			// 啟動 worker thread
			mLooperThread = new LooperThread();
			mLooperThread.start();
	    }

	    public void onClick(View v) {
			if (mLooperThread.mHandler != null) {
				    // 初始化 message
				    Message msg = mLooperThread.mHandler.obtainMessage(0);
				    // 發送訊息mLooperThread.mHandler.sendMessage(msg);
			}
	    }

	    protected void onDestroy() {
			super.onDestroy();
			// 終止 worker thead，讓 Looper.loop 結束 blocking
			mLooperThread.mHandler.getLooper().quit();
	    }
	}

>>如果有一段時間沒有訊息，就會進入 IdleHandler

	public class ConsumeAndQuitThreadActivity extends Activity {
	
	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);

			final ConsumeAndQuitThread consumeAndQuitThread = new ConsumeAndQuitThread();
			consumeAndQuitThread.start();

			// 模擬多個 threads 隨機插入訊息
			for (int i = 0; i < 10; i++) {
				    new Thread(new Runnable() {
						@Override
						public void run() {
							    for (int i = 0; i < 10; i++) {
									SystemClock.sleep(new Random().nextInt(10));
									consumeAndQuitThread.enqueueData(i);
							    }
						}
				    }).start();
			}
	    }

	    private static class ConsumeAndQuitThread extends Thread implements MessageQueue.IdleHandler {

			private static final String THREAD_NAME = "ConsumeAndQuitThread";

			public Handler mConsumerHandler;
			private boolean mIsFirstIdle = true;

			public ConsumeAndQuitThread() {
			    	super(THREAD_NAME);
			}

			@Override
			public void run() {
				    Looper.prepare();

				    mConsumerHandler = new Handler() {
						@Override
						public void handleMessage(Message msg) {
						    // Consume data
						}
				    };
				    // 在啟動背景執行緒時，註冊 IdleHandler
				    Looper.myQueue().addIdleHandler(this);
				    Looper.loop();
			}


			@Override
			public boolean queueIdle() {
				    if (mIsFirstIdle) {
						// 不處理第一次的 idle
						mIsFirstIdle = false;
						return true;
				    }
				    // 發生 idle 時，終止該執行緒
				    mConsumerHandler.getLooper().quit();
				    return false;
			}

			public void enqueueData(int i) {
			    	mConsumerHandler.sendEmptyMessage(i);
			}
	    }
	}

>>以下是資料訊息

	Message.obtain(Handler h);
	Message.obtain(Handler h, int what);
	Message.obtain(Handler h, int what, Object o);
	Message.obtain(Handler h, int what, int arg1, int arg2);
	Message.obtain(Handler h, int what, int arg1, int arg2, Object o);
	
>>將資料訊息插入 message queue

	boolean sendMessage(Message msg)
	boolean sendMessageAtFrontOfQueue(Message msg)
	boolean sendMessageAtTime(Message msg, long uptimeMillis)
	boolean sendMessageDelayed(Message msg, long delayMillis)

	// 簡單的訊息
	boolean sendEmptyMessage(int what)
	boolean sendEmptyMessageAtTime(int what, long uptimeMillis)
	boolean sendEmptyMessageDelayed(int what, long delayMillis)
	
>>以下是任務訊息

	//產生訊息時，同時指定 handler
	Message m = Message.obtain(handler, runnable);
	m.sendToTarget();

>>將任務訊息插入 message queue

	boolean post(Runnable r)
	boolean postAtFrontOfQueue(Runnable r)
	boolean postAtTime(Runnable r, Object token, long uptimeMillis)
	boolean post(Runnable r, long uptimeMillis)
	boolean postDelayed(Runnable r, long delayMillis)

>>雙向傳遞訊息的範例

	public class HandlerExampleActivity extends Activity {

	    private final static int SHOW_PROGRESS_BAR = 1;
	    private final static int HIDE_PROGRESS_BAR = 0;
	    private BackgroundThread mBackgroundThread;

	    private TextView mText;
	    private Button mButton;
	    private ProgressBar mProgressBar;

	    @Override
	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_handler_example);

			// 當 activity 建立時，就啟動背景執行緒，處理來自 UI thread 的任務
			mBackgroundThread = new BackgroundThread();
			mBackgroundThread.start();

			mText = (TextView) findViewById(R.id.text);
			mProgressBar = (ProgressBar) findViewById(R.id.progress);
			mButton = (Button) findViewById(R.id.button);
			mButton.setOnClickListener(new View.OnClickListener() {
				    @Override
				    public void onClick(View v) {
						// 點擊按鈕，將任務傳送給背景執行緒
						mBackgroundThread.doWork();
				    }
			});
	    }

	    @Override
	    protected void onDestroy() {
			super.onDestroy();
			// 停止背景執行緒
			mBackgroundThread.exit();
	    }

	    private final Handler mUiHandler = new Handler() {
			public void handleMessage(Message msg) {

				    switch(msg.what) {
						case SHOW_PROGRESS_BAR:
							    mProgressBar.setVisibility(View.VISIBLE);
							    break;
						case HIDE_PROGRESS_BAR:
							    mText.setText(String.valueOf(msg.arg1));
							    mProgressBar.setVisibility(View.INVISIBLE);
							    break;
				    }
			}
	    };

	    private class BackgroundThread extends Thread {

			private Handler mBackgroundHandler;

			public void run() {
				    // 將 looper 與這個執行緒關聯起來
				    Looper.prepare();
				    // 此 Handler 只處理 Runnable
				    mBackgroundHandler = new Handler();
				    Looper.loop();
			}

			public void doWork() {
				    mBackgroundHandler.post(new Runnable() {
						@Override
						public void run() {
							    // 建立只傳送 what 的 Message 物件，讓 Progress Bar 更新進度
							    Message uiMsg = mUiHandler.obtainMessage(SHOW_PROGRESS_BAR, 0,
								    0, null);
							    // 傳送訊息
							    mUiHandler.sendMessage(uiMsg);

							    Random r = new Random();
							    int randomInt = r.nextInt(5000);
							    SystemClock.sleep(randomInt);

							    // 建立物件，用來移除 progress bar
							    uiMsg = mUiHandler.obtainMessage(HIDE_PROGRESS_BAR, randomInt,
								    0, null);
							    mUiHandler.sendMessage(uiMsg);
						}
				    });
			}

			public void exit() {
			    	mBackgroundHandler.getLooper().quit();
			}
		    }
	}

>>Handler 也可以利用 Callback interface 建立

	public class HandlerCallbackActivity extends Activity implements Handler.Callback {

	    @Override
	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_handler_callback);
	    }

	    @Override
	    public boolean handleMessage(Message msg) {
			switch (msg.what) {
				    case 1:
						msg.what = 11;
						return true;
				    default:
						msg.what = 22;
						return false;
			}
	    }

	    public void onHandlerCallback(View v) {
			Handler handler = new Handler(this) {
				    @Override
				    public void handleMessage(Message msg) {
						// Process message
				    }
			};
			// 插入訊息，該訊息會被 Callback 攔截
			handler.sendEmptyMessage(1);
			handler.sendEmptyMessage(2);
	    }
	}
	
>>觀察 message queue 的方法，為目前的 message queue 產生 snapshot

	public class MQDebugActivity extends Activity {

	    private static final String TAG = "EAT";
	    Handler mWorkerHandler;

	    public void onCreate(Bundle savedInstanceState) {
			super.onCreate(savedInstanceState);
			setContentView(R.layout.activity_mq_debug);

			Thread t = new Thread() {
				    @Override
				    public void run() {
						Looper.prepare();
						mWorkerHandler = new Handler() {
							    @Override
							    public void handleMessage(Message msg) {
									Log.d(TAG, "handleMessage - what = " + msg.what);
							    }
						};
						Looper.loop();
				    }
			};
			t.start();
	    }

	    // Called on button click, i.e. from the UI thread.
	    public void onClick(View v) {
			mWorkerHandler.sendEmptyMessageDelayed(1, 2000);
			mWorkerHandler.sendEmptyMessage(2);
			mWorkerHandler.obtainMessage(3, 0, 0, new Object()).sendToTarget();
			mWorkerHandler.sendEmptyMessageDelayed(4, 300);
			mWorkerHandler.postDelayed(new Runnable() {
				    @Override
				    public void run() {
					Log.d(TAG, "Execute");
				    }
			}, 400);
			mWorkerHandler.sendEmptyMessage(5);

			mWorkerHandler.dump(new LogPrinter(Log.DEBUG, TAG), "");
	    }
	}

>>也可以追蹤 message queue 的處理

	Looper.myLopper().setMessageLogging(new LogPrinter(Log.DEBUG, TAG))
	
>5.與 UI Thread 溝通
>>訊息透過 UI Thread 的 Looper 傳遞給 UI Thread，這個 Looper 可透過 Looper.getMainLooper() 取得。

	Runnable task = new Runnable() {...};
	new Handler(Looper.getMainLooper()).post(task);

>>UI thread 發布給自己的任務訊息，可繞過訊息傳遞機制，並透過 Activity.runOnUiThread(Runnable ) 立刻被執行。
>>可在 Application 中透過 Thread ID 的方式識別 UI thread

	public class TestApplication extends Application {
	    private long mUiThreadId;
	    private Handler mUiHandler;

	    public void onCreate() {
			super.onCreate();
			mUiThreadId = Thread.currentThread().getId();
			mUiHandler = new Handler();
	    }

	    public void customRunOnUiThread(Runnable action) {
			if( Thread.currentThread().getId() != mUiThreadId ) {
			    mUiHandler.post(action);
			} else {
			    action.run();
			}
	    }
	}


###Reference:
[http://blog.maxkit.com.tw/2016/02/android-thread-pipe-blockingqueue.html](http://blog.maxkit.com.tw/2016/02/android-thread-pipe-blockingqueue.html)
[http://programming.im.ncnu.edu.tw/J_Chapter9.htm](http://programming.im.ncnu.edu.tw/J_Chapter9.htm)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node19:Android AsyncTask----Thread之外的另一選擇
-----------------------------------------------
>要做到背景執行，可以使用 Service、Thread 及 AsyncTask 這 3 種類別。

AsyncTask (API level 3，所以幾乎所有目前在市面上流通的 Android 版本皆可使用)
是除了Thread之外的另一種選擇，Android 團隊鼓勵主執行緒(UI thread/Main thread) 專注於操作和畫面的流暢呈現，其餘工作 (如網路資料傳輸、檔案/磁碟/資料存取) 最好都在背景執行；Thread 通常要搭配 Handler 使用，而 AsyncTask 用意在簡化背景執行 Thread 程式碼的撰寫。

>如果您預期要執行的工作能在幾秒內完成，就可以選擇使用 AsyncTask，若執行的時間很長，Android 則強烈建議採用 Executor, ThreadPoolExecutor 及 FutureTask。

要使用 AsyncTask，必定要建立一個繼承自 AsyncTask 的子類別，並傳入 3 項資料：

1. Params -- 要執行 doInBackground() 時傳入的參數，數量可以不止一個 
2. Progress -- doInBackground() 執行過程中回傳給 UI thread 的資料，數量可以不止一個
3. Rsesult -- 傳回執行結果， 若您沒有參數要傳入，則填入 Void (注意 V 為大寫)。

AsyncTask<Params, Progress, Result>，這是基本的架構，使用泛型來定義參數，泛型意思是，你可以定義任意的資料型態給他。
	
	另一種解釋:
	Params ： 參數，你要餵什麼樣的參數給它。
	Progress ： 進度條，進度條的資料型態要用哪種。
	Result ： 結果，你希望這個背景任務最後會有什麼樣的結果回傳給你。
	
AsyncTask 的運作有 4 個階段：

1. onPreExecute -- AsyncTask 執行前的準備工作，例如畫面上顯示進度表，
2. doInBackground -- 實際要執行的程式碼就是寫在這裡，
3. onProgressUpdate -- 用來顯示目前的進度，
4. onPostExecute -- 執行完的結果 - Result 會傳入這裡。
>除了 doInBackground，其他 3 個 method 都是在 UI thread 呼叫

![show](/AsyncTask基本架構.jpg)

如果你要執行一個AsyncTask必須在Main Thread上面呼叫execute, 否則callback method將會傳不到。

	AsyncTask task = new MyTask();
	task.execute(/*參數*/);
	
如果你要取消一個AsyncTask可以這樣
	
	AsyncTask task = new MyTask();
	task.execute(/*參數*/);
	task.cancel(true);
	
關於 AsyncTask 的使用，有幾項原則必須遵守：

1. AsyncTask 必須在 UI 主執行緒載入(JELLY_BEAN 版本開始會自動執行此事)。 
2. 必須在 UI 主執行緒建立 AsyncTask。  
3. 必須在 UI 主執行緒呼叫 AsyncTask.execute()。  
4. 不要自行呼叫 onPreExecute()，onPostExecute()，doInBackground()， onProgressUpdate()。  
5. AsyncTask 只能執行一次。

關於AsyncTask的知識:
1.當你呼叫execute()方法時, 則會使用預設的ThreadPool, 而預設的ThreadPool只會有5個core Thread, 
因此如果超過5個task將會被放進Queue等待





node20:Android的Thread大家族(Handler、Message、Looper、MessageQueue)
-------------------------------------------------------------------
Android的消息處理有三個核心類：Looper,Handler和Message。其實還有一個Message Queue（消息隊列），但是MQ被封裝到Looper裡面了，我們不會直接與MQ打交道，因此我沒將其作為核心類。下面一一介紹：
##線程的魔法師Looper
Looper的字面意思是“循環者”，它被設計用來使一個普通線程變成Looper線程。所謂Looper線程就是循環工作的線程。在程序開發中（尤其是GUI開發中），我們經常會需要一個線程不斷循環，一旦有新任務則執行，執行完繼續等待下一個任務，這就是Looper線程。使用Looper類創建Looper線程很簡單：

	public class LooperThread extends Thread {
	    @Override
	    public void run() {
			// 将当前线程初始化为Looper线程
			Looper.prepare();

			// ...其他处理，如实例化handler

			// 开始循环处理消息队列
			Looper.loop();
	    }
	}

通過上面兩行核心代碼，你的線程就升級為Looper線程了！！！是不是很神奇？讓我們放慢鏡頭，看看這兩行代碼各自做了什麼。

1. Looper.prepare();

![show](/LooperThread.png)

通過上圖可以看到，現在你的線程中有一個Looper對象，它的內部維護了一個消息隊列MQ。注意，一個Thread只能有一個Looper對象，為什麼呢？咱們來看源碼。

	public class Looper {
	    // 每个线程中的Looper对象其实是一个ThreadLocal，即线程本地存储(TLS)对象
	    private static final ThreadLocal sThreadLocal = new ThreadLocal();
	    // Looper内的消息队列
	    final MessageQueue mQueue;
	    // 当前线程
	    Thread mThread;
	    // 。。。其他属性

	    // 每个Looper对象中有它的消息队列，和它所属的线程
	    private Looper() {
		mQueue = new MessageQueue();
		mRun = true;
		mThread = Thread.currentThread();
	    }

	    // 我们调用该方法会在调用线程的TLS中创建Looper对象
	    public static final void prepare() {
		if (sThreadLocal.get() != null) {
		    // 试图在有Looper的线程中再次创建Looper将抛出异常
		    throw new RuntimeException("Only one Looper may be created per thread");
		}
		sThreadLocal.set(new Looper());
	    }
	    // 其他方法
	}

通過源碼，prepare()背後的工作方式一目了然，其核心就是將looper對象定義為ThreadLocal。如果你還不清楚什麼是ThreadLocal，請參考[理解ThreadLocal](http://blog.csdn.net/qjyong/article/details/2158097)。

2. Looper.loop();

![show](/LooperLoop.png)

調用loop方法後，Looper線程就開始真正工作了，它不斷從自己的MQ中取出隊頭的消息(也叫任務)執行。其源碼分析如下：

	public static final void loop() {
		Looper me = myLooper();  //得到当前线程Looper
		MessageQueue queue = me.mQueue;  //得到当前looper的MQ

		// 这两行没看懂= = 不过不影响理解
		Binder.clearCallingIdentity();
		final long ident = Binder.clearCallingIdentity();
		// 开始循环
		while (true) {
		    Message msg = queue.next(); // 取出message
		    if (msg != null) {
			if (msg.target == null) {
			    // message没有target为结束信号，退出循环
			    return;
			}
			// 日志。。。
			if (me.mLogging!= null) me.mLogging.println(
				">>>>> Dispatching to " + msg.target + " "
				+ msg.callback + ": " + msg.what
				);
			// 非常重要！将真正的处理工作交给message的target，即后面要讲的handler
			msg.target.dispatchMessage(msg);
			// 还是日志。。。
			if (me.mLogging!= null) me.mLogging.println(
				".......");

			// 下面没看懂，同样不影响理解
			final long newIdent = Binder.clearCallingIdentity();
			if (ident != newIdent) {
			    Log.wtf("Looper", "Thread identity changed from 0x"
				    + Long.toHexString(ident) + " to 0x"
				    + Long.toHexString(newIdent) + " while dispatching to "
				    + msg.target.getClass().getName() + " "
				    + msg.callback + " what=" + msg.what);
			}
			// 回收message资源
			msg.recycle();
		    }
		}
	}

除了prepare()和loop()方法，Looper類還提供了一些有用的方法，比如
Looper.myLooper()得到當前線程looper對象：

	public static final Looper myLooper() {
		// 在任意线程调用Looper.myLooper()返回的都是那个线程的looper
		return (Looper)sThreadLocal.get();
    	}
	
getThread()得到looper對象所屬線程：

	public Thread getThread() { 
		return mThread; 
	}

quit()方法結束looper循環：

	public void quit() {
		// 创建一个空的message，它的target为NULL，表示结束循环消息
		Message msg = Message.obtain();
		// 发出消息
		mQueue.enqueueMessage(msg, 0);
	}

到此為止，你應該對Looper有了基本的了解，總結幾點：

1. 每個線程有且最多只能有一個Looper對象，它是一個ThreadLocal
2. Looper內部有一個消息隊列，loop()方法調用後線程開始不斷從隊列中取出消息執行
3. Looper使一個線程變成Looper線程。

那麼，我們如何往MQ上添加消息呢？下面有請Handler！（掌聲~~~）
##異步處理大師Handler
什麼是handler？handler扮演了往MQ上添加消息和處理消息的角色（只處理由自己發出的消息），即通知MQ它要執行一個任務(sendMessage)，並在loop到自己的時候執行該任務(handleMessage)，整個過程是異步的。handler創建時會關聯一個looper，默認的構造方法將關聯當前線程的looper，不過這也是可以set的。默認的構造方法：

	public class handler {
	    final MessageQueue mQueue;  // 关联的MQ
	    final Looper mLooper;  // 关联的looper
	    final Callback mCallback; 
	    // 其他属性

	    public Handler() {
		// 没看懂，直接略过，，，
		if (FIND_POTENTIAL_LEAKS) {
		    final Class<? extends Handler> klass = getClass();
		    if ((klass.isAnonymousClass() || klass.isMemberClass() || klass.isLocalClass()) &&
			    (klass.getModifiers() & Modifier.STATIC) == 0) {
			Log.w(TAG, "The following Handler class should be static or leaks might occur: " +
			    klass.getCanonicalName());
		    }
		}
		// 默认将关联当前线程的looper
		mLooper = Looper.myLooper();
		// looper不能为空，即该默认的构造方法只能在looper线程中使用
		if (mLooper == null) {
		    throw new RuntimeException(
			"Can't create handler inside thread that has not called Looper.prepare()");
		}
		// 重要！！！直接把关联looper的MQ作为自己的MQ，因此它的消息将发送到关联looper的MQ上
		mQueue = mLooper.mQueue;
		mCallback = null;
	    }

	    // 其他方法
	}

下面我們就可以為之前的LooperThread類加入Handler：

	public class LooperThread extends Thread {
	    private Handler handler1;
	    private Handler handler2;

	    @Override
	    public void run() {
		// 将当前线程初始化为Looper线程
		Looper.prepare();

		// 实例化两个handler
		handler1 = new Handler();
		handler2 = new Handler();

		// 开始循环处理消息队列
		Looper.loop();
	    }
	}

加入handler後的效果如下圖：

![show](/Handler.png)

可以看到，一個線程可以有多個Handler，但是只能有一個Looper！

###Handler發送消息
有了handler之後，我們就可以使用post(Runnable), postAtTime(Runnable, long), postDelayed(Runnable, long), sendEmptyMessage(int), sendMessage(Message), sendMessageAtTime(Message, long)和 sendMessageDelayed(Message, long)這些方法向MQ上發送消息了。光看這些API你可能會覺得handler能發兩種消息，一種是Runnable對象，一種是message對象，這是直觀的理解，但其實post發出的Runnable對象最後都被封裝成message對象了，見源碼：

	// 此方法用于向关联的MQ上发送Runnable对象，它的run方法将在handler关联的looper线程中执行
	    public final boolean post(Runnable r)
	    {
	       // 注意getPostMessage(r)将runnable封装成message
	       return  sendMessageDelayed(getPostMessage(r), 0);
	    }

	    private final Message getPostMessage(Runnable r) {
		Message m = Message.obtain();  //得到空的message
		m.callback = r;  //将runnable设为message的callback，
		return m;
	    }

	    public boolean sendMessageAtTime(Message msg, long uptimeMillis)
	    {
		boolean sent = false;
		MessageQueue queue = mQueue;
		if (queue != null) {
		    msg.target = this;  // message的target必须设为该handler！
		    sent = queue.enqueueMessage(msg, uptimeMillis);
		}
		else {
		    RuntimeException e = new RuntimeException(
			this + " sendMessageAtTime() called with no mQueue");
		    Log.w("Looper", e.getMessage(), e);
		}
		return sent;
	    }

其他方法就不羅列了，總之通過handler發出的message有如下特點：

1. message.target為該handler對象，這確保了looper執行到該message時能找到處理它的handler，即loop()方法中的關鍵代碼

	msg.target.dispatchMessage(msg);

2. post發出的message，其callback為Runnable對象

###Handler處理消息
說完了消息的發送，再來看下handler如何處理消息。消息的處理是通過核心方法dispatchMessage ( Message msg)與鉤子方法handleMessage ( Message msg)完成的，見源碼:

	// 处理消息，该方法由looper调用
	    public void dispatchMessage(Message msg) {
		if (msg.callback != null) {
		    // 如果message设置了callback，即runnable消息，处理callback！
		    handleCallback(msg);
		} else {
		    // 如果handler本身设置了callback，则执行callback
		    if (mCallback != null) {
			 /* 这种方法允许让activity等来实现Handler.Callback接口，避免了自己编写handler重写handleMessage方法。见http://alex-yang-xiansoftware-com.iteye.com/blog/850865 */
			if (mCallback.handleMessage(msg)) {
			    return;
			}
		    }
		    // 如果message没有callback，则调用handler的钩子方法handleMessage
		    handleMessage(msg);
		}
	    }

	    // 处理runnable消息
	    private final void handleCallback(Message message) {
		message.callback.run();  //直接调用run方法！
	    }
	    // 由子类实现的钩子方法
	    public void handleMessage(Message msg) {
	    }

可以看到，除了handleMessage ( Message msg)和Runnable對象的run方法由開發者實現外（實現具體邏輯），handler的內部工作機制對開發者是透明的。這正是handler API設計的精妙之處！

###Handler的用處
我在小標題中將handler描述為“異步處理大師”，這歸功於Handler擁有下面兩個重要的特點：

1. handler可以在任意線程發送消息，這些消息會被添加到關聯的MQ上。

![show](/HandlerProcess.png)

2. handler是在它關聯的looper線程中處理消息的。

![show](/HandlerProcess2.png)

這就解決了android最經典的不能在其他非主線程中更新UI的問題。android的主線程也是一個looper線程 (looper在android中運用很廣)，我們在其中創建的handler默認將關聯主線程MQ。因此，利用handler的一個solution就是在activity中創建handler並將其引用傳遞給worker thread，worker thread執行完任務後使用handler發送消息通知activity更新UI。(過程如圖)

![show](/HandlerProcess3.png)

下面給出sample代碼，僅供參考：

	public class TestDriverActivity extends Activity {
	    private TextView textview;

	    @Override
	    protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.main);
		textview = (TextView) findViewById(R.id.textview);
		// 创建并启动工作线程
		Thread workerThread = new Thread(new SampleTask(new MyHandler()));
		workerThread.start();
	    }

	    public void appendText(String msg) {
		textview.setText(textview.getText() + "\n" + msg);
	    }

	    class MyHandler extends Handler {
		@Override
		public void handleMessage(Message msg) {
		    String result = msg.getData().getString("message");
		    // 更新UI
		    appendText(result);
		}
	    }
	}

	public class SampleTask implements Runnable {
	    private static final String TAG = SampleTask.class.getSimpleName();
	    Handler handler;

	    public SampleTask(Handler handler) {
		super();
		this.handler = handler;
	    }

	    @Override
	    public void run() {
		try {  // 模拟执行某项任务，下载等
		    Thread.sleep(5000);
		    // 任务完成后通知activity更新UI
		    Message msg = prepareMessage("task completed!");
		    // message将被添加到主线程的MQ中
		    handler.sendMessage(msg);
		} catch (InterruptedException e) {
		    Log.d(TAG, "interrupted!");
		}

	    }

	    private Message prepareMessage(String str) {
		Message result = handler.obtainMessage();
		Bundle data = new Bundle();
		data.putString("message", str);
		result.setData(data);
		return result;
	    }

	}

當然，handler能做的遠遠不僅如此，由於它能post Runnable對象，它還能與Looper配合實現經典的Pipeline Thread(流水線線程)模式。請參考此文[Android Guts: Intro to Loopers and Handlers](http://mindtherobot.com/blog/159/android-guts-intro-to-loopers-and-handlers/)

##封裝任務Message
在整個消息處理機制中，message又叫task，封裝了任務攜帶的信息和處理該任務的handler。message的用法比較簡單，這裡不做總結了。但是有這麼幾點需要注意（待補充）：

1. 儘管Message有public的默認構造方法，但是你應該通過Message.obtain()來從消息池中獲得空消息對象，以節省資源。
2. 如果你的message只需要攜帶簡單的int信息，請優先使用Message.arg1和Message.arg2來傳遞信息，這比用Bundle更省內存
3. 擅用message.what來標識信息，以便用不同方式處理message。

最後補上我自己畫的架構圖(建議下載來看會比較好):

![show](/Android的Handler、Looper、thread、MessageQueue架構圖.jpg)

###Reference:
[http://www.cnblogs.com/codingmyworld/archive/2011/09/12/2174255.html](http://www.cnblogs.com/codingmyworld/archive/2011/09/12/2174255.html)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node21:Android AsyncTask 與 Handler Thread 的差異
------------------------------------------------
在note18中有提到費時的工作得外使用新的 Thread 來處理，如果這費時的工作處理過程或結果不用與 UI 互動，那麼只要起一個一般的 Thread 即可，但是多半不會這樣，所以就出現了 AsyncTask 與 Handler Thread。之所以會一起比較 AyncTask 與 Handler Thread 的原因就在於他們提供相同的功能，即另使用新的 Thread 進行費時的工作，且可以透過 Main Thread 修改 UI。
>先講結論，基於易用與可靠性，Android 建議使用 AsyncTask。
AsyncTask 出現的目的就是在提供簡單易用的方式達成一些的功能，不像 Handler Thread 得與 Handler、Thread 與 Message Queue 搏鬥，AsyncTask 只要定義幾個 Callback 就可以上路了。
>AsyncTask 內部實做機制為較新且較強的 java.util.concurrent，但較佔資源，而 Handler Thread 則為基本的 Java Thread。

由於 Handler Thread 依靠 Message Queue 與 Main Thread 互動，相對於 AsyncTask，Handler Thread 比較可能發生塞車情況。但 Handler Thread 在即時互動上優於 AsyncTask，因為 Main Thread 可以隨時傳送 Message 給 Handler Thread，而 AsyncTask 不行，只能依照事先定義 Callback 進行。基於輕量環境資源的有限，當執行單一的工作時建議使用 AsyncTask，如下載一個大檔案，但是當執行大量重複性的工作時，建議使用 Handler Thread，如下載多個小圖。
###Reference:
[http://cw1057.blogspot.tw/2011/12/android-asynctask-handler-thread.html](http://cw1057.blogspot.tw/2011/12/android-asynctask-handler-thread.html)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)

node22:Android Socket教學與程式範例
---------------------------------
這次寫這篇筆記的原因不是因為我遇到了問題，純粹是因為最近知道了SOCKET這個技術，然後發現它非常的重要，重要到每個語言一定都支援，而且身在這網路時代一定要會的東西。以下開始說明八~
###1.摘要:
現在要用程式撰寫網路傳輸功能，普遍有兩種方式，第一種是使用Socket，也是現在要介紹的技術，第二種是使用Http，在我的note12:使用Android POST and GET Request using HttpURLConnection中已經有講解Android的撰寫方式了，有興趣的可以去看看；基本上按照網路上的說法，Socket是最早期的網路傳輸的技術，最基本支援兩種服務，一種是連接的TCP應用服務,另一種是無連接的UDP應用服務，若不知道TCP、UDP是甚麼可以上網查一下。在HTTP中使用的是請求回應方式,表示當APP發出請求時建立連結通道,當客戶端向伺服器發送完請求,伺服器端才能向客戶端返回資料；而在Socket的TCP/IP連線方式是雙方建立連結後可以直接進行資料的雙向傳輸,就不需要每次由客戶端向伺服器發送請求~所以Socket最適合用在比如聊天室功能，只需一次連線，之後就可以一直更新，直到斷線為止。當然Socket一定也支援其他的傳輸方式，等我更深入了解再寫筆記八。另外其實與note18:Android 中的 Thread 也很有關係，因為就像note18一開始所介紹的，Android不允許在Main Thread中有複雜的運算，所以只要牽涉到複雜的運算比如網路連線、資料庫處理等，皆要用新的thread來實作，這回要介紹的socket也不例外。

###2.Socket基本介紹:(Server)
以下我會用實際例子邊舉例邊解釋socket用法。
首先是server端，這次的實作server端是採用純java語言撰寫，基本上也不會用Android當server，除非是點對點連線(類似Ad-hoc那種)，先來講解架構，簡單來說架構如以下那張圖:

![know](/thread架構.png)

我們在main thread中串建一個新的thread ServerListener，此thread的功用就是建立一台server，並用一個無限迴圈不端監聽port，看看是否有人連進來，若有則做出相對映的動作。

	main.java
	public class main{
		public static void main(String args[]){
			new ServerListener().start();   //串建一個新的ServerListener Thread，並開始執行(參考node18的解說)
		}
	}

	ServerListener.java
	public class ServerListener extends Thread{  //ServerListener繼承自thread，這樣可以直接將此class當作thread來創建
		@Override
		public void run(){		//複寫thread中的run方法，用來指定thread要做的事情
			try{
				ServerSocket serverSocket=new ServerSocket(12345);
				//串建一個serversocket，在後面我們介紹clientSocket時你會發現
				//和serverSocket不同，serverSocket通常是不指定IP的，因為本身就是server
				//，只需指定port，而clientSocket就需指定IP和port。
				while(true){ 		//設定一個無限迴圈，讓server可以不斷的監聽port有無收到請求
					Socket socket=serverSocket.accept(); //利用accept()方法來接收要求，若沒有接收到要求，會一直停在這裡，直到收到要求才往下執行
					//當serverSocket.accept收到一個請求時，會回傳一個新的socket物件，所以用一個Socket物件去接收，然後
					//為這個請求(client)串建一個新的thread(ChatSocket)，並把這個socket傳給此thread，可以把這個socket當作
					//是發出此請求的client的身分識別，因為每遇到一個新的請求，皆會回傳一個socket，不會重複
					new ChatSocket(socket).start(); //ChatSocket開始執行
				}
				
			}catch(IOException e){
				e.printStackTrace();
			}
		}
	}

	ChatSocket.java
	public class ChatSocket extends Thread{ //繼承自thread
		Socket socket;
		public ChatSocket(Socket s){	//將ServerListener thread丟進來的socket接過來
			this.socket=s;
		}
		public void out(String out){    //回應client用
			try{
				socket.getOutputStream().write(out.getBytes("UTF-8")); 
				//利用socket的getOutputStream功能可以取得回覆client的管道，使用write將訊息放入管道
				//中回傳給client，將string轉為utf-8格式
			}catch(IOException e){
				Logger.getLogger(ChatSocket.class.getName()).log(level.SERVERE,null,ex);
			}
		}
		public void run(){
			try{
				int count=0;
				while(true){
					count++;
					out(count+" ");  //設定一個無線迴圈，並設定每1秒回復一次client
					sleep(1000);
				}
			}catch (InterruptedException ex){
				Logger.getLogger(ChatSocket.class.getName()).log(level.SERVERE,null,ex);
			}
		}
		
	}
	
	

###2.Socket基本介紹:(client)(TCP)

可以先參考以下圖片:

![know](/SocketTCP.jpg)

	1.Socket socket = new Socket("192.168.3.119",7628);//創建Socket實例，並綁定連接遠端IP位址和埠
	2.OutputStream ops = socket.getOutputStream();   //定義一個輸出流，來自于Socket輸出流
	3.byte[] bytes = b.getBytes();
	  ops.write(bytes);				 //向輸出流中寫入資料
	4.ops.flush();                                   //刷行輸出流
	//================接下來是接收伺服器發送過來的資料===============================
	5.InputStream ips = socket.getInputStream();	 //定義輸入流，來自于socket的輸入流
	6.byte[] bytes2 = new byte[20];
	  ips.read(bytes2);				 //讀取輸入流資料
	7.String str = new String(bytes2);		 //轉換成字串
	8.socket.close();	
	//================這樣Android上Tcp的Socket就完成了，很簡單======================

###3.Socket基本介紹:(client)(UCP)


[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)
	

node23:WebSocket概觀與Android WebSocket實現
------------------------------------------
WebSocket一種在單個 TCP 連線上進行全雙工通訊的協定。WebSocket通訊協定於2011年被IETF定為標準(RFC 6455)<----記一下!等等AndroidCode會提到，並被RFC7936所補充規範，WebSocketAPI被W3C定為標準。WebSocket 是獨立的、建立在 TCP 上的協定，和 HTTP 的唯一關聯是使用 HTTP 協定的101狀態碼進行協定切換，使用的 TCP 埠是80，可以用於繞過大多數防火牆的限制。WebSocket 使得用戶端和伺服器之間的資料交換變得更加簡單，允許伺服端直接向用戶端推播資料而不需要用戶端進行請求，在 WebSocket API 中，瀏覽器和伺服器只需要完成一次交握，兩者之間就直接可以建立永續性的連線，並允許資料進行雙向傳送。

###WebSocket被創造出來的的原因:
以前很多網站為了實作推播技術，所用的技術都是輪詢(Polling)。在作業系統(Operating System)中我們知道Polling技術是指cpu每隔一段時間向周邊設備詢問是否需要提供服務。在Client-Server架構中，輪詢是在特定的的時間間隔（如每1秒），由瀏覽器對伺服器發出HTTP request，然後由伺服器返回最新的資料給用戶端的瀏覽器。這種傳統的模式帶來很明顯的缺點，即瀏覽器需要不斷的向伺服器發出請求，且HTTP request的header是非常長的，裡面包含的資料可能只是一個很小的值，這樣會占用很多的頻寬和伺服器資源。

而比較新的技術去做polling的效果是Comet，使用了AJAX。但這種技術雖然可達到雙向通訊，但依然需要發出請求，而且在Comet中，普遍採用了長連結，這也會大量消耗伺服器頻寬和資源。面對這種狀況，HTML5定義了WebSocket協定，能更好的節省伺服器資源和頻寬並達到實時通訊。

###WebSocket的優點與特性:
1. 伺服器與用戶端之間交換的封包檔頭很小，大概只有2位元組。（早期版本7.0）
2. 伺服器可以主動傳送資料給用戶端，而用戶端無須向伺服器發出請求。
3. "交握"建立後可以一直保持通訊，直到斷線為止。

在實作websocket連線過程中，需要透過瀏覽器發出websocket連線請求，然後伺服器發出回應，這個過程通常稱為「交握」（handshaking）。後期的版本大多屬於功能上的擴充，例如使用第7版的交握協議同樣也適用於第8版的交握協議。

ex:瀏覽器請求

	GET / HTTP/1.1
	Upgrade: websocket
	Connection: Upgrade
	Host: example.com
	Origin: null
	Sec-WebSocket-Key: sN9cRrP/n9NdMgdcy2VJFQ==
	Sec-WebSocket-Version: 13
	
ex:伺服器回應

	HTTP/1.1 101 Switching Protocols
	Upgrade: websocket
	Connection: Upgrade
	Sec-WebSocket-Accept: fFBooB7FAkLlXgRSz0BT3v4hq5s=
	Sec-WebSocket-Origin: null
	Sec-WebSocket-Location: ws://example.com/
	
在請求中的「Sec-WebSocket-Key」是隨機的，伺服器端會用這些資料來構造出一個SHA-1的資訊摘要。把「Sec-WebSocket-Key」加上一個魔幻字串「258EAFA5-E914-47DA-95CA-C5AB0DC85B11」。使用SHA-1加密，之後進行BASE-64編碼，將結果做為「Sec-WebSocket-Accept」頭的值，返回給用戶端。

>所有最新的瀏覽器支援最新規範（RFC 6455）的WebSocket協定。一個詳細的測試報告列出了這些瀏覽器支援的Websocket版本。

###Android中的WebSocket概觀
由上敘可知，顧名思義，websocket也是socket，用來通信的，只是用在web上，所以叫websocket。 websocket是html5規範中的一項，在chrome等主流瀏覽器中都已經支持。但是在我們android的原生瀏覽器卻……他x的不支援，而android中的webview也是用的原生瀏覽器的核心，所以同樣悲劇。

Android內建瀏覽器不支援WebSocket Client端，導致使用 HTML5 開發的App(PhoneGap)無法使用WebSocket與Server建立連線。主要的問題在於 WebView 元件沒有實作 WebSocket 協定。Android SDK + PhoneGap 所製作 HTML5 App 是將WebView封裝至APK裡，所以 WebSocket 無法正常工作是正常的。不過這個問題也沒有那麼難解決，在等待 WebView 加入 WebSocket 以及更多 HTML5 功能前，我們只能暫時自行實作。還好，現在有很多 Open source 的 WebSocket 程式庫可供使用。


###Android的WebScoket應用實作
據我所知，目前大部分簡單的android應用很少會需要用到websocket，這可能也是導致官方初期沒有重視、沒有將其納入基本函式庫的原因，而目前我在網路上研究了一下，通常遇到android不支援webSocket問題的人，是希望將WebSocket實作在下列兩種製作Android APP方式的情形:

####1.使用HTML5製作Android APP:
沒錯!你沒看錯，就是使用html5實作，現在想要學APP程式，只要用 HTML5 就能夠在 Android、iOS 以及 Windows Phone 上面執行了。HTML5 不是寫網頁程式嗎?是的，所以我們需要透過 Adobe PhoneGap 幫我們把 HTML5 的程式轉成可以安裝、上架的 APP。雖然 HTML5 APP 的效能會受到部份人士的質疑，畢竟它不是原生程式，但它很適合推薦給想進階學習的程式新手。另一方面，如果程式有寫好，HTML5 的效能也不會輸給原生程式。

>事實上二百年前(?)就有神人用 HTML5 寫遊戲了，例如Cut the Rope是先有HTML5網頁才有 APP~

#####使用 PhoneGap API
雖然我們寫的程式是 HTML5，但是必須透過 PhoneGap 才能轉成 APP，所以這個系列的文章會用「PhoneGap(程式)」來取代 HTML5 的字眼。因為並非所有的 HTML5 程式都能順利轉成 APP，也就是說瀏覽器能跑，不代表 APP 能執行。我們必須要撰寫 PhoneGap 看得懂的程式才行。因此僅管 PhoneGap 只算是一個軟體，我們還是會把它作程式語言稱呼。撰寫 PhoneGap 程式基本上和一般的 HTML5 沒有什麼不同，不過如果你需要使用 PhoneGap API，必須在 </head> 之前加入下面的程式碼。

	<script src="phonegap.js"></script>

那麼如果在撰寫phoneGap時遇到要使用websocket的問題時該如何解決呢?目前知道解決方式有兩種:

1. 使用WebSocket程式庫"Autobahn WebSocket"，現在，只需要自行擴充 WebView，並使用 Autobahn WebSocket 來實作 WebSocket Client 即可。Android WebView 不支援 WebSocket 的問題解決了。在此提供一份簡單的程式碼實作：[android-browser-websocket](https://github.com/Chao-wei-chu/android-browser-websocket)。

2. 在websocket出現之後就有人開發了socket.io，這又是個啥呢？其實它就幹了一個事，就是封裝websocket，使得即使不支持websocket的平台在調用socket.io時也能正常通信。而且在使用socket.io時，不管支不支持websocket，都只要一份代碼就可以。有了socket.io，我們就可以在android環境的webview當中使用socket通信了。但是，android並不支持websocket啊，socket.io到底是怎麼實現的socket通信呢？原來socket.io會在平台不支持websocket的情況下使用其他的方式實現，比如：xhr、flashsocket。在android中，socket.io實現使用的就是xhr方式。xhr是實現了通信，但是與websocket相比，xhr的實現方式性能上還是不能比。那麼有沒有方式讓android也實現真正的websocket呢？有，有人就想出了迂回的辦法：利用webview與頁面可以相會調用的特性，采用JAVA NIO將websocket實現了一遍，這下可就是貨真價實的socket了！

其實已經有人實現了這種方式，而且只需要導入一些插件及修改極少的代碼即可采用socket.io的代碼在android的webview中實現websocket。[android-websockets](https://github.com/Chao-wei-chu/android-websockets)

####2.使用AndroidStudio正統方式實作APP:

到目前為止我個人認為Android比較好用的WebSocketClient有：autobahn、AndroidAsync、Java-WebSocket。好不好用其實需要看實際需求而定，此筆記舉例選擇Java-WebSocket。

#####一、Android客戶端的創建（使用Java-WebSocket庫）：
1.其實只需要掌握一個類，WebSocketClient即可

![show](/pic1.png)

2.指定IP/域名和端口連接服務器，當服務器端有通知時會回調onMessage方法

![show](/pic2.png)

3.然後調用connect方法進行連接

![show](/pic3.png)

4.連接後就可以發送消息了，發送消息也很簡單，除了支持String的發送還支持byte發送，好了，客戶端就這麼愉快的寫完了（詳細代碼見後面打包的demo）。

![show](/pic4.png)

#####二、服務端的創建(JavaCode)：

1-1. Java Application服務端創建（使用Java-WebSocket庫），其實也很簡單，就繼承一個類WebSocketServer。

1-2. 然後在main方法中開啟服務端，現在就可以用Android客戶端來連接進行聊天、接收推送了，實在是太簡單了。

2-1. Java Web（tomcat）服務端創建，這裡不使用Java-WebSocket庫，直接使用Java API javax.websocket包中的WebSocket相關類（注意Java API只實現了標準的RFC 6455（JSR256），如果你非要選擇其它早期草案則需要用Java-WebSocket來實現，在Java-WebSocket中連接協議"Draft_17"就是標準的RFC 6455（JSR256），另外要使用Java API javax.websocket包中的WebSocket相關類要求JDK7及以上,Tomcat 7.0.49及以上）：

2-2. 然後啟動tomcat就可以愉快的用Android客戶端來連接進行聊天、接收推送了。

程式碼範例:

	public class WebSocketserver extends WebSocketServer { //繼承WebSocketServer
	
		public WebSocketserver(int port) throws UnknownHostException {
			super(new InetSocketAddress(port));
		} //設定constructor(讀取port)

		public WebSocketserver(InetSocketAddress address) {
			super(address);
		} //設定constructor(讀取位置)，server的IP位置是自動取得，不需設定

	       //以下必須覆寫四種方法:onOpen、onClose、onMessage、onError
		@Override
		public void onOpen(WebSocket client, ClientHandshake handshake) {  

			//sendToAll(client.getRemoteSocketAddress().getAddress().getHostAddress()+ " 进入房间 ！");

			System.out.println(client.getRemoteSocketAddress().getAddress() //client.getRemoteSocketAddress().getAddress().getHostAddress()在取得用戶端IP
					.getHostAddress()
					+ " 进入房间 ！");
		} //當有client連進來時觸發此函式，client變數負責識別用戶端，handshake負責記錄握手狀態，連線是自動建立的

		@Override
		public void onClose(WebSocket client, int code, String reason, boolean remote) {

			//sendToAll(client.getRemoteSocketAddress().getAddress().getHostAddress()+ " 离开房间 ！");

			System.out.println(client.getRemoteSocketAddress().getAddress()
					.getHostAddress()
					+ " 离开房间 ！");
		}//當有client斷線時觸發此函式，client變數負責識別用戶端，code紀錄狀態代碼，reason紀錄狀態資訊，remote表示對方是否已斷線

		@Override
		public void onMessage(WebSocket client, String message) {

			//sendToAll("["+ client.getRemoteSocketAddress().getAddress().getHostAddress()+ "]" + message);

			System.out.println("["
					+ client.getRemoteSocketAddress().getAddress().getHostAddress()
					+ "]" + message);
		}//當用戶端傳送訊息(String or Bytes[])過來時觸發的函式，client變數負責識別用戶端，message負責記錄傳過來的訊息

		@Override
		public void onError(WebSocket client, Exception e) {
			e.printStackTrace();
			if (client != null) {
				client.close();
			}
		}//當與用戶端的連線發生意外時觸發，先確認client變數是否有用戶端使用，再關閉用戶端連線
	}
	
在main方法中開啟服務

	// 发送给所有的聊天者
	/*
        private void sendToAll(String text) {
		Collection<WebSocket> clients = connections(); //取得目前所有的用戶端身分
		
              synchronized (clients) { //使用WebSocket內建同步函式
			for (WebSocket client : clients) { //取得所有的client，並向他們回傳訊息
				client.send(text);
			}
		}
	}
        */
	// 测试
        /*
	public static void main(String[] args) throws InterruptedException,
			IOException {

		int port = 8887; //隨機設定一個port

		WebSocketserver server = new WebSocketserver(port); //創建WebSocketServer物件，並把port丟給它
		server.start(); //WebSocketServer開始執行，在此注意，只要有新的client連進來，server會自動配對，不需像Socket還要使用accept()來接收client

		System.out.println("房间已开启，等待客户端接入，端口号: " + server.getPort());

		BufferedReader webSocketIn = new BufferedReader(new InputStreamReader(System.in)); //設定用戶端傳送訊息buffer，和Android的Socket、HttpURLConnection的BufferedReader使用方式一樣

		while (true) { //無線迴圈，不斷地在接收用戶端傳來的訊息
			String stringIn = webSocketIn.readLine(); 
			server.sendToAll(stringIn); //將傳來的訊息丟回給全部的client
		}
	}


#####三、實作成果:

![show](/Finish1.png)

![show](/Finish2.png)


###Reference:
[http://www.chengxuyuans.com/Android/97798.html](http://www.chengxuyuans.com/Android/97798.html)

[http://www.moke.tw/wordpress/computer/advanced/438](http://www.moke.tw/wordpress/computer/advanced/438)

[http://xuepiaoqiyue.blog.51cto.com/4391594/1285791](http://xuepiaoqiyue.blog.51cto.com/4391594/1285791)

[http://www.jollen.org/blog/2012/10/android-webview-websocket-howto.html](http://www.jollen.org/blog/2012/10/android-webview-websocket-howto.html)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)


node24:Android Studio 2.x版本常見問題(2016/10/14)
------------------------------------
從2016年開始，Android Studio開始正式進入2.x.x版本，隨著版本重1.x晉升到2.x，Android Studio的功能也有了重大的突破，基本上的突破功能如下列所示:

1. Instant Run: 在開發測試階段最常見的過程就是修改、執行與測試，接著再來一次同樣的過程，不斷地在修改後執行，問題是，編譯一個應用程式需要不算短的時間，少則3-5秒，多則超過一分鐘。有時，只修改了一小段程式碼，執行時卻要花費同樣長的等待時間。Instant Run以軟體解決了這個麻煩，自動判斷修改了那一類的資料，若不是變更如AndroidManifest.xml這類需要重新包裝的內容，則以即時更新模擬器內部的方式，瞬間就能在模擬器看到修改後的執行結果。
2. Cloud Test Lab: 雲端測試平台讓應用程式可以在雲端上測試結果，雲端測試平台上已提供數百種的裝置與特性配置，開發人員可依照規範與API設計測試流程與驗證條件，將應用程式與測試案例上傳雲端進行自動佈署、測試、回報，我們只需要等它執行完成後，產生測試報告。
3. 新版模擬器: 新版與前一版本的模擬器在執行上快上三倍，包括CPU、RAM與輸出入的效能都提昇了不只一個等級，使用者當然可以繼續使用如Genymotion第三方模擬器，但現在，新版模擬器已與第三方相差無幾。除此之外，也加入了新的使用者操作介面，在控制、測試如感應器(sensor)的模擬時更加方便，也可以將APK安裝檔直接拖放到模擬器中快速安裝，亦能夠更改模擬器的視窗大小等。
4. App Indexing: 使用應用程式索引能夠讓我們的應用程式更容易在Google中被搜尋到，Android Studio 2.0提供產生正確的參考網址的功能，能讓開發者將網址加在AndroidManifest.xml中，如此一來，Google應用程式索引服務就能夠找到我們的應用程式，並可直接在Android Studio中測試。
5. GPU Debugger Preview: 提供在開發OpenGL ES遊戲時一個GPU除錯器介面，讓開發人員能夠在一張張貼圖中找到問題，例如GPU的執行負荷等問題。
6. 2.2版本(2016/09)新功能1: 2.2的建置速度，比起2.1版本快了10倍，甚至模擬器也快上3倍，透過新的Instant Run功能，使用者可以直接將改變的程式碼，直接部署至運行中的程式。
7. 2.2版本(2016/09)新功能2: 測試側錄（testing recording）功能。開發者在啟動程式時，同時啟動測試側錄功能，Android Studio則會自動產生Espresso測試碼，「效果就像使用者自己撰寫一樣。」為了確保開發者的App能在各Android裝置上運作順利，測試側錄功能不僅支援本地端開發環境，同時也能在雲端環境Cloud Test Lab使用。
8. 2.2版本(2016/09)新功能3: Google重新編寫了Layout設計工具，新增約束條件Layout（Contraint Layouts），在此限制下，使用者可以在畫面中擺放元件位置。而UI在此版本也會運作更順暢，豐富的UI介面，必須要搭配巢狀Layout（nested layout），也耗費更多資源，「有了約束條件Layout，就不需要使用巢狀結構」，UI也能運作更順。

總之Android2.x帶來很多新的功能，我原本是使用Android1.x，然後想說竟然這麼神，何不更新看看，於是我就很開心得花了我一個下午更新成2.2版，更新完後我很興奮地打開project想說來體驗一下高速編譯是甚麼感覺，於是按下執行紐，AndroidStudio就非常他x的快速回覆我以下錯誤，讓我再次對2.x版本的快速震撼到:

	Unsupported method: AndroidProject.getPluginGeneration() while running project
	The version of Gradle you connect to does not support that method.
	
花惹發?這甚麼錯誤?於是上網查了一下，得知原因是因為2.2版本自動會把Instant Run開啟，而當你的專案採用舊版的gradle時，Instant Run依舊是開啟狀態，而這時已經不支持這個功能了，所有會報這個錯誤。解決方式如下:
	
	Windows & Linux:
	File -> Settings -> Build, Execution, Deployment -> Instant Run.--->all disable
	
	Mac:
	Android Studio -> Preferences -> Build, Execution, Deployment -> Instant Run.--->all disable

另外AndroidStudio2.x也有缺點，比如Instant Run雖然能大大加快編譯速度，但是它在第一次編譯的時候確實太慢了，雖然2.2比之前的版本已經快很多了，但還是比一般情況慢很多；之前我用的是gradle1.x，但是切換到2.2後編譯時出現了大量的報錯，整整幾百個錯誤讓人不寒而栗，而與其說是錯誤，不如說是警告，絕大部分還是第三方，雖然不影響正常運行程序。

###Reference:
[http://whitelife.win/2016/09/30/gradle版本切换问题/](http://whitelife.win/2016/09/30/gradle版本切换问题/)

[返回目錄](https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#目錄)



