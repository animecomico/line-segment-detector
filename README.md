
This is a javascript version of the famous [LSD (Line Segment Detector) algorithm](http://www.ipol.im/pub/art/2012/gjmr-lsd/). It was created using emscripten to compile the official C version into javascript and adding a bit of wrapper code to convert between javascript and C data types.

Currently only the main lsd() function call is available.

# Usage

See example.js

# Compiling

You don't need to compile this unless you change the C code. Just use the pre-compiled index.js and index.*.js files.

First install emscripten. On a Ubuntu 14.04 the following should work:

```
sudo apt-get install emscripten
```

On Ubuntu 16.04 there appears to be an issue with emscripten. You'll need to build emscripten using emsdk:

```
sudo apt-get install cmake build-essential git
wget "https://s3.amazonaws.com/mozilla-games/emscripten/releases/emsdk-portable.tar.gz"
tar cvzf emsdk-portable.tar.gz
cd emsdk-portable/
./emsdk update
./emsdk install latest
./emsdk activate latest
source ./emsdk_env.sh
```

Now get the lsd source code:

```
cd line-segment-detector/
wget "http://www.ipol.im/pub/art/2012/gjmr-lsd/lsd_1.6.zip"
unzip lsd_1.6.zip
```

To build:

```
./build.sh
```

# License

License is AGPLv3