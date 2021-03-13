# Detect-File-Encoding-and-Language
An NPM package that detects the encoding and language of a file.

* Detects 34 languages and the appropriate encoding
* Works best with large inputs
* Completely free, no API key required

For reliable encoding and language detection inputs of 500 words or more are recommended. Smaller inputs can work as well but the results will be less accurate and in some cases incorrect. 

## Installation

`npm install detect-file-encoding-and-language`

## Example

```html
index.html

<input type="file" id="input" >

```

```javascript
app.js

const languageEncoding = require("detect-file-encoding-and-language");

document.getElementById("input").addEventListener("change", inputHandler)

function inputHandler(e) {
    const file = e.target.files[0];

    languageEncoding(file).then(fileInfo => console.log(fileInfo));   // { language: English, encoding: UTF-8, confidence: 1}
}

```