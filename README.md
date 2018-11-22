# docker-iobroker-rpi
Docker image for ioBroker (http://iobroker.net) based on resin/rpi-raspbian for Raspberry Pi (https://hub.docker.com/r/resin/rpi-raspbian/) Its tested an a Raspberry PI 3b with YAHM and openHAB running anlong with it.

## Installation & Usage

For installing Docker on a Raspberry Pi 3b please refere to: https://docs.docker.com/install/linux/docker-ce/debian/#set-up-the-repository

The just download the repository and run: 

```
docker build -t iobroker . 

```

to build the Image - this could take a while!

To start the image run:

```
docker run -p 8081:8081 iobroker
```

For producational use I would recommend to run it with docker-compose.

To install docker-compose refere to https://docs.docker.com/compose/install/

To deploy it you can use the following docker-compose.yml file

```
version: '3'
services:
	iobroker:
		build: .
		ports: 
		 - "8081:8081"
		 - "8082:8082"
		 - "8083:8083"
		 - "8084:8084"
```


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

