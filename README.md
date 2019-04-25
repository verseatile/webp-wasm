# webp-wasm
encoding a webp image with wasm

## GUIDE
Read the tutorial from Google, here: https://developers.google.com/web/updates/2018/03/emscripting-a-c-library

## BUILD
- Make sure you have emcc (Emscripten) installed
- grab libwebp from https://github.com/webmproject/libwebp and place it inside of this directory
- compile with ```emcc -O3 -s WASM=1 -s ASSERTIONS=1 -s EXTRA_EXPORTED_RUNTIME_METHODS='["cwrap"]'     -I libwebp     webp.c     libwebp/src/{dec,dsp,demux,enc,mux,utils}/*.c```
