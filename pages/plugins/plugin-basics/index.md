<div dir="rtl">
	
# بنەمای سەرەتایی زیادکراوە
<!-- position: 1 -->

زیادکراوەکان لە بلوودیت لە بوخچەی `bl-plugins` جێگیر بووە، وە هەر زیادکراوە چوارچێوەیێکی تایبەتی هەیە. هەر زیادکراوە لە بلوودیت لە ئۆبجیکتەکان بە هووک(مێتۆد)ـی جیاواز دروست بووە. (methods).

<h2 id="structure">چوارچێوەی پەڕگە و بوخچە</h2>
ئەمە چوارچێوەی بنەمایی بۆ پەڕگە و بوخچەکانن :
</div>

```
/bl-plugins/{PLUGIN_NAME}/
	languages/en.json
	metadata.json
	plugin.php
```

<div dir="rtl">
<h2 id="name-and-description">ناو و شڕۆڤە</h2>
ناو و شڕۆڤەی زیادکراوەکان لە پەڕگەی JSON جێبەجێ بووە بەم جۆرە, `languages/en.json`.
</div>

```
{
	"plugin-data":
	{
		"name": "Hello World",
		"description": "Print Hello World in the sidebar"
	}
}
```

<div dir="rtl">
<h2 id="information">زانیاری</h2>
زانیاری زیادکراوە لە پەڕگەی JSON بوونی هەیە بە شێوازی پەڕگەی `metadata.json`.
</div>

```
{
	"author": "Bludit",
	"email": "",
	"website": "https://plugins.bludit.com",
	"version": "1.0",
	"releaseDate": "2018-08-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

<div dir="rtl">
<h2 id="hello-world">سڵاو یاپراخ</h2>
سڵآو یاپراخ لە نێو پەڕگەیێک بە ناوی`plugin.php` جێگیر دەبێت تا کرداری زیادکراوەیێک بۆ بلوودیت ئەنجام بدات.
</div>

```
<?php
	class pluginHello extends Plugin {
		public function siteSidebar() {
			echo 'سڵآو یاپراخ';
		}
	}
?>
```
<div dir="rtl">
<div class="note">
<div class="title">داگرتن</div>
سەرچاوەکۆدی سڵاو یاپراخ دابگرە <a href="https://github.com/bludit/examples/tree/master/plugins/hello-world">سڵآو یاپراخ</a>.
</div>
</div>
</div>
