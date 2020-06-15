# Include plugins
<!-- position: 6 -->

بلودیت لە زیادکراوەکان پاڵپشتی دەکا هەر زیادکراوەیێک هۆکێکی تایبەت بە خۆی هەیە، هۆک فانکسێنێکن کە لە شوێنی جیاواز لە ڕووکار جێبەجی دەکرێن

پێرستێک لە هۆکەکان لێرە دەتوانن ببینن
- https://docs.bludit.com/en/plugins/hooks-list

بۆ نمونە بۆ جێبەجیکردنی تەواو زیاکراوە چالاکەکان  لە لایەن هۆکەکان لە  `siteHead`, ئەتوانن سود بگرن لە helper `Theme::plugins()`  .
```
<?php
	Theme::plugins('siteHead');
?>
```

<h2 id="example">نمونە</h2>

ليم نمونە ئێوە دەتوانن ببینن چۆن شی دانە هۆک لە شوێنی جیاواز لە ڕووکارێک جێبەجیبوون بە شێوازێکی دروست.

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