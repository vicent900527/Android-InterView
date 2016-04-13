# Android-InterView

在github上下载了一份面试题，花了些时间做了一遍。
多媒体那块的就没做了。
原面试题地址：[https://github.com/boredream/Android-Common-Interview-Questions](https://github.com/boredream/Android-Common-Interview-Questions)


* 安卓学习途径, 寻找资料学习的博客网站  
* AndroidStudio使用, 插件使用, 通用的调试工具  
* 安卓和苹果的区别  

--------------

* 四大组件  

  > * Content Provider
  > * Service
  > * Activity
  > * BroadCast Receiver

* 五大存储方式 

  > * Shared Preference
  > * sqlite DB
  > * file
  > * 远程存储
  > * Content Provider

* Layout布局有哪几种 FrameLayout什么时候用  

  > ### 5种布局方式
  > 分别为： FrameLayout,LinearLayout,RelativeLayout,TableLayout,AbsoluteLayout
  > FrameLayout 通常在自定义组件或者自由布局时使用

* ListView的优化 

  > * 视图重用
  > * 子组件的监听只加载一次
  > * 图片异步加载
  > * 数据与UI绑定

* 点击事件设置监听的几种方式 

  > * 自定义类继承View.OnClickListener
  > * 使用匿名类
  > * Activity继承View.OnClickListener
  > * 在layout文件里使用onclick属性指定方法名 

* 安卓主线程和子线程的关系  

  > 主线程指支撑APP运行的线程，负责APP的UI绘制工作，在主线程里不能进行网络请求的操作，也尽量不要在   主线程里进行耗时的操作。
  > 子线程与主线程的通信一般是通过handler，主线程向子线程通信可以通过接口(interface)

* Activity生命周期 onStart onResume区别  

  > onStart是Activity创建后执行，重新返回时可能不会执行onStart；
  > onResume是Activity创建和重启都会走的一个方法，只要Activity出现在屏幕上，就会执行onResume

* Fragment生命周期 Activity和Fragment区别  

  > Fragment的生命周期和Activity类似
  > Fragment是在Android3.0之后出现的，是Activity的一个组成部分，一个Activity可以有多个Fragment，Fragment不能脱离Activity单独存在

* 页面之间如何传递数据, 如果传递一个对象如何处理, 如何传递集合  

  > 页面之间的数据传递可以通过Intent传值，或者使用onActivityForResult回传；
  > 如果是对象可以把对象序列化转成Serializable或者Parcelable传递
  > 集合可以转成List传递
  > 也可以通过第三方工具进行传值

* dp px sp的区别  

  > dp 与密度无关的像素单位，在不同设备上及时像素密度不一样，但dp的大小是不便的。
  > px 1px 就是1个像素点。
  > sp 跟尺寸无关的像素单位，一般处理字体的大小。

* gravity和layout_gravity的区别  

  > gravity是元素本身的内容摆放规则;
  > layout_gravity是元素相对于父元素的摆放规则

* margin和padding的区别  

  > margin是外边距
  > padding是内补白

* weight的作用  

  > 控制元素在父元素的所占大小的比例。只适用于线性布局
  
* Handler机制  

  > 由Handler MessageQueue Looper三步分组成
  > Handler负责 消息的收发，MessageQueue负责存储，Looper负责管理消息

* 什么是ANR, 如何避免  

  > Android Not Responsing
  > 安卓定义的主线程响应时长为5秒，如果5秒内没响应，则会回收APP进程
  > 耗时的工作在子线程里做。

* 显式意图和隐式意图区别,隐式意图的使用 

  > 显式意图一般用于APP内，具有明确的目标页面
  > 隐式意图一般用于APP之间的调用，只要申明意图的标志，比如打开浏览器的意图。

* 广播几种接收方式, 广播有几种类型, 区别  

* 开启Service的几种方式, 区别, Service和Activity之间如何传递数据  

  > ### 两种
  > * startService
  > * bindService
  > 传递数据：
  > 广播、Interface、Handler、bind对象

* Service中如果要start一个Activity要如何特殊处理,为什么  

  > * 隐式启动。
  > * 启动时标记Intent的NEW_TASK

* 自定义控件 

  > 简单的组合自定义控件
  > 图文混排的自定义控件，需要重写View的一些方法
  
* 常用开源框架的使用  

  > OKHttp,Volley,xUtils,EventBus

* 动画类型 

  > Tweens
  > Frame
  > Animation 

* 任务栈,页面启动方式    

  > standard,singleTask,singleTop,singleInstence
 
* Material Design / 新控件RecyclerView CardView等使用 

  > RecyclerView智能化了ListView
  > CardView即卡片View，也是智能化的View，实现某类业务很简单。

* 图片压缩和双缓存原理  

  > * Matrix
  > * 双缓存：
  > 先通过setBitmap方法将要绘制的所有的图形绘制到一个Bitmap上也就是先在内存空间完成，然后再来调用drawBitmap方法绘制出这个Bitmap，显示在屏幕上

* 多层View的onTouch事件分发  

  > GroupView->ChildView->GroupView
  >呈U形分发事件

-----------

* Android绘制原理 onMeasure onLayout onDraw作用  

  > * onMeasure View的大小计算，视图的最终大小在这里确定
  
  > * onLayout操作用于设置视图在屏幕中显示的位置
  
  > * onDraw会将前两部操作后的参数：大小和位置等，将内容绘制到屏幕
 
* 什么是MVC MVP,区别  

  > MVC 是 把软件分为三个部分：Model,View,Controller.三者相互作用
  > MVP 是把软件分为：Model, View, Presenter.Model 和View通过Presenter相互通信

* 响应式编程  

  > 一种面向数据流和变化传播的编程方式.

* 常见开源框架源码  

  > * Android 
  > * Volley
  > * LruCache
  > * xUtils
  > * VLC
* 单元测试常用框架和实际使用 场景 

  > Monkey 自动化测试

-----

#### 多媒体

* 音频的环绕声和混响等如何处理  

* 音频录制播放  

* 视频的录制和播放  

* 播放使用的常用框架  

* Android原生支持格式  

* 软解码硬解码的区别  

* 如果要做一个按住屏幕右侧滑动调整声音功能如何处理 
