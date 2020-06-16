<div dir="rtl">

# چوارچێوەی بوخچەکان
<!-- position: 2 -->

چوارچێوەی بوخچەکان لە بلوودیت بەم جۆرە بوونیان هەیە
</div>

```
/bl-content/	<-- Databases and uploaded images
/bl-kernel/		<-- Core of Bludit
/bl-languages/	<-- Languages files
/bl-plugins/	<-- Plugins
/bl-themes/		<-- Themes
```

<div dir="rtl">
	
## bl-content
ئەم بوخچە زۆر گرنگە, بۆ ئەوە وەک پاشکۆی پەڕگەکان کردار دەکا لە بلوودیت, بۆ ووینە وەک بنکەدراوە بۆ نووسراوەکان و وێنە ،پاش بەڕۆژکردنی بلوودیت پێشنیار ئەوەیە کە بەکاپێک لەم  بوخچە بگرن.
</div>

```
/bl-content/

	databases/
		plugins/		<-- Database: plugins
		pages.php		<-- Database: pages
		security.php	<-- Database: black list, brute force protection, others
		site.php		<-- Database: site variables, name, description, slogan, others
		tags.php		<-- Database: tags
		users.php		<-- Database: users

	pages/				<-- Content: pages
		about/index.txt
		food/index.txt

	tmp/				<-- Temp files

	uploads/			<-- Uploaded files
		profiles/		<-- Profiles images
		thumbnails/		<-- Thumbnails images
		photo1.jpg
		photo2.png

	workspaces/			<-- Workspaces for the plugins
```

<div dir="rtl">
	
## bl-kernel
ئەم بوخچە ناوکی بلوودیتە واتە بەشی بەڕێوەبردنی سیستەم


## bl-languages
تەواوی زمانەکان کە بلوودیتی پێ وەرگێڕاوە لەم بوخچەن کە بریتییەلە چەندین پەڕگەی JSON ,بە ئینکۆدینگی UTF-8.
</div>

```
/bl-languages/
	bg_BG.json
	cs_CZ.json
	de_CH.json
	en.json
	es.json
	...
```

<div dir="rtl">
	
## bl-plugins
بوخچەی زیادکراوەکان ،هەر زیادکراوەیێک کە دایدەگرن دەبێ بیخەنە نێو ئەم بوخچە و پاشان لە بەشی بەڕێوەبەر دامەزرێنن
</div>

```
/bl-plugins/
	about/
	disqus/
	rss/
	sitemap/
	tinymce/
	...
```

<div dir="rtl">
	
## bl-themes
بوخچەی رووکارەکان، هەر ڕووکارێکیش دادەگرن سەرەتا دەبێ لەم بوخچە باری بکەن ئینجا لە بەشی بەرێوەبەر چالاکی بکەن
</div>

```
/bl-themes/
	alternative/
	blogx/
	...
```
