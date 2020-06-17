# صشتەکانی دڵخواز
<!-- position: 7 -->

## ناساندن
خشتە دڵخوازەکان ڕێگا دەدەن بە بەکارهێنەر کە خشتی تایبەت بە خۆیان زیاد بکەن لە ناوەڕۆکی نووسین; ئەم خشتانە لە تختەی بەڕێوەبەرایەتی لە کاتی نووسین و  دەستکاری دەردەکەون گەر دروستت کردبێت.

## نمونەی خێرا
خشتێکی دڵخواز بەناوی `subtitle`.زیاد دەکەین و دەبێ بەم شوێنە هەنگاو بنینی
```
Admin panel > Sidebar > Settings > General > Custom fields
```

ئەم دەقەی پەڕگەی JSON لە نێو بۆکسی نووسین دادەنین و لە سەر دوگمەی "پاشکەوت" کرتە دەکین.
```
{
    "subtitle": {
        "type": "string",
        "placeholder": "Subtitle for the page",
		"position": "bottom"
    }
}
```

بۆ دروستکردنی پەڕەیێکی نوێ بەم شوێنە هەنگاو دادەنینی
```
Admin panel > Sidebar > New content
```

As you can see there is a new field at the bottom of the editor requesting a "Subtitle for the page". Complete the "Title", "Content" and the new field "Subtitle for the page" and click on the button "Save".

The new page has a custom field called `subtitle` and you can print the value from the theme. For example.
```
<?php
	echo "The title of the page is " . $page->title();
	echo "The subtitle of the page is " . $page->custom('subtitle');
?>
```

## چوارچێوە
The structure is defined in the JSON format, and supports the following keys:
- (required) `type`: Type of the custom field, supported values (`string`, `bool`).
- (optional) `label`: The label for the custom field.
- (optional) `tip`: Small text for the user to describe the custom field.
- (optional) `default`: Default value for the custom field.
- (optional) `placeholder`: Small text inside the field.
- (optional) `position`: Position in the editor, supported values (`top`, `bottom`). Default value is empty and the field apper in "Editor > Options > Custom".

## زیادکردنی خشتە دڵخوازەکان
بۆ ئەم مەبەستە هەنگاو بنە لەم شوێنە:
```
Admin panel > Sidebar > Settings > General > Custom fields
```

بۆ ناساندنی خشتەکان, بە دروستکرەری مەکینەی JSON نە.ئەم نمونە چاو لێبکە:

خشتە دڵخواز وەک `string` وە کەی ناوێک `youtube`:
```
{
    "youtube": {
        "type": "string",
        "label": "YouTube",
        "tip": "Write the YouTube URL."
    }
}
```

خشتە دڵخوازێک وەک `boolean`وە کەی ناوێک `inStock`:
```
{
    "inStock": {
        "type": "bool",
        "label": "In Stock",
        "tip": "Select this field if you have stock."
    }
}
```

دوو خشتە دڵخوازەکە جیاوازن بەم جۆرە
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

سیهەمین خشتە دڵخواز لە دەستکاری کەر بۆم جۆرە دەبێ نیشان بدرێت
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

## وەرگرتنی خشتە دڵخواز
The class page provides the method `custom()`, which returns the value of the field.

The following example prints the value of the field `youtube` from the above example.
```
<?php
    echo $page->custom('youtube');
?>
```

Check the boolean value from the field `inStock` from the above example.
```
<?php
    if ($page->custom('inStock')) {
        echo "There is stock!";
    } else {
        echo "No more products";
    }
?>
```

## سڕینەوەی خشتە دڵخوازەکان
To delete a custom field you just need to remove the entry from the JSON structure. The custom fields are not completely deleted from the database when you do this, but they are invalidated.

If you want to remove all custom fields, just set an empty JSON in the textarea, as following:
```
{}
```
