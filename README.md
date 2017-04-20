












# IdentityImageView
一个能带进度条的图片框架，同时有身份标识动能，简单易用

## 效果图：
![效果图](https://github.com/385841539/IdentityImageView/blob/master/app/src/main/res/drawable/biaoshi.gif)


# 博客介绍

CSDN:[http://blog.csdn.net/iamdingruihaha/article/details/69895266](http://blog.csdn.net/iamdingruihaha/article/details/69895266)


## Download
```java
    allprojects {
	    repositories {
		    ...
		    maven { url 'https://jitpack.io' }
	    }
	}

    dependencies {
     compile 'com.github.385841539:IdentityImageView:-SNAPSHOT'
	}

```

# Usage


基本使用：


```xml
<com.example.identityimageview.widegt.IdentityImageView
        android:id="@+id/iiv"
        android:layout_width="300dp"
        android:layout_height="300dp"
        app:iciv_progress_collor="@color/colorPrimary"
        android:layout_centerVertical="true"
        android:layout_centerHorizontal="true"></com.example.identityimageview.widegt.IdentityImageView>
```


自定义(均设有默认值，可不使用)：


| 命名           	 		|    参数           	| 说明  					|
| ------------------------- |------------------ | --------------------- |
| iciv_bigimage				| reference 			|大图片|
| iciv_smallimage		| reference       	    | 小图片(标识)|
| iciv_angle				| float angle     	| 标识的角度，默认为45度|
| iciv_radiusscale			| float x |大小图片比例,默认为0.2|
| iciv_isprogress|boolean flag | 是否有进度条,默认为false,如果要用，必须设置为true|
|iciv_progress_collor|Color color Or reference|  进度条颜色|
|  iciv_border_color  |Color color Or reference|  边框颜色  |
|  iciv_border_width  |integer y| 边框和进度条宽度  |
|iciv_hint_smallimageview | boolean|  是否隐藏小图片|
```java

	CommonBehavior.from(mFloatingActionButton).show();//代码控制显示
	CommonBehavior.from(mFloatingActionButton).hide();//隐藏

	CommonBehavior.from(mFloatingActionButton)
		.setMinScrollY(20)
		.setScrollYDistance(100)
		.setDuration(1000)
		.setInterpolator(new LinearOutSlowInInterpolator());
```

## Tips

1、因为根布局为CoordinatorLayout，所以使用时Toolbar可能会遮盖RecyclerView顶部的item，BottomBar也可能会遮盖底部item。
可以参考知乎首页设置顶部留白，具体可为RecyclerView添加一个占位的ItemDecoration，或者顶部加一个占位的View，若场景比较固定可简单设置Padding，Margin等，
详情可见Demo，简单处理了这种情况。


2、FloatingActionButton的elevation若大于BottomBar的elevation，则FloatingActionButton动画覆盖在BottomBar上层，反之则在下层，为gif的下部两个按钮的效果。


## Apk and More Info

For more usage, you can download or clone the demo. You can also [download the demo apk](https://github.com/Lauzy/LBehavior/raw/master/apk/demo.apk).









