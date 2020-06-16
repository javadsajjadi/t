<div dir="rtl">

# بنەمای ڕووکار
<!-- position: 1 -->

رووکاری بلودیت زۆر نەرمەو و ئێوە دەتوانن لە نێوی سوود لە چوارچێوەکانی ([Bootstrap](http://getbootstrap.com/), [Foundation](https://foundation.zurb.com/), [Bulma](https://bulma.io), [UIkit](https://getuikit.com/), [Semantic UI](https://semantic-ui.com), etc), هەر کۆدێکی Javascript , لە هەر کوێ گەرەکتانە بگرن.

تەواو رووکارەکان لە بوخچەی `bl-themes` و چوارچێکەوەکەیان لە پێش بە شێوازی ستاندارد ذاڕژاوە.

<h2 id="structure">چوارچێوەی بوخچە و پەڕگەکان</h2>

ئەمە چوارچێوەیێکی ستانداردە بۆ ڕووکارەکان.
</div>


```
/bl-themes/{THEME_NAME}/
	languages/en.json
	metadata.json
	index.php
```

<div dir="rtl">
	
<h2 id="name-description">ناو و شرۆڤە</h2>

ناو و شڕۆڤەکانی ڕووکار لە پەڕگەیێکیJSON لەم شوێنە جێگیر بووە  `languages/en.json`   .
</div>

```
{
	"theme-data":
	{
		"name": "Hello World",
		"description": "My new theme"
	}
}
```
<div dir="rtl">
<h2 id="information">زانیاری</h2>

زانیاری رووکار لە پەرگەیێکیJSON لەم شوێنێ دابین کراوە    `metadata.json`  .
</div>

```
{
	"author": "Bludit",
	"email": "",
	"website": "https://themes.bludit.com",
	"version": "1.0",
	"releaseDate": "2018-08-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

<div dir="rtl">
<h2 id="examples">نمونەی روکار</h2>

لێرە دوو نمونە رووکارمان هەیە نمونەیێکی سادە و نموونەیێک کەمێ ئاڵۆز لەگەڵ پەڕگەکانی CSS وە Javascript پەڕگەیە.

- [یەکەمین رووکارەکەم](https://docs.bludit.com/en/themes/example-my-first-theme)
- [دووهەمین رووکارەکەم](https://docs.bludit.com/en/themes/example-my-second-theme)

</div>
