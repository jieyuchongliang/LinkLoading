## LinkLoading 转圈，加载提示框

第一步. 在Project层级的build.gradle文件中添加下文中的```maven { url 'https://jitpack.io' }```

Add it in your root build.gradle at the end of repositories:
```javascript
        allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
第二步. Add the dependency

	dependencies {
	        compile 'com.github.jieyuchongliang:LinkLoading:v1.0.0'
	}

第三步. 在需要使用的地方自己手动new一个LoadingView的对象。需要显示的时候就调用show方法，不需要显示时就调用dismiss方法隐藏。

```javascript
    LoadingView loadingView = new LoadingView(this,R.style.CustomDialog);//获取控件
    loadingView.show();//在需要显示的地方调用show方法显示
    loadingView.dismiss();//在不需要显示的时候调用dismiss方法隐藏
```
