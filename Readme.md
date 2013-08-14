
# jszip

A library for creating, reading and editing .zip files with Javascript, with a lovely and simple API.

See http://stuartk.com/jszip for all the documentation

Modified for use as a component module.

## Installation

  Install with [component(1)](http://component.io):

    $ component install chemzqm/jszip

## Usage

``` js
var JSZip = require('jszip');
var zip = new JSZip();

zip.file("Hello.txt", "Hello World\n");

var img = zip.folder("images");
img.file("smile.gif", imgData, {base64: true});

var content = zip.generate();

location.href = "data:application/zip;base64," + content;
/*
Results in a zip containing
Hello.txt
images/
    smile.gif
*/
```
## License

  MIT
