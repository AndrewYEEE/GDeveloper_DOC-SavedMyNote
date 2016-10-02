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
	<h5>Note19:Android AsyncTask 與 Handler Thread 的差異(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node19android-asynctask-與-handler-thread-的差異)</h5>
	<h5>Note20:Android Socket教學與程式範例(https://github.com/Chao-wei-chu/GDeveloper_DOC-SavedMyNote/blob/master/My_android_note.md#node20android-socket教學與程式範例)</h5>
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

node9:Error inflating class android.support.design.widget.NavigationView問題
----------------------------------------------------------------------------

此問題通常發生在使用DrawerBar等特殊主題套件，解法:
	
	Actually it is not the matter of the primarycolortext, upgrading or downgrading the dependencies.This problem will likely occur when the version of your appcompat library and design support library doesn't match.
	Example of matching condition
		compile 'com.android.support:appcompat-v7:23.1.1' // appcompat library
		compile 'com.android.support:design:23.1.1' //design support library

意思是指請更新library :)

node10:map fragment 之意外:android.view.InflateException: Binary XML file line
------------------------------------------------------------------------------

自從Android改版後，所有使用到Map的程式皆要在AndroidManifest.xml中的<application>加入:

		<meta-data android:name="com.google.android.geo.API_KEY" android:value="your Key"/>
		
不再只需要:

		<meta-data android:name="com.google.android.maps.v2.API_KEY" android:value="your Key"/>
		
若不加會一直出錯。

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


node18:Android 中的 Thread 與傳遞資料的方式
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

node19:Android AsyncTask 與 Handler Thread 的差異
------------------------------------------------
在note18中有提到費時的工作得外使用新的 Thread 來處理，如果這費時的工作處理過程或結果不用與 UI 互動，那麼只要起一個一般的 Thread 即可，但是多半不會這樣，所以就出現了 AsyncTask 與 Handler Thread。之所以會一起比較 AyncTask 與 Handler Thread 的原因就在於他們提供相同的功能，即另使用新的 Thread 進行費時的工作，且可以透過 Main Thread 修改 UI。
>先講結論，基於易用與可靠性，Android 建議使用 AsyncTask。
AsyncTask 出現的目的就是在提供簡單易用的方式達成一些的功能，不像 Handler Thread 得與 Handler、Thread 與 Message Queue 搏鬥，AsyncTask 只要定義幾個 Callback 就可以上路了。
>AsyncTask 內部實做機制為較新且較強的 java.util.concurrent，但較佔資源，而 Handler Thread 則為基本的 Java Thread。

由於 Handler Thread 依靠 Message Queue 與 Main Thread 互動，相對於 AsyncTask，Handler Thread 比較可能發生塞車情況。但 Handler Thread 在即時互動上優於 AsyncTask，因為 Main Thread 可以隨時傳送 Message 給 Handler Thread，而 AsyncTask 不行，只能依照事先定義 Callback 進行。基於輕量環境資源的有限，當執行單一的工作時建議使用 AsyncTask，如下載一個大檔案，但是當執行大量重複性的工作時，建議使用 Handler Thread，如下載多個小圖。



node20:Android Socket教學與程式範例
--------------------------
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

	
	


