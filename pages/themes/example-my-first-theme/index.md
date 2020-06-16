<div dir="rtl">
	
# نموونە: یەکەم ڕووکارەکەم
<!-- position: 101 -->

وەرن بە ڕووکارێکی سادە دروستبکەین ناوی ئەم رووکارە دنم `Coffee`.

- لە نێو ئەم بوخچە `/bl-themes/` ڕووکارەکەم دادەنێم کە دەبێتە ئەم شوێنە : `/bl-themes/coffee/`.
- بوخچەی  `languages` دروستدەکەم، لە نێو ئەم شوێنە `/bl-themes/coffee/` .
- بوخچەی `en.json` دروستدەکەم لەنێو بوخچەی `/bl-themes/coffee/languages/` .
- پەڕگەی `metadata.json` لە نێو بوخچەی `/bl-themes/coffee/` دروستدەکەم.
- پەڕگەی `index.php`، لە نێو بوخچەی `/bl-themes/coffee/` دروستدەکەم.

کاتێک تەواو بوو، ئێوە بوخچە و پەڕگەی نێو ڕووکارەکەتان بەم جۆرە دەبینن:
</div>
	
```
/bl-themes/coffee/
	languages/en.json
	metadata.json
	index.php
```

<div dir="rtl">
قۆناغی دیکە نووسینی ناوەڕۆکی پەڕگەکانە. بێنەوە دەست بە٣دروستکردنی پەڕگەی `index.php` بەیارمەتی HTML وە PHP بکەین:
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>Bludit</title>
</head>
<body>
	<?php foreach ($content as $page): ?>

		<h1><?php echo $page->title(); ?></h1>
		<div><?php echo $page->content(); ?></div>
		<hr>

	<?php endforeach; ?>
</body>
</html>
```

<div dir="rtl">
دەستکاری پەڕگەی `languages/en.json` بکەن و ناو و شرۆڤەی ڕووکاری پێ زیاد بکەن.
</div>

```
{
	"theme-data":
	{
		"name": "Coffee",
		"description": "This is my first theme for Bludit."
	}
}
```

<div dir="rtl">
ئێستا دەستکاری پەڕگەی `metadata.json` بۆ تەواوکردنی زانیاری رووکار ئەنجام بدەن
</div>

```
{
	"author": "Bludit",
	"email": "",
	"website": "",
	"version": "1.0",
	"releaseDate": "2019-01-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

<div dir="rtl">
پیرۆزە!یەکەم ڕووکارت دروست کرد!ئێستا دەبێ بچن بۆ بەشت رێکخستنەکان لە تەختەی بەڕێوەبەر و ڕووکارەکەتان چالاک بکەن.
</div>
