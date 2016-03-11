Select with options

import: <link rel="import" href="components/select-fix.html">



#Select with options

There is a known limitation with Polymer (more specifically with template tags) using dom-repeats inside of ```<select>``` tags in Internet Explorer. This is called out in Polymer's issue [#1735](https://github.com/Polymer/polymer/issues/1735)

 This component works around this issue without the need for much rework.


## Quick start

Several quick start options are available:

* [Download the latest release](https://github.com/vehikl/polymer-select-with-options/archive/master.zip).
* Clone the repo: `git clone https://github.com/vehikl/polymer-select-with-options.git`.
* Install with [Bower](http://bower.io): `bower install polymer-select-with-options`.

### What's included

Within the download you'll find the following directories and files, logically grouping common assets and providing both compiled and minified variations. You'll see something like this:

```
├── README.md
├── bower.json
├── demo.html
├── polymer-micro.html
├── polymer-mini.html
├── polymer.html
└── select-with-options.html
```

For an existing polymer project only the select-with-option.html file is required to be imported. The remaining html files are for use in the demo.html file.

## Usage

Import select-with-options.html into your project;
```
<link rel="import" href="select-with-options.html">
```



```
<select is="select-with-options" options="{{options}}" value="{{value::change}}"></select>
```

```
<select is="select-with-options" options="{{options}}" option-value="id" option-label="name" value="{{value::change}}"></select>
```

```
<select is="select-with-options" options="{{options}}" option-value="id" option-label="name" value="{{value::change}}">
    <option value="hardcoded_option">Hardcoded Option</option>
</select>
```

## Dependencies

If you are not using a pre-compiler, you will need to wrap your Polymer objects in an event listener for WebComponentsReady as outlined in the WebComponents.js documentation:

[http://webcomponents.org/polyfills/html-imports/](http://webcomponents.org/polyfills/html-imports/)

You can see an example of this in demo.html-imports

```
window.addEventListener('WebComponentsReady', function(e) {
    new Polymer({
        is: 'demo-1',
        properties: {
            value : {
                type: String,
                value: 'three'
            },
            options: {
                value: [
                    'one',
                    'two',
                    'three'
                ]
            }
        }
    });
});
```
