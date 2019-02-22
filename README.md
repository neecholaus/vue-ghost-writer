# Vue Ghost Writer Component
VueJS component for a configurable ghost writer.
## Features:
* Custom phrases
* Optional prefix and suffix
* Option to add CSS classes to the full line or to the phrase
## Properties
* phrases
	- Description: Array of phrases that will be typed repeatedly typed out.
	- Type: **Array\<String\>**
	- Required: **True**
* prefix
	- Description: Text to be displayed after the phrase.
	- Type: **String**
	- Required: **False**
* suffix
	- Description: Text to be displayed after the phrase.
	- Type: **String**
	- Required: **False**
* classes
	- Description: One or more CSS classes that can be applied to the full line element.
	- Type: **String**
	- Required: **False**
* phraseClasses
	- Description: Same as classes, but only applies to the phrase text.
	- Type: **String**
	- Required: **False**
