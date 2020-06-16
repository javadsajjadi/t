<div dir="rtl">

# لەپێش ناساندنی گۆڕاوەکان
<!-- position: 3 -->

بلوودیت چەندین گۆڕاوەی لە پێش ناساندووە بۆ پەڕەپێدەران

<h2 id="content">$content</h2>

گۆڕاوەی `$content`  کە  array ناسراوە بۆ تەواو پەڕەکان (بریتییەلە `pages` وە `sticky`, بەڵام بریتی نییە لە پەڕەکانی `statics`). هەر پەڕەیێک بریتییە لە  array کە لەم بەستەرە [Page Object](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php)زانیاری هەس.

ئارایەکان ریز دەکرێن لەگەڵ `date` وەیا `position`, کە ئێوە دەتوانن بیانگۆڕن لە بەشی رێکخستنی ماڵپەڕ

دەتوانن بۆ زانیاری فرەتر ئەم بەستەرە لە خوارەوە چاولێبکەن
- https://docs.bludit.com/en/dev-snippets/content-pages

<h2 id="staticContent">$staticContent</h2>

گۆڕاوەی `$staticContent`  دەتوانێت array بۆ تەواو پەڕەکانی `static` بێت. هەر پەڕەیێک لەم بەشە بریتییە لە ئارایەیێک لە [Page Object](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php).

ئارایەکان بریتین لە شوێنێک `position` بۆ دیزاین کردن

دەتوانن بۆ زانیاری فرەتر سەردانی ئەم بەستەرە لە گۆڕاوەکان بکەن
- https://docs.bludit.com/en/dev-snippets/content-static

<h2 id="page">$page</h2>

گۆڕاوەی `$page` نوینەری هەپەڕەیێکە کە بەکارهێنەر بۆی دەگەڕێ. ئەم گۆڕاوە هەیە لە [Page Object](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php).

بۆ نمونە گەر بەکارهێنەر لە ناونیشانی `https://www.example.com/my-dog-rules`,  `$page` گۆڕاوە دەتوانێت وەک کلیلێک کردار بکات, e.g. `my-dog-rules`.

<h2 id="pages">$pages</h2>

 `$pages` گۆڕاوەی هەیە لە [Pages Object](https://github.com/bludit/bludit/blob/master/bl-kernel/pages.class.php). ئەم گۆڕاوە دەتوانێت ئابجێکتیک بێت لە بنکە دراوە ناوەرۆک

<h2 id="tags">$tags</h2>

گۆڕاوەی `$tags` هەیە وەک [Tags Object](https://github.com/bludit/bludit/blob/master/bl-kernel/tags.class.php). دەتوانێت وە بنکەی تاگەکان سوودی لێبگیرن

<h2 id="categories">$categories</h2>

گۆڕاوەی `$categories`هەیە لە [Categories Object](https://github.com/bludit/bludit/blob/master/bl-kernel/categories.class.php). ئەم ئابجێکتە دەتوانن دەستکاری بکەن لە هاوپۆلەکانی زانیاری

</div>
