<div dir="rtl">

#  پەڕگەکانیCSS
<!-- position: 3 -->

بلودیت helpers بۆ گەشەپێدەران بڵاوکردووە کە کۆدی کەمتر لێبدەن.

بۆ ئەم فێرکارییە لە نێوەکانی خوارەوە سوود دەگرین
- ناوی رووکار `box`
- ناونیشانی ماڵپەڕ `https://www.example.com`
- شوێنی رووکار `/bl-themes/box/`
- CSS شوێنی پەڕگەکانی `/bl-themes/box/style.css`

helper بێت زۆر گرینگی نادەن بە مەسیریوەرن  پەڕگەیێک بە ناوی   `style.css`زیاد بکەین. شوێنی ئەم پەڕگەیە  `/bl-themes/box/style.css`؛ گەر ئێوە پەڕگەیێک بەناوی `Theme::` .
</div>


```
<?php
	echo Theme::css('style.css');
?>
```

<div dir="rtl">

دەرئەنجامیHTML

</div>

```
<link rel="stylesheet" type="text/css" href="https://www.example.com/bl-themes/box/style.css">
```

<div dir="rtl">
<h2 id="example">نمونەکان</h2>

کۆدی HTML وە PHP نمونەیێکی تەواو لە گونجاندنی دوو پەڕگەی CSS لە رووکارێکە
</div>


```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			echo Theme::css('style.css');
			echo Theme::css('buttons.css');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
