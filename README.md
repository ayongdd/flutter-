# Flutter笔记

## 如何在Column中嵌入横着滚动的ListView      https://www.bilibili.com/video/BV1PT41177rs/?spm_id_from=autoNext&vd_source=61596f2e8aeaf8e4e3087056bd6404c4

## flutter key: 
 #### 局部键（Local Key）:ValueKey(dynamic) ObjectKey(dynamic) UniqueKey()    
 #### 全局键（Global key）: GlobalKey() 可以获取组件信息，也可以全局组件context
 ![image](https://user-images.githubusercontent.com/84298308/218069123-b6667a93-d0df-483f-b8b3-64a25c1ceaef.png)
 ![image](https://user-images.githubusercontent.com/84298308/231687587-955fcce2-1485-4c94-b7f5-0a9d7419cef7.png)



 
 ## 可拖拽Widget:      
 #### ReorderableListView() 
 #### Draggable()
 
 ## 模型约束：BoxConstraints
 ## UnconstrainedBox():取消父级盒子宽高约束，且大小不能超过父组件约束，否则报错,
 其它约束组件 比如AspectRatio，它可以指定子组件的长宽比、LimitedBox 用于指定最大宽高、FractionallySizedBox 可以根据父容器宽高的百分比来设置子组件宽高等

##  shuffle() ：随机打乱列表数据     
List<String> countries = ["USA", "United Kingdom","China", "Russia", "Brazil"];
countries.shuffle();
print(countries); 
// [United Kingdom, Brazil, Russia, China, USA]
 
## Listener():监听 widget
 ![image](https://user-images.githubusercontent.com/84298308/215252827-c25c9b61-9e78-44c2-a589-e7f29808a2f6.png)
 
## Colors:颜色 
 #### Colors.primaries:获取内置颜色库
 #### 获取随机颜色: Colors.primaries[Random().nextInt(Colors.primaries.length)]
 #### Colors.computeLuminance():获取颜色亮度（double 类型）
 
## Matrix4:flutter内置4D矩阵插件，通过它可以实现各种特效
 ![image](https://user-images.githubusercontent.com/84298308/220535733-d91bfbd9-c14d-486a-a4d3-c2125b62052a.png)

 
 
## 显式动画 Animated
 #### AnimatedContainer()
 #### AnimatedSwitcher()
 #### AnimatedPadding()
 #### TweenAnimationBuilder()
 ![image](https://user-images.githubusercontent.com/84298308/215262086-24dfec05-506d-40f7-a0ae-4274e75d7e89.png)     
 #### AnimatedCrossFade
 ![image](https://user-images.githubusercontent.com/84298308/220030431-d2c344f1-3252-4bef-a572-0129c2e1cc54.png)


 
## 隐式动画 Transition     
 #### RotationTransition():旋转动画
 #### FadeTransition():透明度动画
 #### ScaleTransition():缩放动画
 #### SliderTransition():上下左右移动动画

![image](https://user-images.githubusercontent.com/84298308/217500388-eb17a0f6-b3d5-455e-84ad-b48727a8f575.png)
![image](https://user-images.githubusercontent.com/84298308/220536919-f08e1134-e5e8-432b-a48b-53e76182438f.png)

 
 ## 交错动画 
 #### 通过 <strong>.chain(CurveTween(curve:Interval(0.1,0.2)))</strong>  控制动画触发和结束时间形成交错动画
 ![image](https://user-images.githubusercontent.com/84298308/217506463-8c272d04-06c3-442a-9827-9b0866691738.png)


## Transform:位移widget (Transform.scale 、 Transform.rotate、Transform.translate )     
 ![image](https://user-images.githubusercontent.com/84298308/215262368-d9298fc4-81d1-4a3d-ac5f-b86299ae83d9.png)
 
 
 ### double取整: 2.31 ~/1 输出:2       
 #### int转double  value.toDouble()   double转int value.toInt()

 ### 生成随机bool值 Random.secure().nextBool()
 
 ## 自定义动画
 ![image](https://user-images.githubusercontent.com/84298308/217518969-bd9abb7e-cff3-464f-bde8-2089a3e65873.png)

 ## Hero动画
 ### 页面穿梭动画 https://www.bilibili.com/video/BV1cC4y1a7u6/?spm_id_from=333.788&vd_source=61596f2e8aeaf8e4e3087056bd6404c4
 
 
## Container 渐变
 ![image](https://user-images.githubusercontent.com/84298308/217794285-e5afcf86-7126-4591-8348-0d452c4d4857.png)


## 滑动删除控件 Dismissible
 ![image](https://user-images.githubusercontent.com/84298308/218246438-e9288433-dcee-4496-8dfb-a1ee6b7cd2f7.png)

## 旋转控件（将子控件旋转） RotatedBox() 
 ![image](https://user-images.githubusercontent.com/84298308/218247874-3f3d7726-0099-4ba5-8b83-858bffd791ea.png)
 
 ## 类似ios选择日期的 滚动控件 ListWheelScrollView()
 ![image](https://user-images.githubusercontent.com/84298308/218247976-bbcf3bc4-de69-4175-b83a-fc0011c1e043.png)

 ## FutureBuidler
![image](https://user-images.githubusercontent.com/84298308/218671808-f7b8712e-f44d-407b-aa49-146725ad6918.png)

## StreamBuilder 
 ![image](https://user-images.githubusercontent.com/84298308/218940685-07bc4d01-cab7-45a8-aeb2-84919ce8dd15.png)
 ![image](https://user-images.githubusercontent.com/84298308/218940529-27dad09d-c664-4d49-b85f-40d9b36bc572.png)

## customMultiChild (用途：文字加下划线)
 ![image](https://user-images.githubusercontent.com/84298308/219273228-daa4c1ed-4ef4-4ce1-b098-2e50ccd8b182.png)
 ![image](https://user-images.githubusercontent.com/84298308/219273152-62200b7d-26ba-4cda-a7b5-d275d6c5ca76.png)
 
 ## customScrollView :列表控件（数据不多用SliverToBoxAdapter,数据多用 SliverGrid、SliverList）
 ![image](https://user-images.githubusercontent.com/84298308/219553206-86c03db4-d322-4b5f-a42b-8cd1a1e6ec3b.png)

 ## SliverAppBar (弹性AppBar，可替换AppBar)
 ![image](https://user-images.githubusercontent.com/84298308/219559022-8a5081b9-7e0a-4b6e-961a-69c3890aeedb.png)

## 裁切头像
 ![image](https://user-images.githubusercontent.com/84298308/219567038-04e1d375-398e-42f2-9eb8-cc84f1f65f7e.png)
 
 ## SliverPersistentHeader : sliver 吸附效果 用于多用于好友分组
 ![image](https://user-images.githubusercontent.com/84298308/219571773-7247efa1-1e4e-4d07-b3db-5168494517d8.png)

 ## 根据手机横屏竖屏 设置排列方向
 ![image](https://user-images.githubusercontent.com/84298308/219596224-51a12f84-7e3c-417b-bd3a-23f70988b39f.png)
 
 ## 插件
 
 #### flutter_rating_bar: 评分插件
 ![image](https://user-images.githubusercontent.com/84298308/233781242-48d00058-d2f6-4097-90d8-0fc3de9782f6.png)
 
#### flutter_slidable: 可滑动列表项的 Flutter 实现。
 ![image](https://user-images.githubusercontent.com/84298308/233782794-9de8257b-2803-4179-bd69-6c02c8ccbed5.png)

#### hive: 是一个纯 Dart 编写的、基于文件存储的、轻量且功能强大的 Key-Value 型数据库。使用 AES-256 进行高度加密。
 https://www.jianshu.com/p/ae5b93d9a490
 
 #### flutter_screenutil: flutter屏幕适合配置方案，利用调整整屏和字体大小的flutter插件，让你的UI在不同尺寸的屏幕上都能显示合理的布局！

### dart 读取json文件
![image](https://github.com/ayongdd/flutter-/assets/84298308/540cd303-a463-4cc1-acab-2b69ad8112d6)

### 下拉刷新list
pull_to_refresh

### getX 
#### Get.isRegistered<Tab_missionLogic>() getx检测是否注册Tab_missionLogic

### 打包web本地访问 python3 -m http.server 8080
### --web-renderer=html --web-port=8686 --web-hostname=192.168.4.35

### _notifyUI函数是一个回调函数，它负责在数据发生变化时调用setState()来触发UI更新。通过将setState()方法作为回调函数传递给_notifyUI，可以确保在更新数据后，Flutter框架会调用setState()来重新构建UI。
![image](https://github.com/ayongdd/flutter-/assets/84298308/c8b8d2e0-fb97-40f8-bca8-5345c8ff9a7f)


### WidgetsBinding.instance.addPostFrameCallback((_) {
  // 在UI渲染完成后执行的回调函数
  // 可以在这里执行一些需要等待UI构建完成的逻辑
  // 例如测量组件尺寸、执行动画等
});

### ![image](https://github.com/ayongdd/flutter-/assets/84298308/ead4ea54-6feb-469f-b9de-1fbaedba8410)

### ![image](https://github.com/ayongdd/flutter-/assets/84298308/1d435a82-b8d5-4b39-ab27-036c206b1fbb)
.cast<String>()方法将列表中的元素转换为字符串类型。

###   final cardData = <WBMyCardModel>[].obs  列表响应式声明

### 创建了一个BankListRefreshNotify对象，并使用.listen()方法来订阅linster事件流。当事件流中有新事件时，会执行传递给.listen()方法的回调函数
![image](https://github.com/ayongdd/flutter-/assets/84298308/5d505abf-868a-4c27-980e-6170dcf04cd7)
![image](https://github.com/ayongdd/flutter-/assets/84298308/bc8ffffc-a056-414f-bb62-42872895d2c2)

### TextFiled 正则写法
![image](https://github.com/ayongdd/flutter-/assets/84298308/f8b437a2-c854-42ce-96e5-17427403f362)


### flutter 机器人 https://poe.com/chat/239se6osl2tr4wa3wet

### flutter 键盘升起遮挡TextField 解决办法 
#### 方法1. 用flutter_keyboard_visibility插件
#### 方法2. 创建 WBKeyBoardObsercer类

import 'package:flutter/material.dart';
import 'dart:math';
import 'dart:ui';
import 'package:get/get.dart';
typedef FunctionType = void Function(double boardHeight);
class WBKeyBoardObsercer extends WidgetsBindingObserver {
  double keyboardHeight = 0;
  bool? isKeyboardShow;
  bool? _preKeyboardShow;

  ScrollController scController; // 滑动视图控制器
  double widgetHeight; //文本框高度
  FunctionType? keyBoardChange;
  WBKeyBoardObsercer({required this.scController,required this.widgetHeight});



  @override
  Future<bool> didPopRoute() {
    // TODO: implement didPopRoute
    print("routes did pop");
    return super.didPopRoute();
  }
  @override
  void didChangeMetrics() {
    debugPrint("didChangeMetrics");
    final bottom = Get.mediaQuery.viewInsets.bottom;
    // 键盘存在中间态，回调是键盘冒出来的高度
    keyboardHeight = max(keyboardHeight, bottom);
    if (bottom == 0) {

      isKeyboardShow = false;
    } else if (bottom == keyboardHeight || keyboardHeight == 0) {

      isKeyboardShow = true;
    } else {
      ///键盘打开和收起，都会走这里。

      isKeyboardShow = null;

      ///当键盘之前处于打开的时候才需要获取
      if (_preKeyboardShow == true) {
        ///从手写切换到拼音，键盘会变小，这个时候无法判断，延迟一下，如果bottom 大于200，那么就是键盘高度。

      }
    }

    ///展开和收起
    if (isKeyboardShow != null && _preKeyboardShow != isKeyboardShow) {
      double bottom = Get.mediaQuery.viewInsets.bottom;

      ///改变键盘为手写模式也会走这里，但是如果是手写改成9按键（键盘由高变小），不会走这里。



      ///收起时候保存键盘高度
      if (bottom == 0 && keyboardHeight != 0) {

      }
    }

    Future.delayed(const Duration(milliseconds: 10), () {
      final height = Get.mediaQuery.viewInsets.bottom;
      keyBoardChange?.call(height);
      if (height > 200) {

        keyboardHeight = height;


        var bottom = Get.mediaQuery.viewInsets.bottom;
        print("key board frame:${bottom}");
        var rect = Get.focusScope?.rect ?? Rect.zero;
        print("focus tf rect:${rect}");
        print("screen height:${Get.height}");
        var offset =  Get.height - bottom - (widgetHeight) - rect.top;
        print("offset aaaa :${offset}");
        if (offset < 0) {
          if (scController.offset > 0) {
            offset = offset - scController.offset;
          }
          scController.animateTo(
              -offset, duration: Duration(milliseconds: 10), curve: Curves.linear);
        }

      }
    });
    _preKeyboardShow = isKeyboardShow;
  }
}
##### 用法：
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/5d473662-a3da-4522-b02c-2c543230f867)
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/e12a8b95-5270-4b83-ba00-32fe24a7b2ee)
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/421bb975-2a37-4b67-9179-38e500beda91)
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/90aa4632-f65f-4327-8dcb-3e300193a8c5)


### flutter 下拉菜单写法
#### 利用GlobalKey 获取定位container 的尺寸大小 定位  利用showMenu组件下拉
####  final GlobalKey _widgetKey = GlobalKey();

#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/581563c4-e3fb-4003-96cf-adbe30462af9)

#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/2eda7949-0b55-42e1-a16a-cdb6c60b2ff4)

### flutter点击 阻止冒泡 GestureDetector behavior属性
####   behavior: HitTestBehavior.deferToChild, 手势事件将被传递给GestureDetector的子小部件。
####    behavior: HitTestBehavior.opaque,GestureDetector将独占手势事件，并阻止它们传递给子小部件。


### flutter_scrollview_observer 滚动观察
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/cc79c067-0d97-43d8-b234-fd60c4b18c4e)
#### 应用场景 1.获取最顶部的子部件信息（可以获取当前的第一个子部件和所有正在显示的子部件信息）  2.视频列表自动播放（当子部件进入列表中间区域时，自动播放视频） 3.模块定位（当滚动到一些特定模块时，顶部的 TabBar 的指示器切换到对应模块 tab）

 ### scroll_to_index 点击tabbar 滚动到指定的定位位置

 ### map转 list .toList()

 ### getx UI界面获取不到状态改变 可以用 change(null,status: RxStatus.success())  需要加  extends GetxController with StateMixin 混淆;

 ### common_utils Dart常用工具类库。包含日期，正则，倒计时，时间轴等工具类

 ### 读取本地图片  
 #### late ui.Image indrIcon;
 #### indrIcon = await loadImageFromAssets("assets/${curLanguage()}/home/checked2@2x.png");
 #### ![image](https://github.com/ayongdd/flutter-/assets/84298308/ac5085e4-7c49-4e82-88d6-2a369157596e)

### 获取box 相对于offset(0,0)的偏移量 
####   final GlobalKey _widgetKey = GlobalKey();
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/de7054ed-da50-4585-b6b6-e4fdf08c1650)
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/f31b04e7-26a8-46db-a754-4f5726ceb48f)

### 运行web端指令  --web-renderer=html --web-port=8686 --web-hostname=192.168.4.35
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/022cdae7-5982-43b4-b655-215e3e759315)
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/8ee2a66e-c17f-4036-97f1-6474b4d9e014)

### resizeToAvoidBottomInset 是一个布尔值属性，用于控制页面是否自动调整大小以避免底部插入（例如键盘）
#### ![image](https://github.com/ayongdd/flutter-/assets/84298308/0b309839-e2f0-4d65-a8e7-8bfe3e74a284)


