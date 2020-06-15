<div dir="rtl">

# Translate a plugin



<!-- position: 1 -->

هەر زیادکراوە بوخچەیێکی`languages` تێدایە، لە نێم ئەم بوخچە ئێوە دەتوانن زمانی خۆتان زیاد بکەن و بۆ زمانی جیاوازی دیکە پەڕگەی تایبەت وەک وێنەکانی خوارەوە زیاد بکەن.

```
/bl-plugins/{PLUGIN_NAME}/languages/
	de_DE.json
	en.json
	es.json
	fr_FR.json
	ckb.json
	...
```

<div class="note">
<div class="title">ئینکۆدینگی پەڕەکان</div>
تەواوی پەڕگەکانی زمان بە شێوەی <b>JSON</b> ئینجا ئینکۆدینگی تەواوی پەڕگە زمانییەکان بە شێوەی <b>UTF-8</b>دابین کراوە.
</div>


لێرەنمونەیێک لە زمانی ئینگلیزییە (`en.json`). هەر هێڵ لە پەڕگەی `en.json`  پێکهاتووە لە کلیل-نرخ (key-value )کلیلی لە لای چەپ و نرخ لە لای چەپە.

```
{
	"plugin-data":
	{
		"name": "Page list",
		"description": "Shows the list of pages in order."
	},

	"home": "Home",
	"show-home-link": "Show home link"
}
```

هەر وا کە دەبینن خانەییکتان هەیە بە ناوی `plugin-data`, ئەمە ناو و شرۆڤەی زیادکراوەیە؛ وە لە خانەکانی دیکە دەست واژە بۆ زیادکراوە هەن، وەک : `home` وە`show-home-link`.

لێرە وێنەیێک لە زمانی سپانیۆلی دێنین کە لە مەسیری `/bl-plugins/{PLUGIN_NAME}/languages/es.json` دانراوەن.

```
{
	"plugin-data":
	{
		"name": "Listado de paginas",
		"description": "Muestra el listado de paginas en orden."
	},

	"home": "Inicio",
	"show-home-link": "Mostrar link de la pagina de incio"
}
```

</div>