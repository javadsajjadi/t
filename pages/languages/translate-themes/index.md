<div dir="rtl">

# وەرگێڕانی ڕووکار

<!-- position: 2 -->

هەر رووکارێک بوخچەیێکی بە ناوی `languages`، لە نێو ئەم بۆخچە بۆ هەر زمانێک پەڕگەی تایبەت دابین کراوە.

</div>

```
/bl-themes/{THEME_NAME}/languages/
	de_DE.json
	en.json
	es.json
	fr_FR.json
	...
```
<div dir="rtl">
<div class="note">
<div class="title">ئینکۆدینگی پەڕگە</div>
هەموو پەڕگەکان بە شێوەی <b>JSON</b> دروستکراوەن, وە هەموویان بە شێوەی <b>UTF-8</b> ئینکۆد کراون.
</div>

لێرە نمونەیێک لە زمانی ئینگلیزی لە پەڕگەی (`en.json`) دێنینەوە. هەر هێڵ لە پەڕگەی `en.json` جووتێک ژمارە-نرخی هەیە ، کە کلیلی لای ڕاست ئەندازە و کلیلی لای چەپ نرخ ـێکی بۆ دابین کراوە.

</div>

```
{
	"theme-data":
	{
		"name": "Pure",
		"description": "Simple and clean, based on the framework Pure.css."
	}
}
```

<div dir="rtl">

هەر وا کە دەبینن هەر ئێوە خانەیێک بە ناوی `theme-data`، کە بریتییە لە ناو و شرۆڤەی رووکار.

لێرە نمونەیێک لە زمانی سپانیۆلی دێنین کە لە مەسیری `/bl-themes/{THEME_NAME}/languages/es.json` جێگیر کراوە

 </div>

```
{
	"theme-data":
	{
		"name": "Pure",
		"description": "Simple y minimalista, basado en el framework Pure.css."
	}
}
```
