<div dir="rtl">

# سەردێر و شڕۆڤە
<!-- position: 2 -->

بلودیت یارمەتیتان دەدا کە بە کەمترین نووسین کۆدێکی پاک و خاوێن بنووسن.

<h2 id="title">سەردێڕ</h2>

چاپی بکە `<title>` سەردێر لە ناوەرۆکی جوولاو. سەردێر پەیکەرسازی دەکا ماڵپەڕەکەتان بۆ ریکخستن.
</div>

```
<?php
	echo Theme::metaTags('title');
?>
```

<div dir="rtl">
دەرئەنجامی کۆد
</div>	
	
```
<title>Page title | Title site</title>
```
<div dir="rtl">

<h2 id="description">شرۆڤە</h2>

چپکردنی`<description>` تاگێکی سەردێر بۆ ناوەرۆکی جولاو. شرۆڤە پەیکەرسازی دەکا بۆ رێکخستنی ماڵپەڕەکەت .

</div>

```
<?php
	echo Theme::metaTags('description');
?>
```
<div dir="rtl">
دەرنجامی HTML 
```
<meta name="description" content="Description about your site">
```
<div dir="rtl">
<h2 id="example">نمونە</h2>

لێرە نمونەیێکی تەواو لە سەردێر و شڕۆڤەیە بۆ نێو ماڵپەڕەکەت.
</div>

```
<!DOCTYPE html>
<html>
	<head>
		<?php
			echo Theme::metaTags('title');
			echo Theme::metaTags('description');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
