<div dir="rtl" >
	
# پەڕەی باوان و ژێر پەڕە
<!-- position: 7 -->

<div class="note">
ئەم پارچەکۆدانە ئیش دەکەن لە بلوودیت > v2.3
</div>

## چاو لە پەرەی منداڵ بکەن (ژێرپەڕەکان)
</div>

```
<?php
	// The variable $page is an Page-Object
	if ($page->hasChildren())) {
		echo 'The page has children';
	} else {
		echo 'The page does not have children';
	}
?>
```
<div dir="rtl" >
## پێرستی تەواو ژێرپەڕەکان لە پەڕەیێک
</div>

```
<?php
	// The variable $page is an Page-Object
	$children = $page->children();

	// Each child is a Page-Object
	foreach ($children as $child) {
		echo $child->title();
	}
?>
```
<div dir="rtl" >
## چاودێری بکە گەر پەڕەیێک ژێرپەڕە بوو باوانی هەبوو
</div>

```
<?php
	// The variable $page is an Page-Object
	if ($page->isChild())) {
		echo 'The page is a child';
	} else {
		echo 'The page is not a child';
	}
?>
```
<div dir="rtl" >
## چاپکردنی  سەردێڕی پەڕەی باوان لە ژێر پەڕە
گە پەڕەێکی منداڵ بوو,دەتوانن ناوی بنن پاوان پەڕە بە مێتۆدی `parentMethod()`.
</div>

```
<?php
	// The variable $page is an Page-Object
	if ($page->isChild())) {
		echo 'Title of the parent page: ' . $page->parentMethod('title');
	} else {
		echo 'The page is not child';
	}
?>
```
<div dir="rtl" >
## جاپکردنی شریتی مێنیۆ
باوان پەڕە دەتوانێت ژێرپەڕەی هەبێ یان نە
</div>

```
<?php
	// Get the list of parent pages
	$parents = buildParentPages();

	foreach ($parents as $parent) {
		echo $parent->title();

		// Check if the page has children
		if ($parent->hasChildren()) {
			// Get the list of children
			$children = $parent->children();

			foreach ($children as $child) {
				echo " > " . $child->title();
			}
		}
	}
?>
```
</div>
