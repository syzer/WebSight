# TODO
- [X] what went wrong: don't work on the mobile iphone/android.

# WAT
WebSight demonstrates a comparison of performance between JavaScript, <a href="http://asmjs.org/">asm.js</a>, and <a href="http://webassembly.org/">WebAssembly</a>. A user uploaded static image or live video is displayed for each target. Performance is measured by the length of time it takes to detect face(s) or eyes in the image or video.

Each target is run in its own <a href="https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API">web worker</a>. The popular open source computer vision library, <a href="http://opencv.org/">OpenCV</a>, was compiled using <a href="http://kripken.github.io/emscripten-site/">Emscripten</a> to asm.js and wasm (WebAssembly module) to utilize the <a href="https://en.wikipedia.org/wiki/Viola%E2%80%93Jones_object_detection_framework">Viola-Jones algorithm</a> for object detection. <a href="https://github.com/foo123/HAAR.js">HAAR.js</a> was modified to remove the DOM manipulation, so it could be used in the JavaScript web worker.

The demo is accessible from http://websightjs.com.

Thanks to <a href="https://github.com/shamadee/web-dsp">WebDSP</a> for the inspiration, and to <a href="https://github.com/ucisysarch/opencvjs">uscisysarch</a>, <a href="https://github.com/njor/opencvjs">njor</a>, and <a href="https://github.com/foo123/HAAR.js">foo123</a> for giving us a starting point.

Contributors to this project are <a href="https://github.com/BrianJFeldman">BrianJFeldman</a>, <a href="https://github.com/DebraD">DebraD</a>, <a href="https://github.com/MarkGeeRomano">MarkGeeRomano</a> and <a href="https://github.com/YervantB">YervantB</a>.
