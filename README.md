# QueryDialog���

---

����һ�����ײ�������ݴ���Ĳ�������̬����һ����ѯ�����༭���û��༭���ѯ����֮���ٴ�����̨�������ݽ��й��ˡ�

## Dependencies

��ͨ��JQuery������.  

- [jQuery v2.1.3 (>= 1.9.0)](http://jquery.com/)

## Getting Started

[����](https://github.com/aphy358/QueryDialog/archive/master.zip)

### Usage

������������ʽ�ļ���js�ļ�.

```html
<!-- Required Stylesheets -->
<link href="QueryDialog.css" rel="stylesheet">

<!-- Required Javascript -->
<script src="jquery.js"></script>
<script src="QueryDialog.js"></script>
```

�������������ʽ��DOM�����ҳ��ԭ��û�У���������ҳ���Զ��������DOM.

```html
<div id="QueryDialog"></div>
```

�����÷�����.

```javascript
$(document).ready(function () {
    var arrStr = '[{"queryfieldtype":"1","queryfieldname":"age","queryfieldrmk":"����"},{"queryfieldtype":"6","queryfieldname":"name","queryfieldrmk":"����"},{"queryfieldtype":"5","queryfieldname":"ismarried","queryfieldrmk":"�Ƿ��ѻ�"},{"queryfieldtype":"4","queryfieldname":"birthday","queryfieldrmk":"��������"}]';
    $("#QueryDialog").QueryDialog({ data: arrStr });
});

function test() {
    $("#QueryDialog").show();
    $(".qdialog-mask").show();
}
```

## Data Structure

������һ���ַ������ṹʾ����

```javascript
var arrStr = '[{"queryfieldtype":"1","queryfieldname":"age","queryfieldrmk":"����"},{"queryfieldtype":"6","queryfieldname":"name","queryfieldrmk":"����"},{"queryfieldtype":"5","queryfieldname":"ismarried","queryfieldrmk":"�Ƿ��ѻ�"},{"queryfieldtype":"4","queryfieldname":"birthday","queryfieldrmk":"��������"}]';
```