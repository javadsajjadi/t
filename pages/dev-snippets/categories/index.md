<div dir="rtl" >
	
# هاوپۆلەکان
<!-- position: 5 -->

پارچەکۆدێک لە جۆری ئیشکردن بە هاوپۆلەکان لێرە دەخەینە بەردەست

گۆڕاوەکان کە پێشتر ناسراوەن بۆ هاوپۆلەکان:

- `$categories` ئابجێکتی هاوپۆلە; [بۆ کلاسەکانی](https://github.com/bludit/bludit/blob/master/bl-kernel/categories.class.php).

<div class="note">
بە شێوازی پێسگریمان هاپۆلەکان بە پیتی ئەلف و بێ ریز کراوەن
</div>

<h2 id="list-all-categories">پێرستی تەواو هاوپۆلەکان:</h2>
</DIV>

```
<?php
	$items = getCategories();

	foreach ($items as $category) {
		// Each category is an Category-Object
		echo 'Category name: '			. $category->name();
		echo 'Category key: ' 			. $category->key();
		echo 'Category description: ' 		. $category->description();
		echo 'Category template: ' 		. $category->template();
		echo 'Category link: ' 			. $category->permalink();
		echo 'Category number of pages: ' 	. count($category->pages());
	}
?>
```
<div dir="rtl" >
جێگرەوە:

```
<?php
	foreach ($categories->keys() as $key) {
		// Create Category-Object
		$category = new Category($key);

		echo 'Category name: '			. $category->name();
		echo 'Category key: ' 			. $category->key();
		echo 'Category description: ' 		. $category->description();
		echo 'Category template: ' 		. $category->template();
		echo 'Category link: ' 			. $category->permalink();
		echo 'Category amount of pages: ' 	. count($category->pages());
	}
?>
```

<div dir="rtl" >
<h2 id="list-categories-that-have-pages">پێرستی هاوپۆلەکان کە پەڕەیان هەیە:</h2>
</DIV>

```
<?php
	$items = getCategories();

	foreach ($items as $category) {
		// Each category is an Category-Object
		if (count($category->pages())>0) {
			echo 'Category name: '	. $category->name();
			echo 'Category key: ' 	. $category->key();
			echo 'Category link: ' 	. $category->permalink();
		}
	}
?>
```

<div dir="rtl" >
<h2 id="list-all-categories-and-pages">پێرستی هاوپۆلەکان و پەڕەی پەیوەندی بە هاوپۆلەکان:</h2>
</DIV>

```
<?php
	$items = getCategories();

	foreach ($items as $category) {
		// Each category is an Category-Object
		echo 'Category name: ' . $category->name();

		// The method $category->pages() returns all the pages keys releated to the category
		foreach ($category->pages() as $pageKey) {
			$page = new Page($pageKey);
			echo '- Page title: ' . $page->title();
		}
	}
?>
```

<div dir="rtl" >
<h2 id="list-all-pages-related-to-a-particular-category">پێرستی تەواو پەڕەکان کە پەیوەندی بە هاوپۆلێکی تایبەت هەیە:</h2>
</DIV>

```
<?php
        // Category key
        $categoryKey = 'example';

		// The category is an Category-Object
        $category = getCategory($categoryKey);

        // Print the category name
        echo 'Category name: ' . $category->name();

        // Print the pages title related to the category "example"
        foreach ($category->pages() as $pageKey) {
			$page = new Page($pageKey);
			echo $page->title();
        }
?>
```

<div dir="rtl" >
<h2 id="get-the-active-category">بۆ وەرگرتنی چالاکی هاوپۆل:</h2>
	</DIV>
	
```
<?php
	// Check if the user is browsing a category
	if ($WHERE_AM_I=='category') {
		// Get the category key from the URL
		$categoryKey = $url->slug();

		// Create the Category-Object
		$category = new Category($categoryKey);

		// Print the category name
		echo $category->name();

		// Print the category description
		echo $category->description();
	}
?>
```
