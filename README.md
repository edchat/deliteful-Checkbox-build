# deliteful-Checkbox-build

Build version of [ibm-js/deliteful/Checkbox](https://github.com/ibm-js/deliteful/Checkbox).

## Status

No official release yet.

## Installation

_Bower_ release installation:

    $ bower install "https://github.com/edchat/deliteful-Checkbox-build.git"

In the future (after it is published) it will be:

    $ bower install deliteful-Checkbox-build


## How to use

To load the minified layer you have two options, you can include the layer with a script tag, or you can wrap your main `require`
call with another `require`, requiring `"deliteful-Checkbox-build/layer"`. Then you should continue to refer to modules
with `"deliteful/Checkbox"`.

For example, to wrap the main require with another require, this code:
```js
require(["app/main", "deliteful/Checkbox"], function() {
	...
});
```
Becomes:
```js
require(["deliteful-Checkbox-build/layer"], function() {
	require(["app/main", "deliteful/Checkbox"], function() {
		...
	});
});
```

Or you can load the "deliteful-Checkbox-build/layer" with a script tag, and without the extra require for `"deliteful-Checkbox-build/layer"`
```
<script src="bower_components/deliteful-Checkbox-build/layer.js"></script>
```

Then to use the Checkbox widget with a declarative instantiation, add this to your html:
```
  <label>
    <d-checkbox name="option1" checked="true"></d-checkbox>
    Option 1
  </label>
  <label>
    <d-checkbox name="option2"></d-checkbox>
    Option 2
  </label>
  <label>
    <d-checkbox disabled="true" name="option3"></d-checkbox>
    Option 3
  </label>
```
See [`deliteful/Checkbox`](https://github.com/ibm-js/deliteful/blob/master/docs/Checkbox.md) for full details on how instantiate a Checkbox widget.

## Licensing

This project is distributed by the Dojo Foundation and licensed under the ["New" BSD License](./LICENSE).
All contributions require a [Dojo Foundation CLA](http://dojofoundation.org/about/claForm).
