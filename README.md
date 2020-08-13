# yunUI
### 致力于“微信小程序”原生组件扩展组件开发 —— 功能更强大，使用更方便。

## 现在有
- 扩展微信小程序原生日期组件【picker】，使选择时间可精确到分、秒

## 如何使用

(components中是组件 pages里是相关使用实例)

调用时需要先在对应文件夹的```.json```文件里的**usingComponents**字段添加ypicker组件路径，如：
```
"usingComponents": {
    "y-picker":"../../components/yPicker/ypicker"
 }
```

**其余组件亦是如此！**

然后即可在wxml中调用：
```
<y-picker></y-picker>
```
并传参！

## 参数说明
### yPicker（日期扩展组件）
- open：true / false —— 是否启用已定义的颜色、字体大小 —— 必选
- size：left / center / right —— 自定义组件展示位置（默认为right） —— 可选
- color：颜色值（支持rgb、rgba、十六进制） —— 自定义选中日期后的文字颜色 —— 必选
- seo：true / false —— 是否支持“精确到秒” —— 不填或默认为false：精确到“分钟”（如果只精确到日，则用小程序自带picker即可。**本组件为微信小程序扩展组件！**）
- holder：颜色值（支持rgb、rgba、十六进制） —— 自定义默认展示文字的颜色 ）—— 可选
- bind:bindMultiPickerChange：接收组件传回的事件名 —— 在其中可直接取到“字符串”形式的选中日期，便于后续操作


## 展示实例
### yPicker
```
<y-picker open="true" size="right" color="#888888" seo="true" holder="#888888" bind:bindMultiPickerChange="bindMultiPickerChange"></y-picker>
```