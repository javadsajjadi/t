<div dir="rtl">

# وەرگێڕانی روکار

<!-- position: 2 -->

هەر روکارێک بوخچەیێکی بە ناوی `languages`، لە نێو ئەم بۆخچە بۆ هەر زمانێک پەڕگەی تایبەت دابین کراوە.

</div>

```
/bl-themes/{THEME_NAME}/languages/
	de_DE.json
	en.json
	es.json
	fr_FR.json
	...
```

<div class="note">
<div class="title">ئینکۆدینگی پەڕگە</div>
هەموو پەڕگەکان بە شێوەی <b>JSON</b> دروستکراوەن, وە هەموویان بە شێوەی <b>UTF-8</b> ئینکۆد کراون.
</div>

This is an example of an English dictionary file (`en.json`). Each line in the `en.json` file is a key-value pair, with the key on the left and the value on the right.

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

> </div>

```
{
	"theme-data":
	{
		"name": "Pure",
		"description": "Simple y minimalista, basado en el framework Pure.css."
	}
}
```
