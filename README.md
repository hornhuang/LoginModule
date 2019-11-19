# EasyLogin

EasyLogin is a login module, build with ARouter. You can use it to free up your time！



It just like use a LoginActivity. So before you enjoy it please implematention Alibaba/ARouter first. 



Add this in your app/gradle

```java
// ARouter
implementation 'com.alibaba:arouter-api:1.5.0'
```



Good! And then please add my repository to your project, like this:



```java
compile('com.fishinwater:login:1.0')
```



At last, add this to project/gradle:



```java
allprojects {
    repositories {
        ...
        maven { url "https://github.com/yuanhao-1999/EasyLogin/raw/master" }
        ...
        
    }
}
```



How to use ? Just build an application in your project like: 



```java
/**
 * @author fishinwater-1999
 * @version 2019-11-19
 */
public class App extends Application {

    @Override
    public void onCreate() {
        super.onCreate();
        ARouter.init(this);
    }
}
```





Finally let's begin :

```java
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        ARouter.getInstance().build("/login/login")
                .withLong("key1", 666L)
                .withString("key3", "888")
                .navigation();
    }
}
```





Yeah! We  jump to the new LoginActivity, without coding! 





Thanks for you star.
