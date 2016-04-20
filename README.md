# QueryDialog简介

---

这是一个简易插件，根据传入的参数，动态生成一个查询条件编辑框，用户编辑完查询条件之后再传到后台，对数据进行过滤。

![QueryDialog Default View](https://github.com/aphy358/QueryDialog/blob/master/ScreenShot.jpg)

## Dependencies

普通的JQuery包即可.  

- [jQuery v2.1.3 (>= 1.9.0)](http://jquery.com/)

## Getting Started


### Usage

首先是引入样式文件和js文件.

```html
<!-- Required Stylesheets -->
<link href="QueryDialog.css" rel="stylesheet">

<!-- Required Javascript -->
<script src="jquery.js"></script>
<script src="QueryDialog.js"></script>
```

插件将绑定如下样式的DOM，如果页面原本没有，则插件将在页面自动生成这个DOM.

```html
<div id="QueryDialog"></div>
```

基本用法如下.

```javascript
$(document).ready(function () {
    var arrStr = '[{"queryfieldtype":"1","queryfieldname":"age","queryfieldrmk":"年龄"},{"queryfieldtype":"6","queryfieldname":"name","queryfieldrmk":"姓名"},{"queryfieldtype":"5","queryfieldname":"ismarried","queryfieldrmk":"是否已婚"},{"queryfieldtype":"4","queryfieldname":"birthday","queryfieldrmk":"出生日期"}]';
    $("#QueryDialog").QueryDialog({ data: arrStr });
});

function test() {
    $("#QueryDialog").show();
    $(".qdialog-mask").show();
}
```

## Data Structure

参数是一个字符串，结构示例：

```javascript
var arrStr = '[{"queryfieldtype":"1","queryfieldname":"age","queryfieldrmk":"年龄"},{"queryfieldtype":"6","queryfieldname":"name","queryfieldrmk":"姓名"},{"queryfieldtype":"5","queryfieldname":"ismarried","queryfieldrmk":"是否已婚"},{"queryfieldtype":"4","queryfieldname":"birthday","queryfieldrmk":"出生日期"}]';

//参数arrStr是一个数组的字符串，插件会将它转成json格式，并进一步处理；
//每一个参数单体结构：{"queryfieldtype":"1","queryfieldname":"age","queryfieldrmk":"年龄"}；
//1、queryfieldtype表示查询条件的参数类型，如“整数”、“字符型”、“日期型”等，这里“1”代表的是“浮点型数字”，当然也可以根据实际情况另外约定；
//2、queryfieldname表示查询条件的字段名称，是要对哪个字段进行过滤；
//3、queryfieldrmk表示查询条件字段的显示名称；
```
