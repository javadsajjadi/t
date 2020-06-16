<div dir="rtl">
	
# بریتیبوونی زیادکراوەکان
<!-- position: 6 -->

بلودیت لە زیادکراوەکان پاڵپشتی دەکا هەر زیادکراوەیێک هووکێکی تایبەت بە خۆی هەیە، هووک فانکشێنێکن کە لە شوێنی جیاواز لە ڕووکار .جێبەجی دەکرێن

پێرستێک لە هووکەکان لێرە دەتوانن ببینن
- https://docs.bludit.com/en/plugins/hooks-list

بۆ نمونە بۆ جێبەجیکردنی تەواو زیادکراوە چالاکەکان  لە لایەن هووکەکان لە  `siteHead`, ئەتوانن سود بگرن لە helper `Theme::plugins()`  .
</div>

```
<?php
	Theme::plugins('siteHead');
?>
```
<div dir="rtl">
<h2 id="example">نمونە</h2>

لەم نمونە ئێوە دەتوانن ببینن چۆن سێ دانە هووک لە شوێنی جیاواز لە ڕووکارێک جێبەجێبوون بە شێوازێکی دروست.
</div>

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			Theme::plugins('siteHead');
		?>
	</head>
<body>

<?php
	Theme::plugins('siteBodyBegin');
?>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

<?php
	Theme::plugins('siteBodyEnd');
?>

</body>
</html>
```
