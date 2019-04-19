# preview
## 实现浏览器得预览功能，能预览word/excel等word文件，也能预览pdf文件
使用方式<br/>

先得有个文件地址，该地址必须得能用域名的方式访问，本地路径那种不行<br/>

let **<font color="#660000">URL</font>** = "http://www.test.com/test.xlsx"
<iframe src='http://view.officeapps.live.com/op/view.aspx?src=**<font color="#660000">URL</font>**' width='100%' height='1000px' frameborder='1'>
 </iframe>
 
 上面这种方式只能预览office文件，要预览pdf文件需要一个插件[PDFObject.js](http://jhyt.oss-cn-shanghai.aliyuncs.com/images/1531367199089_PDFObject.js)
 
 基本用法<br/>
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
