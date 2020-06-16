<div dir="rtl">
	
# بریتییبوونی چوارچێوەلکان
<!-- position: 7 -->

ڕووکارەکانی بلوودیت زۆر نەرمن؛ ئێوە دەتوانن هەر چوارچێوە یان کتێبخانەیێکی تێخزێنن و سوودی لێبگرن (Bootstrap, Foundation, Bulma, UIkit, Semantic UI, ...), هەر Javascript کۆدێکیش, هەر شتێک کە هەرەکتانبێت.

ئێمە ژمارەیێکی کەم لە چوارچێوەکانمان نووسییەوە لەم پەڕە بەڵام ئێوە دەتوانن بە دەستکاری ئەم پەرە پێیان زیاد بکەن.

<h2 id="jquery">دابینکردنی jQuery</h2>

بلوودیت دوایین وشانی jQueryلە نێو پاکەتەکەی جێگیر کردووە، بەڵام ئێوە دەتوانن سوود بگرن بەیارمەتی helper
</div>

```
<?php
	echo Theme::jquery();
?>
```

<div dir="rtl">
HTML دەرئەنجامی
</div>

```
<script src="https://www.example.com/bl-kernel/js/jquery.min.js"></script>
```
<div dir="rtl">
<h2 id="bootstrap">Include Bootstrap</h2>

بلوودەیت دوایین وشانی  Bootstrap لە خۆی جێگیر کردووە، ئێوە دەتوانن بەیارمەتی helper بیخەنە نێو ڕووکار هەروەها پەڕگەکانی جاڤاسکریپت و...

دابینکردنی پەڕگەی  Javascript بۆ Bootstrap.
</div>

```
<?php
	echo Theme::jsBootstrap();
?>
```
<div dir="rtl">
HTML دەرئەنجام
</div>

```
<script src="https://www.example.com/bl-kernel/js/bootstrap.bundle.min.js"></script>
```
<div dir="rtl">
دابین کردنی پەڕگەی CSS بۆ Bootstrap.
</div>

```
<?php
	echo Theme::cssBootstrap();
?>
```

<div dir="rtl">
HTML دەرئەنجامی
</div>

```
<link rel="stylesheet" type="text/css" href="https://www.example.com/bl-kernel/css/bootstrap.min.css">
```
<div dir="rtl">
<h2 id="uikit">برییتییەکانی UIkit</h2>

ئەم پاکەتە لە نێو بلوودیت دابین نەکراوە بەڵآم ئێوە بەیارمەتی  helpers  لە نێو پەڕەکانی `Theme::css()` وە `Theme::js()` سوودی لێبگرن , هەروەها سوود بگرن لە UIkit CDN یان بە داگرتنی فایلە پێداویستییەکانی لە نێو رووکارەکەتان جێگیری بکەن،

نمونەی خوارەوە UIkit لە CDN دەخاتە نێو رووکار ،خاڵ وشەی `false` لە کۆتایی هێڵ سرنج بدەن ، ئەمە بە پەڕگە دەڵێت کە ئێمە هەرەکمانە کە پەڕگەیێک لە دەرەوە بێنین بۆ سوود وەرگرتن.
</div>

```
<?php
	echo Theme::css('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/css/uikit.min.css', false);

	echo Theme::js('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit.min.js', false);
	echo Theme::js('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit-icons.min.js', false);
?>
```
<div dir="rtl">
HTML دەرئەنجام
</div>

```
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/css/uikit.min.css">

<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit-icons.min.js"></script>
```
