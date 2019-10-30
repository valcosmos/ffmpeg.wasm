<p align="center">
  <a href="#">
    <img alt="ffmpeg.js" width="128px" height="128px" src="https://github.com/ffmpegjs/ffmpeg.js/raw/master/docs/images/ffmpegjs-icon.png">
  </a>
</p>

# ffmpeg.js

[![Actions Status](https://github.com/ffmpegjs/ffmpeg.js/workflows/CI/badge.svg)](https://github.com/ffmpegjs/ffmpeg.js/actions)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/ffmpegjs/ffmpeg.js/graphs/commit-activity)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Code Style](https://badgen.net/badge/code%20style/airbnb/ff5a5f?icon=airbnb)](https://github.com/airbnb/javascript)
[![Downloads Total](https://img.shields.io/npm/dt/@ffmpeg/ffmpeg.svg)](https://www.npmjs.com/package/@ffmpeg/ffmpeg)
[![Downloads Month](https://img.shields.io/npm/dm/@ffmpeg/ffmpeg.svg)](https://www.npmjs.com/package/@ffmpeg/ffmpeg)

Use FFmpeg directly in your browser without any backend services!!

**Transcode**

<p align="center">
  <a href="#">
    <img alt="transcode-demo" src="https://github.com/ffmpegjs/ffmpeg.js/raw/master/docs/images/transcode.gif">
  </a>
</p>

<a href="https://codepen.io/jeromewu/pen/NWWaMeY">
  <img alt="codepen" width="128px" src="https://blog.codepen.io/wp-content/uploads/2012/06/codepen-wordmark-display-inside-black@10x.png">
</a>

ffmpeg.js provides simple to use APIs, to transcode a video you only need few lines of code:

```javascript
const fs = require('fs');
const { createWorker } = require('@ffmpeg/ffmpeg');

const worker = createWorker();

(async () => {
  await worker.load();
  const { data } = await worker.transcode('./test.avi', 'mp4');
  fs.wrieFileSync('./test.mp4', data);
})();
```
---

## Installation

```
$ npm install @ffmpeg/ffmpeg
```

## Documentation

WIP

## Tutorials

Learn how to build ffmpeg.js from stories:

- [Part.1 Preparation](https://itnext.io/build-ffmpeg-webassembly-version-ffmpeg-js-part-1-preparation-ed12bf4c8fac)
- [Part.2 Compile with Emscripten](https://itnext.io/build-ffmpeg-webassembly-version-ffmpeg-js-part-2-compile-with-emscripten-4c581e8c9a16)
- [Part.3 ffmpeg.js v0.1.0 — Transcoding avi to mp4](https://itnext.io/build-ffmpeg-webassembly-version-ffmpeg-js-part-3-ffmpeg-js-v0-1-0-transcoding-avi-to-mp4-f729e503a397)