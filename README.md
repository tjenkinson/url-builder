[![npm version](https://badge.fury.io/js/url-toolkit.svg)](https://badge.fury.io/js/url-toolkit)
[![Build Status](https://travis-ci.org/tjenkinson/url-toolkit.svg?branch=master)](https://travis-ci.org/tjenkinson/url-toolkit)

# URL Toolkit
Lightweight library to build an absolute URL from a base URL and a relative URL. Initially part of [HLS.JS](https://github.com/dailymotion/hls.js).

## Example
```javascript
var URLToolkit = require('url-toolkit');
var url = URLToolkit.buildAbsoluteURL('https://a.com/b/cd/e.m3u8?test=1#something', '../z.ts?abc=1#test');
console.log(url); // 'https://a.com/b/z.ts?abc=1#test'
```

## Browser
This can also be used in the browser thanks to [jsDelivr](https://github.com/jsdelivr/jsdelivr):
```html
<head>
  <script type="text/javascript" src="https://cdn.jsdelivr.net/url-toolkit/latest/url-toolkit.js"></script>
  <script type="text/javascript">
    var url = URLToolkit.buildAbsoluteURL('https://a.com/b/cd/e.m3u8?test=1#something', '../z.ts?abc=1#test');
    console.log(url); // 'https://a.com/b/z.ts?abc=1#test'
  </script>
</head>
```
