# Speedtest

Simple down/upload bandwidth test in browser javascript.

It has a simple interface with only the essentials.
There are no dependencies other than the binary files.
It doesn't even require a backend language such as PHP
and runs great on static hosting.

You simply upload the `index.html` file and generate
the binary testing files. The number precision can be
changed up to 3 decimals using the arrow keys on your
keyboard.

- [Example](#example)
- [Installation](#installation)
- [Note on testing](#note-on-testing)
- [Unlicense](#unlicense)
- [Author](#author)


## Installation

Just clone the repo:

```sh
git clone https://github.com/fvdm/speedtest
```

Or download the [`index.html`](https://raw.githubusercontent.com/fvdm/speedtest/master/index.html) file:

```sh
wget https://raw.githubusercontent.com/fvdm/speedtest/master/index.html
```


### Binary files

To keep the repository small I have not included the test binaries.

You can instantly generate them yourself:

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

# on Windows
# Open the Command Prompt as Administrator
fsutil file createnew 1mb.bin 1000000
fsutil file createnew 5mb.bin 5000000
fsutil file createnew 10mb.bin 10000000
fsutil file createnew 100mb.bin 100000000
fsutil file createnew 1000mb.bin 1000000000

# others like Synology
dd if=/dev/zero of=1mb.bin bs=1 count=0 seek=1M
dd if=/dev/zero of=5mb.bin bs=1 count=0 seek=5M
dd if=/dev/zero of=10mb.bin bs=1 count=0 seek=10M
dd if=/dev/zero of=100mb.bin bs=1 count=0 seek=100M
dd if=/dev/zero of=1000mb.bin bs=1 count=0 seek=1000M
```

These commands only create the files in the filesystem.
No bytes are actually written to the storage.
The suffix `m` is megabytes and `g` is gigabytes and so on.


## Note on testing

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

The speedtest is at its best when the connection is as
short as possible. For example, on your NAS or RPi to
check on your LAN bandwidth.


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

[Franklin](https://fvdm.com)

Do you like this project?
Please consider to [buy me a coffee](https://fvdm.com/donating/).
