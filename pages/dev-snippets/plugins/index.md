<div dir="rtl" >

# زیادکراوەکان
<!-- position: 10 -->

پارچەکۆدێک دەربارەی زیادکراوەکان

## زیادکراوەی چالاک
</div>

```
<?php
	// Class name of the plugin
	$className = 'pluginAbout';

	activatePlugin($className);
?>
```
<div dir="rtl" >
	
## زیادکراوەی ناچالاک
</div>

```
<?php
	// Class name of the plugin
	$className = 'pluginAbout';

	deactivatePlugin($className);
?>
```
<div dir="rtl" >
## چاودێری بکە گەر زیادکراوەیێک چالاک بوو
</div>

```
<?php
	// Class name of the plugin
	$className = 'pluginAbout';

	if (pluginActivated($className)) {
		echo 'The plugin About is activated';
	} else {
		echo 'The plugin About is deactivated';
	}
?>
```

<div dir="rtl" >

## وەرگرتنی زیادکراوە
ئەم فۆنکشێنە دەگەڕێنێتەوە [ئانجێکتی زیادکراوە](https://github.com/bludit/bludit/blob/master/bl-kernel/abstract/plugin.class.php).

ئەم زیادکراوە پێویستی بە چالاکبوون هەیە, هەرچەند کە `getPlugin()` بۆ گەڕانەوەی ئەم فۆنکشێنە دەبێ `false`.
</div>

```
<?php
	// Class name of the plugin
	$className = 'pluginAbout';

	// Get the Plugin-Object
	$plugin = getPlugin($className);

	// Print the plugin label
	echo $plugin->label();

	// Execute the hook siteSidebar of the plugin and print it
	echo $plugin->siteSidebar();
?>
```
