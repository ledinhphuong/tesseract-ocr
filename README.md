[![view on npm](http://img.shields.io/npm/v/tesseractocr.svg?style=flat-square)](https://www.npmjs.com/package/tesseractocr)
[![downloads per month](http://img.shields.io/npm/dm/tesseractocr.svg?style=flat-square)](https://www.npmjs.com/package/tesseractocr)
[![node version](https://img.shields.io/badge/node-%3E=4-brightgreen.svg?style=flat-square)](https://nodejs.org/download)
[![build status](https://img.shields.io/travis/schwarzkopfb/tesseractocr.svg?style=flat-square)](https://travis-ci.org/schwarzkopfb/tesseractocr)
[![test coverage](https://img.shields.io/coveralls/schwarzkopfb/tesseractocr.svg?style=flat-square)](https://coveralls.io/github/schwarzkopfb/tesseractocr)
[![license](https://img.shields.io/npm/l/tesseractocr.svg?style=flat-square)](https://github.com/schwarzkopfb/tesseractocr/blob/master/LICENSE)

# Tesseract OCR for Node.js

Simple and modern Node.js wrapper implementation for Tesseract OCR CLI.

## Features & Advantages

- focus on high performance
- both promise and callback APIs are supported
- full test coverage
- void of sync operations
- no temp files are used

## Usage

```js
const recognize = require('tesseractocr')

recognize(`${__dirname}/image.png`, (err, text) => {
    if (err)
        throw err
    else
        console.log('Yay! Text recognized!', text)
})

```

## Complete API docs

__TODO__

## Installation

There is a hard dependency on the [Tesseract project](https://github.com/tesseract-ocr/tesseract).  You can find installation instructions for various platforms on the project site. For Homebrew users, the installation is quick and easy.

    brew install tesseract --with-all-languages

The above will install all of the language packages available, if you don't need them all you can remove the `--all-languages` flag and install them manually, by downloading them to your local machine and then exposing the `TESSDATA_PREFIX` variable into your path:

    export TESSDATA_PREFIX=~/Downloads/

You can then go about installing the Node.js package to expose the JavaScript API:

    npm install tesseractocr

## Tests and benchmarks

Clone the repo, `npm install` and then `npm test` or `npm run benchmarks`.

## License

[MIT](/LICENSE)