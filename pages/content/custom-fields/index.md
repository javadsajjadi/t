<div dir="rtl">
	
# خشتەکانی دڵخواز
<!-- position: 7 -->

## ناساندن
خشتە دڵخوازەکان ڕێگا دەدەن بە بەکارهێنەر کە خشتی تایبەت بە خۆیان زیاد بکەن لە ناوەڕۆکی نووسین; ئەم خشتانە لە تختەی بەڕێوەبەرایەتی لە کاتی نووسین و  دەستکاری دەردەکەون گەر دروستت کردبێت.

## نمونەی خێرا
خشتێکی دڵخواز بەناوی `subtitle`.زیاد دەکەین و دەبێ بەم شوێنە هەنگاو بنینی
</div>

```
Admin panel > Sidebar > Settings > General > Custom fields
```
<div dir="rtl">
ئەم دەقەی پەڕگەی JSON لە نێو بۆکسی نووسین دادەنین و لە سەر دوگمەی "پاشکەوت" کرتە دەکین.
</div>

```
{
    "subtitle": {
        "type": "string",
        "placeholder": "Subtitle for the page",
		"position": "bottom"
    }
}
```
<div dir="rtl">
بۆ دروستکردنی پەڕەیێکی نوێ بەم شوێنە هەنگاو دادەنینی
</div>

```
Admin panel > Sidebar > New content
```
<div dir="rtl">
هەروا کە دەبینن خشتێک لە ژێر دەستکاری کەرەکە بوونی هەیە کە بەم عینوانە خۆیدەرخستووە "Subtitle for the page". تەواوی بکەن "Title", "Content" وە خشتی نوێی "Subtitle for the page" وە لە کۆتایی کرتە لەسەر دوگمەی "پاشکەوت" بکەن.

پەڕەی نوێی خشتێکی هەیە بەناوی `subtitle` ئێوە دەتوانن ئەم خشتە لە ڕووکارەکەتان بانگ بکەن یان چاپی بکەن وەک ئەم نموونە. 
</div>

```
<?php
	echo "The title of the page is " . $page->title();
	echo "The subtitle of the page is " . $page->custom('subtitle');
?>
```
<div dir="rtl">
## چوارچێوە
چوارچێوە بەم شێوازە JSON سروستدەکرێت,وە پشتیوانی دەکا لە کلیلانە:
- (required) `type`: جۆری خشتی دڵخواز بەم دوو کلیلە (`string`, `bool`).
- (optional) `label`: نیشانەی خشتی دڵخواز
- (optional) `tip`: دەقێکی بچکۆڵە بۆ شڕۆڤەی خشتی دڵخواز
- (optional) `default`: نرخی پێشگریمان بۆ خشتی دڵخوازی تایبەت
- (optional) `placeholder`: نووسراوەیێک بچکۆڵە لە نێو خشت
- (optional) `position`: شوێن لە دەستکاریکەر, پاڵپشتی دەکرێت بەم نرخانە (`top`, `bottom`). نرخەکان بە شێوەی پێشگریمان چۆڵن بەڵام شوێنی خشتەکان بەم ڕیگەن "Editor > Options > Custom".

## زیادکردنی خشتە دڵخوازەکان
بۆ ئەم مەبەستە هەنگاو بنە لەم شوێنە:
</div>

```
Admin panel > Sidebar > Settings > General > Custom fields
```
<div dir="rtl">
بۆ ناساندنی خشتەکان, بە دروستکرەری مەکینەی JSON نە.ئەم نمونە چاو لێبکە:

خشتە دڵخواز وەک `string` وە کەی ناوێک `youtube`:
</div>

```
{
    "youtube": {
        "type": "string",
        "label": "YouTube",
        "tip": "Write the YouTube URL."
    }
}
```
<div dir="rtl">
خشتە دڵخوازێک وەک `boolean`وە کەی ناوێک `inStock`:
</div>

```
{
    "inStock": {
        "type": "bool",
        "label": "In Stock",
        "tip": "Select this field if you have stock."
    }
}
```
<div dir="rtl">
دوو خشتە دڵخوازەکە جیاوازن بەم جۆرە
</div>

```
{
    "product": {
        "type": "string",
        "label": "Product",
        "tip": "Write the product name."
    },
    "inStock": {
        "type": "bool",
        "label": "In Stock",
        "tip": "Select this field if you have stock."
    }
}
```
<div dir="rtl">
سیهەمین خشتە دڵخواز لە دەستکاری کەر بۆم جۆرە دەبێ نیشان بدرێت
</div>

```
{
    "product": {
        "type": "string",
		"placeholder": "Product name",
		"position": "top"
    },
    "inStock": {
        "type": "bool",
        "tip": "Select this field if you have stock.",
		"position": "top"
    },
    "imageURL": {
        "type": "string",
		"placeholder": "Image URL",
		"position": "bottom"
    }
}
```
<div dir="rtl">
## وەرگرتنی خشتە دڵخواز
The class page provides the method `custom()`, which returns the value of the field.

The following example prints the value of the field `youtube` from the above example.
</div>

```
<?php
    echo $page->custom('youtube');
?>
```
<div dir="rtl">
Check the boolean value from the field `inStock` from the above example.
</div>

```
<?php
    if ($page->custom('inStock')) {
        echo "There is stock!";
    } else {
        echo "No more products";
    }
?>
```
<div dir="rtl">
## سڕینەوەی خشتە دڵخوازەکان
To delete a custom field you just need to remove the entry from the JSON structure. The custom fields are not completely deleted from the database when you do this, but they are invalidated.

If you want to remove all custom fields, just set an empty JSON in the textarea, as following:
</div>

```
{}
```
