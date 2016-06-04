This is my Android notes :)
=========================

note1:
------

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
    

note2:
------

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

node5 (GPS的三種寫法)
----------------------
以下是我在學GPS時獵奇找到的三種寫法，但觀念都一樣。
第一種:
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
=====================================================================================
寫法二:
    Android初學特訓班那本教的
寫法三:
    已失傳.....(code太亂了)
-----------------------------------------------------------------------------------------------------------------------------------
node6 關於在androidView物件上顯示數字之注意事項:
一般會在android的View物件顯示文字以凸顯功能，但要顯示數字呢?一般人會想到這樣，ex:
     private int count=0;
     
     textView=(TextView)findViewById(R.id.tvCount);
     textView.setText(count);
但有經驗的人都知道，上方的作法會導致錯誤，所以要改成:

     textView=(TextView)findViewById(R.id.tvCount);
     textView.setText(String.valueOf(count));

即可。
------------------------------------------------------------------------------------------------------------------------------------
