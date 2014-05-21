## SWF Reader
  
  Simple [node][nodejs] module for reading a [SWF format][swf-format].

## Installation

```sh
$ npm install swf-reader
```

## Usage

```js
var SWFReader = require('swf-reader');

SWFReader.read( 'swf_path.swf', function(err, swf) {
  console.log(swf.version);
});
``` 

## SWF Object

The SWG Object passed to the `callback` function of the `read` method has the following properties :

* `version`: The SWF version.
* `size`: The SWF size in bytes.
* `frameSize`: An Object containing the `width` and `height` of the SWF.
* `fps`: The SWF framerate.
* `frameCount`: How many frames there're in the SWF.
* `tags`: An array of `tag`. Each item in the array is an object with the folowing properties:
  * `code`: A number representing the type of the tag. (see [SWF format][swf-format] for more information)
  * `length`: The length of the tag in bytes

## Running test

To run the test, invoke the following command : 

```sh
$ npm test
```

## Todo

* Read Tags' fields 
* Write in Tags block

## Contributors

  Author: [Rafael Leal Dias][rdleal-git]

## License

MIT 

[nodejs]: www.nodejs.org
[swf-format]: http://wwwimages.adobe.com/content/dam/Adobe/en/devnet/swf/pdf/swf-file-format-spec.pdf
[rdleal-git]: https://github.com/rafaeldias
