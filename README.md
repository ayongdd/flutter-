# Flutter笔记

## 如何在Column中嵌入横着滚动的ListView      https://www.bilibili.com/video/BV1PT41177rs/?spm_id_from=autoNext&vd_source=61596f2e8aeaf8e4e3087056bd6404c4

## flutter key: 
 #### 局部键（Local Key）:ValueKey(dynamic) ObjectKey(dynamic) UniqueKey()    
 #### 全局键（Global key）: GlobalKey()
 ![image](https://user-images.githubusercontent.com/84298308/218069123-b6667a93-d0df-483f-b8b3-64a25c1ceaef.png)

 
 ## 可拖拽Widget:      
 #### ReorderableListView() 
 #### Draggable() 

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

 
 ## 交错动画 
 #### 通过 <strong>.chain(CurveTween(curve:Interval(0.1,0.2)))</strong>  控制动画触发和结束时间形成交错动画
 ![image](https://user-images.githubusercontent.com/84298308/217506463-8c272d04-06c3-442a-9827-9b0866691738.png)


## Transform:位移widget (Transform.scale 、 Transform.rotate、Transform.translate )     
 ![image](https://user-images.githubusercontent.com/84298308/215262368-d9298fc4-81d1-4a3d-ac5f-b86299ae83d9.png)
 
 
 ### double取整: 2.31 ~/1 输出:2       
 #### int转double  value.toDouble()   double转int value.toInt()
 
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

