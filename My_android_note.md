This is my Android notes :)
=========================
Auther: Chao Wei-Chu
--------------------

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
        $(".newh3").css("margin-left",20);
        $(".newh4").css("margin-left",40);
        $(".newh5").css("margin-left",60);
        $(".newh6").css("margin-left",80);
      });
 });
</script>
<div id="category"></div>

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
    已失傳.....(code太亂了)

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

	
	
