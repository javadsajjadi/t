<div dir="rtl" >

# تاگەکان
<!-- position: 6 -->

کۆدەبچکۆلەکان بۆ ئیشکردن لە سەر تاگەکان

گۆڕاوەکان کە ناسراوەن بۆ تاگەکان:
- `$tags` ئابجێکتی تاگەکانە بریتین لە , [ئەم کلاسانە](https://github.com/bludit/bludit/blob/master/bl-kernel/tags.class.php)

<div class="note">
بە پێشگریمان پەڕەی تاگەکان بە شێوەی ئەلف و بێ ریزکراوەن
</div>

<h2 id="list-all-tags"پێرستی تەواو تاگەکان</h2>
</div>

```
<?php
	// Returns an array with all the tags
	$items = getTags();

	foreach ($items as $tag) {
		// Each tag is an Tag-Object
		echo 'Tag name: '		. $tag->name();
		echo 'Tag key: ' 		. $tag->key();
		echo 'Tag link: ' 		. $tag->permalink();
		echo 'Tag number of pages: ' 	. count($tag->pages());
	}
?>
```

<div dir="rtl" >
جێگرەوە:
</div>

```
<?php
	foreach ($tags->keys() as $key) {
		// Create Tag-Object
		$tag = new Tag($key);

		echo 'Tag name: '		. $tag->name();
		echo 'Tag key: ' 		. $tag->key();
		echo 'Tag link: ' 		. $tag->permalink();
		echo 'Tag number of pages: ' 	. count($tag->pages());
	}
?>
```

<div dir="rtl" >
<h2 id="list-tags-that-have-pages">پیرستی تاگەکان لە  پەڕە</h2>
</div>

```
<?php
	$items = getTags();

	foreach ($items as $tag) {
		// Each tag is an Tag-Object
		if (count($tag->pages())>0) {
			echo 'Tag name: '	. $tag->name();
			echo 'Tag key: ' 	. $tag->key();
			echo 'Tag link: ' 	. $tag->permalink();
		}
	}
?>
```

<div dir="rtl" >
<h2 id="list-all-tags-and-pages">پێرستی تاگ و پەڕەکان کە پەیوەندیان بە تاگەکان هەیە</h2>
</div>

```
<?php
	$items = getTags();

	foreach ($items as $tag) {
		// Each tag is an Tag-Object
		echo 'Tag name: ' . $tag->name();

		// The method $tag->pages() returns all the pages keys releated to the tag
		foreach ($tag->pages() as $pageKey) {
			$page = new Page($pageKey);
			echo '- Page title: ' . $page->title();
		}
	}
?>
```

<div dir="rtl" >
<h2 id="list-all-pages-related-to-a-particular-tag">پێرستی تاگەکان کە پەیوەندیان بە پەڕەکان هەیە</h2>
</div>

```
<?php
        // Tag key
        $tagKey = 'example';

	// The tag is an Tag-Object
        $tag = getTag($tagKey);

        // Print the tag name
        echo 'Tag name: ' . $tag->name();

        // Print the pages title related to the tag "example"
        foreach ($tag->pages() as $pageKey) {
		$page = new Page($pageKey);
		echo $page->title();
        }
?>
```

<div dir="rtl" >
<h2 id="get-the-active-tag">وەرگرتنی تاگی چالاک</h2>
</div>

```
<?php
	// Check if the user is browsing a tag
	if ($WHERE_AM_I=='tag') {
		// Get the tag key from the URL
		$tagKey = $Url->slug();

		// Create the Tag-Object
		$tag = new Tag($tagKey);

		// Print the tag name
		echo $tag->name();
	}
?>
```

<div dir="rtl" >
<h2 id="print-the-tags-of-a-page">تاگەکانی یەک پەڕە</h2>

چاپی تاگەکان لە پەڕە:
</div>
```
<?php
	$returnsArray = true;

	$items = $page->tags($returnsArray);

	foreach ($items as $tagKey=>$tagName) {
		echo $tagName;
	}
?>
```

<div dir="rtl" >
چاپکردنی تاگ و بەستەرەکەی:
</div>

```

<?php
	$returnsArray = true;

	$items = $page->tags($returnsArray);

	foreach ($items as $tagKey=>$tagName) {
		$tag = new Tag($tagKey);

		echo '<a href="'.$tag->permalink().'">'.$tag->name().'</a>';
	}
?>
```

