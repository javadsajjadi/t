<div dir="rtl" >

# نمونە: دووهەمین ڕووکارەکەم
<!-- position: 101 -->

لێرە دووهەمین نمونە لە دروستکردنی ڕووکار بۆ بڵوودیت دەهێنینەوە کە بریتییە لە پەڕگەی CSS, Javascript, وە پاڵپشتی زیادکراوەکان

ناوی ئەم ڕووکارە  `Mars` ــە.

گەر خۆشت لە خوویندنیوەی ئەم فێرکارییە نییە دەتوانی کۆدی ئەم ڕووکارە لێرە دابگری <a href="https://github.com/bludit/examples/tree/master/themes/mars">ڕووکاری مارس</a>.

<h2 id="folder-structure">چوارچێوەی بوخچەی ڕووکار</h2>
لەم شوێنە بوخچەی ڕووکارێ دیزاین بکەن `/bl-themes/` ;شوێنەکەی بەم شێوە دەبێ: `/bl-themes/mars/`.

ئێستا دەبێ بوخچەکان languages ، CSS وە JAVASCRIPT دروستبکەن
- بوخچەیێک بە ناوی  `languages` لەم مەسیرە دروستبکەن `/bl-themes/mars/`
- بوخچەیێک بە ناوی `css` لەم مەسیرە دروستبکەن `/bl-themes/mars/`
- بوخچەیێک بە ناوی `js` لەم مەسیرە دروستبکەن `/bl-themes/mars/`
</div>

```
/bl-themes/mars/
	css/
	js/
	language/
```

<div dir="rtl" >
<h2 id="name-and-information">ناو و زانیاری</h2>
پەڕەیێک بۆ زانیاری ڕووکار دروستبکەن.ئەم پەڕگەیە دەبێ لە نێو بوخچەی ڕووکار بێت, دەبێ نێوی `metadata.json` بێت. ئەمە بریتییە لە پەڕگەی JSON کۆد:
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

<div dir="rtl" >
پەڕگەیێکی دیکەبە ناوی `en.json` دروستبکەن, کە ناوی و شرۆڤەی ڕووکاری تێدا یە، ئینجا بیخەنە نێو ئەم شوێنە `/bl-themes/mars/languages/` ئەمەش شێوەپەڕگەی JSON کۆدە:
</div>

```
{
	"theme-data":
	{
		"name": "Mars",
		"description": "This is my second theme for Bludit."
	}
}
```

<div dir="rtl" >
<h2 id="index">Index.php پەڕگەی</h2>
بینەوە ئیش لەسەر پەڕگەی `index.php` بکەین; لەم شوێنە ئەم پەڕەگەی دروستبکەن `/bl-themes/mars/` ,بە یارمەتی HTML کۆدەکان:
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
</head>
<body>

</body>
</html>
```

<div dir="rtl" >
<h2 id="css-files">CSS پەڕگەکانی</h2>
لە نێو پەڕگەی CSS چەند شت زیاد دەکەین:
- سوود بگرن لە ئابجێکتی Helper وەک `Theme::css()`
- یان سوود بگرن لە کۆدەکانی HTML  `<link href="..." rel="stylesheet" type="text/css" />`

لەم نمونە ئێمە پەڕگەکانی  CSS لەم شوێنە دادەنین `/bl-themes/mars/css/style.css`. بە Helper, ئێوە پێویستان بە شوێنی تەواو نییە
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>
</head>
<body>

</body>
</html>
```

<div dir="rtl" >
<h2 id="javascript-files">Javascript پەڕگەکان</h2>
پەڕگەکان جاڤاسکریپت بەم جۆرە زیاددەکەین:
- سوود وەرگرتن لە ئابجێکتی یاریدەدەر `Theme::js()`
- یان سوود گرتن لە کۆدەکانی تاگی HTML بەم جۆرە `<script>...</script>`

لەم نمونە ئێمە کۆدەکانی جاڤا سکریپت  لەم شوێنە دادەنین  `/bl-themes/mars/js/mars.js`. بە سوود وەرگرتن لە یاریدەدەر ئێوە پێویست بە  شوێنی تەواو ناکەن لە کۆد نووسینی لە پەڕە.
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>
</head>
<body>

</body>
</html>
```

<div dir="rtl" >
<h2 id="plugin-support">زیادکردنی پشتیوانی زیادکراوە</h2>
بۆ پشتیوانی لە زیادکراوەکان لە رووکار،دەتوانن سوود بگرن لە یارمەتیدەر helper `Theme::plugins()`.

هووکی زیادکراوەکان لە ماڵپەڕ بەم جۆرن کە خۆیان لە ڕووکار دەگونجێنن:
- `siteHead` بریتییە لە تەواو ئەم زیادکراوانە کە دەگەرێنەوە بۆ ناوی تاگەکانی `<head>...</head>` .
- `siteBodyBegin` دەگەڕیتەوە بۆ تەواو ئەو زیادکراوانە کە لە نێو تاگەکانی `<body>...</body>` بۆ وینە بەنێرێکی بەخێرهاتن یان مێنیۆیێک لە سەرەوەی ناوەرۆکەکان
- `siteBodyEnd` دەگەڕێتەوە بۆ تەواو زیادکراوەکانکە لە نێوان تاگەکانی `<body>...</body>`ئەڵبەت لەخوارەوەی پەڕە,وەک کۆدەکانی JavaScript .
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<!-- Here all the rest of HTML code -->

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```
<div dir="rtl" >
<h2 id="site-logo-title-and-slogan">لۆگۆ و سەردێڕی ماڵپەڕ</h2>
دەتوانن لە ئابجیکتی ماڵپەڕ بۆ لۆگۆ و سەردێر سوود بگرن
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<img src="<?php echo $site->logo() ?>" alt="" width="128">
	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<div dir="rtl" >
<h2 id="where-am-i">تا ئێستا من لە کوێی دیزاینم</h2>
بێنەوە با ئیش لە سەر ناوەڕۆکی ماڵپەڕ بکەین کە دەنووسرێت لە لایەن بەکارهێنەر

بۆ ئەوە پەڕە کە بەکارهێنەر بۆی دەگەڕێت لە مآلپەر دەتوانن ئەم گۆڕاوە `$WHERE_AM_I` بەکاربهێنن. بۆ نمونە, گەر بەکارهێنەر چاو لە پەڕەیێک دەکات،نرخی گۆڕاوە بەشێوازی `page` لێدێت, گەر بەکارهێنەر چاو لە پەڕەی سەرەتایی دەکات (پەڕەی ماڵەوە) نرخی گۆراوە دەگەڕێتەوە بۆ `home`.
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<p>The user is watching a particular page</p>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<p>The user is watching the homepage</p>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<div dir="rtl" >
<h2 id="main-content">ناوەڕۆکی ئەسڵی</h2>
گەر بەکارهێنەرێک لە پەڕەی سەرەتایی بێت,بلوودیت ئاراییکی گشتی دروست دەکات بەناوی `$pages` بۆ تەواو پەڕەی بڵاوکراوە.هەر پەڕەیێک دانەیێک `Page Object` هەیە.
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<p>The user is watching a particular page</p>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<?php foreach ($content as $page): ?>
			<h3><?php echo $page->title(); ?></h3>
		<?php endforeach ?>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<div dir="rtl" >
گەر بەکارهێنەر خەریکی چاولێکردن لە پەڕەیێکی تایبەت بێت بلوودیت نەکینەی پەڕەکان دروست دەکا لە  `$page`. ئەم نمونە بۆ ئەوەدەهێننەوە کە پەڕەکەمان بریتییە لە سەردێڕ و ناوەڕۆکی نووسراوە کەدەتوانێ وێنە ،دەنگ،فیلم و.. بێت.
</div>

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<h3><?php echo $page->title(); ?></h3>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<?php foreach ($pages as $page): ?>
			<h3><?php echo $page->title(); ?></h3>
		<?php endforeach ?>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```
<div dir="rtl" >
<div class="note">
<div class="title">داگرتن</div>
داگرتنی کۆدی سەرچاوەی <a href="https://github.com/bludit/examples/tree/master/themes/mars">رووکاری مارس</a>.
</div>
</div>
