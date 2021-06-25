speedtest
=========

Simple bandwidth test in browser javascript.

- [Example](#example)
- [Installation](#installation)
- [Note on testing](#note-on-testing)
- [Unlicense](#unlicense)
- [Author](#author)


Example
-------

<https://fvdm.com/speedtest/>

You can change the number precision up to 3 decimals using the arrow
keys on your keyboard.


Installation
------------

Just clone the repo:

```sh
git clone https://github.com/fvdm/speedtest
```

To keep the repository small I have not included the test binaries.
You can download them from my server.

**Please don't hotlink these!!**

* [1mb.bin](https://fvdm.com/speedtest/1mb.bin)
* [5mb.bin](https://fvdm.com/speedtest/5mb.bin)
* [10mb.bin](https://fvdm.com/speedtest/10mb.bin)
* [100mb.bin](https://fvdm.com/speedtest/100mb.bin)

Or instantly generate them yourself: (faster)

```sh
# on linux
fallocate -l 1m 1mb.bin
fallocate -l 5m 5mb.bin
fallocate -l 10m 10mb.bin
fallocate -l 100m 100mb.bin
fallocate -l 1000m 1000mb.bin

# on macOS
mkfile -n 1m 1mb.bin
mkfile -n 5m 5mb.bin
mkfile -n 10m 10mb.bin
mkfile -n 100m 100mb.bin
mkfile -n 1000m 1000mb.bin
```

These commands only create the files in the filesystem.
No bytes are actually written to the storage.
The suffix `m` is megabytes and `g` is gigabytes and so on.


Note on testing
---------------

With these kind of tools you are testing the available bandwidth of
the slowest connection between your device and the host. When your web
server connection is slower than your own network, you are actually
testing the server's bandwidth instead of your own.

There can be many causes for slow connections, like the type of wiring,
other devices, interference, packetloss or the peering between network
providers somewhere along the route.

For example, I tested this speedtest from my own server to my home
network both connected from Amsterdam and I got only 70 Mbit but using
my provider's speedtest I get double at least. Doing the same to my
LiquidSky box in Frankfurt I easily get over 900 Mbit. So there is a
bottleneck somewhere between the web server and my home ISP.


Unlicense
---------

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <https://unlicense.org/>


Author
------

[Franklin van de Meent](https://fra.nkl.in)

Do you like this project?
Please consider to [buy me a coffee](https://ko-fi.com/franklin).
Please consider to [buy me a coffee](https://fvdm.com/donating/).
