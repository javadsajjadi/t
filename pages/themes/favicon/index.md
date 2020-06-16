<div dir="rtl">
	
# ئایکۆن
<!-- position: 5 -->

بلودیت helpers  بڵآوکردووە تا گەشەپێدەران کۆدی کەمتر بنووسن.

بۆ ئەم فێرکارییە کە ناوەکانی خوارەوە سوود دەگرین
- ناوی رووکار `box`
- ناونیشانی ماڵپەڕ `https://www.example.com`
- شوێنی رووکار `/bl-themes/box/`
- شوێنی ئایکۆن `/bl-themes/box/favicon.png`

قۆناغی دیکە لە  helperـی  `Theme::` تاگی head بۆ ئایکۆن دروست دەکرێت; بە شێوازی گریمانە،  MIME type نرخی `image/png` دەگەڕێنێتەوە .
</div>

```
<?php
	echo Theme::favicon('favicon.png');
?>
```
<div dir="rtl">
دەرئەنجامی HTML
</div>

```
<link rel="shortcut icon" href="https://www.example.com/bl-themes/box/favicon.png" type="image/png">
```
<div dir="rtl">
هەروەها گەر هەرەکتانە لەجۆرێکی دیکەی ئایکۆن سوود بگەن بۆ وێنە `.ico` دەتوانن  MIME type دابین بکەن .
	</div>
	
```
<?php
	echo Theme::favicon('favicon.ico', 'image/x-icon');
?>
```

<div dir="rtl">
دەرئەنجامی HTML
</div>

```
<link rel="shortcut icon" href="https://www.example.com/bl-themes/box/favicon.ico" type="image/x-icon">
```
<div dir="rtl">
<h2 id="example">نموونە</h2>

لێرە نمونەیێکی تەواو لە فێرکاری دابین کردنی ئایکۆن لە کۆدی رووکارمان هاوردووەتەوە.
</div>

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			echo Theme::favicon('favicon.png');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```
