# CityPickerWebView
省市县三级联动，WebView实现

<img src="./city.gif"/>

添加依赖
```
compile 'me.leefeng:citypicker:1.0'
```

使用方法：

onCreat()中：
```
  cityPicker = new CityPicker(MainActivity.this, this);

```
打开选择器：
```
 cityPicker.show();

```

监听方法回调：
```
@Override
 public void getCity(final String name) {
        textView.setText(name);
 }
```

处理返回键：
```
 @Override
    public void onBackPressed() {
        if (cityPicker.isShow()){
            cityPicker.close();
            return;
        }
        super.onBackPressed();
    }
```

 参考文献：<a href="https://github.com/dcloudio/mui/">mui</a>