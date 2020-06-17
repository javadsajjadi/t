<div dir="rtl" >

# ناوەڕۆکی پەڕەکان
<!-- position: 3 -->

لە نمونەی خوارەوە جۆری ناوەرۆکی **پەڕەکان**بەکاربراوە; پەڕەکان بڵاوکراوەن (بەکارهێنەران دەیانبینن) لەم نمونە کە ئیشی لەسەر دەکەین.

<h2 id="list-all-pages-from-the-active-page">پێرستی تەواو ژێر پەڕەکان لە پەڕەی تایبەت:</h2>

بلوودیت بە شیوازی پێشگریمان `$content` ئەرای تەواو ژێر پەڕەکانی (یان منداڵ پەڕەکان) لە پەڕەی ئێستا کە بەکارهێنەر دەیبینێت هەیە. ئەم یەرایە سوودی لێدەگرن لە ڕووکار ئەم کۆدە سەردێر و ناوەڕۆک لە پەڕە چاپ دەکات.
</div>

```
<?php
	foreach ($content as $page) {
		echo $page->title();
		echo $page->content();
	}
?>
```

<div dir="rtl" >
<h2 id="list-the-latest-5-pages">پێرستی ٥ پەڕە</h2>

ئەم کۆدە چکۆڵە دەگەڕێنێتەوە `title` لە ٥ پەڕەی بڵاوکراوە کە لە ئاستی `published` دان.
</div>

```
<?php
	// Page number, the first page is 1
	$pageNumber = 1;

	// Number of items to return
	$numberOfItems = 5;

	// Only get the pages with the status published
	$onlyPublished = true;

	// Get the list of keys of pages
	$items = $pages->getList($pageNumber, $numberOfItems, $onlyPublished);

	foreach ($items as $key) {
		// buildPage function returns a Page-Object
		$page = buildPage($key);

		// Print the page title
		echo $page->title();
	}
?>
```

<div dir="rtl" >
<h2 id="list-all-pages">پێرستی تەواو پەڕەکان</h2>

ئەم کۆدە بچکۆڵە چاپدەکات `title` بۆ تەواو پەڕەکان لەدۆخی `published`. تکایە ئاگادار بە بە پێی ژمارە پەڕەکان دەتوانێت کاریگەری لەسەر کردار بێت.
</div>

```
<?php
	// Page number of the paginator, the first page is 1
	$pageNumber = 1;

	// The value -1 tell to Bludit to returns all the pages on the system
	$numberOfItems = -1;

	// Only get the pages with the satus published
	$onlyPublished = true;

	// Get the list of keys of pages
	$items = $pages->getList($pageNumber, $numberOfItems, $onlyPublished);

	foreach ($items as $key) {
		// buildPage function returns a Page-Object
		$page = buildPage($key);

		// Print the page title
		echo $page->title();
	}
?>
```
<div dir="rtl" >
## ئیسکردن بە ژێر پەڕە
بلوودیت پشتیوانی دەکات ئاستی ژێرپەڕە

بۆ ئیش کردن بە ژێر پەڕە پێویستان بە جێگیرکردنی پەڕە لە ئاستی `position` هەیە.
</div>
