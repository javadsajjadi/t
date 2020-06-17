<div dir="rtl" >

# ناوەڕۆکی نەججوولاو
<!-- position: 4 -->

ئەم پەشە پەیوەندی بە ناوەرۆکی نەجوولاو هەیە [پەڕەکانی نەجوولاو](https://docs.bludit.com/en/content/content-basics#static).

## نیشاندانی تەواو پەڕە نەجوولاوەکان واتە ستاتیک
بلوودیت ناوێکی بە [predefined variable for static pages](https://docs.bludit.com/en/developers/predefined-variables#staticContent) named `$staticContent` هەیە. گۆڕاوێکە بۆ نیشاندانی تەواو پەڕە نەجولاوەکان
</div>

```
<?php
	// Each static page is an Page-Object
	foreach ($staticContent as $page) {
		echo $page->title();
	}
?>
```
