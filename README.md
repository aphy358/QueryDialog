# QueryDialog简介

---

这是一个简易插件，根据传入的参数，动态生成一个查询条件编辑框，用户编辑完查询条件之后再传到后台，对数据进行过滤。

## Dependencies

普通的JQuery包即可.  

- [jQuery v2.1.3 (>= 1.9.0)](http://jquery.com/)

## Getting Started

[下载](https://github.com/aphy358/QueryDialog/archive/master.zip)

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
```