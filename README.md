# docker-iobroker-rpi
Docker image for ioBroker (http://iobroker.net) based on resin/rpi-raspbian for Raspberry Pi (http://hub.docker.com/_/debian/)

This project creates a Docker image for running ioBroker in a Docker container. It is made for and tested on a Raspberry Pi 3b with Docker CE and YAHM. But it should also work on other systems with Docker!<br>
Cause the container ist based on resin/rpi-raspbian, it acts nearly like a full virtual machine. That makes it possible to easily add some additional dependies for some ioBroker-Adapters.

## Installation & Usage

For installing Docker on a Raspberry Pi 3b (recommended becaus the RAM is needet!) please refere here: https://docs.docker.com/install/linux/docker-ce/debian/#set-up-the-repository

The just download the repository and run: 



```
docker build -t iobroker . 
docker run -p 8081:8081 iobroker
```

This could take a while!


## Changelog

### v1.0
Forked from buanet, initial commit. Still under development!

## License

MIT License

Copyright (c) 2017 Andre Germann

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Credits

Inspired by and forked from https://github.com/buanet/docker-iobroker

