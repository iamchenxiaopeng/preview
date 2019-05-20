# preview
## 实现浏览器得预览功能，能预览word/excel等word文件，也能预览pdf文件
使用方式<br/>

先得有个文件地址，该地址必须得能用**域名**的方式访问，本地路径那种不行<br/>

代码：
```javascript
<iframe src='https://view.officeapps.live.com/op/view.aspx?src=http://storage.xuetangx.com/public_assets/xuetangx/PDF/1.xls' width='100%' height='1000px' frameborder='1'>
 </iframe>
 ```
 上面这种方式只能预览office文件，要预览pdf文件使用一个标签：embed。
 
 ```javascript
 <embed class="pdfobject" :src="./a.pdf" type="application/pdf" style="overflow: auto; width: 100%; height: 1000px;" internalinstanceid="5">
 ```
 
 或者下载一个插件（这个插件好像在vue中无法使用），官网：[PDFObject](https://pdfobject.com/)，下载：[PDFObject.js](https://github.com/iamchenxiaopeng/PDFObject)
 
 基本用法
 
 ```javascript
 <script>
 
var options = {

height: "550px",

pdfOpenParams: {view: 'FitV', page: '0' },

name:"mans",

fallbackLink: "<p>您的浏览器暂不支持此pdf，请下载最新的浏览器</p>"

};

let url = './副本TJ1901083.pdf'

PDFObject.embed(url, "#example1",options);

</script>
```
