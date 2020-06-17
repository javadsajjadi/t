<div dir="rtl">

# سڕینەوەی پەڕەیێک
<!-- position: 6 -->

سڕینەوەی پەڕەیێک.

تەواو داواکان پێویستیان بە APIهەیە هەروا نیازیان بە `API Token`. ئێوە دەتوانن تۆکن پەیدا بکەن لە API پەڕەی رێکخستنی زیادکراوەی.
</div>

```bash
Admin panel > Plugins > API > API Token
```

<div dir="rtl">
بۆ تەواو داواکانی API بۆ نووسینی ناوەڕۆک, ئێوە دەبێ نیشانی بدەن `Authentication Token`. بۆ وەرگرتنی تۆکن,ئێوە پێویستان بە بەکارهێنەرێک بە ڕۆڵێ `Administrator` هەیە. ئەم ڕۆڵە واتە `Authentication Token` لە پرۆفایلی بەکارهێنەر وەربگرن
</div>

```bash
Admin panel > Manage > Users > {Username} > Security > Authentication Token
```
<div dir="rtl">
<h2 id="request">HTTP وڵامی</h2>
</div>

```bash
DELETE /api/pages/{key}
```

<div dir="rtl">
<h2 id="parameters">پارامەتر</h2>

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token. | |
| `required` authentication | `string` Authentication token. | |

<h2 id="response">وڵام</h2>
</div>

```bash
HTTP Code: 200
Content-Type: application/json
Body:
{
	"status": "0",
	"message": "Page deleted."
}
```

<div dir="rtl">
<h2 id="curl-example">CURLنمونە فەرمانی</h2>
بۆ نمونە فەرمانی curl نیشانی دەدا سڕینەوەی پەڕەیێک بە کلیلی `my-dog`.
</div>

```bash
$ curl  -X DELETE \
	--data "token=24a8857ed78a8c89a91c99afd503afa7" \
	--data "authentication=193569a9d341624e967486efb3d36d75" \
	-H "Content-Type: application/json" \
	"https://www.example.com/api/pages/my-dog"
```

<div dir="rtl">
جەستەی وڵام
</div>

```bash
{
	"status": "0",
	"message": "Page deleted.",
	"data": {
		"key": "my-dog"
	}
}
```
