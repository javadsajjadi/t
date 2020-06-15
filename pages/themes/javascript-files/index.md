# Javascript files
<!-- position: 4 -->

بلودیت helpers ـی دابین کردووە کە گەشەپێدەران بتوانن کۆدی کەمتر بنووسن.

بۆ فێرکاری لە نێوەکانی خواروە سوود دەبینین:
- ناوی رووکار `box`
- ناونیشانی ماڵپەڕ `https://www.example.com`
- Tمەسیری رووکار `/bl-themes/box/`
- مەسیری پەڕگەی جاڤاسکریپت `/bl-themes/box/main.js`

بێنەوە پەڕگەیێکی جاڤاسکریپت  Javascript لە رووکار بەناوی `main.js`، کە لە مەسیری  `/bl-themes/box/main.js`   زیادی بکەین. گەر ئێوە helperبەناوی `Theme::`  ببێت .
```
<?php
	echo Theme::js('main.js');
?>
```

HTML دەرئەنجام
```
<script src="https://www.example.com/bl-themes/box/main.js"></script>
```

<h2 id="example">نمونە</h2>

لەم نمونە فێردەبیین کە چۆن دوو کۆدی   Javascript رووکار بوونیان هەیە.

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

<?php
	echo Theme::js('main.js');
	echo Theme::js('buttons.js');
?>

</body>
</html>
```
