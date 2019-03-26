# activity
Android实验一
核心代码:
```java
package com.example.myapplication1;

import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.util.Log;

public class MainActivity extends AppCompatActivity {

    private final static String TAG="yyyy";
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    @Override
    protected void onStart() {
        super.onStart();
        // The activity is about to become visible.
        Log.d("TAG","OnStart");
    }
    @Override
    protected void onResume() {
        super.onResume();
        // The activity has become visible (it is now "resumed").
        Log.d("TAG","OnResume");
    }
    @Override
    protected void onPause() {
        super.onPause();
        // Another activity is taking focus (this activity is about to be "paused").
        Log.d("TAG","OnPause");
    }
    @Override
    protected void onStop() {
        super.onStop();
        // The activity is no longer visible (it is now "stopped")
        Log.d("TAG","OnStop");
    }
    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.d("TAG","OnDestroy");
    }
}
```

运行截图:![在这里插入图片描述](https://img-blog.csdnimg.cn/20190326215659311.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
结果截图:![在这里插入图片描述](https://img-blog.csdnimg.cn/20190326215935815.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dhbmdiaW5fMTAxMg==,size_16,color_FFFFFF,t_70)
