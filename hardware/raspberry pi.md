---
is: "[[hardware]]"
---
# Notes
Raspberry Pi

SD Cards
* make sure to format as FAT. Win8 doesn’t support it any more (but possibly with diskpart). Used Kali

nRF24L01+
RF24 Library - https://github.com/tmrh20/RF24 doesn’t work on Pi2, but works on Pi B+ Connecting - http://blog.carr3r.com/post/raspberry-pi-b-and-arduino-talking-through-nrf24l01-modules/

Camera motion detection
http://www.richardmudhar.com/blog/2015/02/raspberry-pi-camera-and-motion-out-of-the-box-sparrowcam/

# Raspberry Pi Temperature Sensor

[Raspberry Pi Humidity Sensor using the DHT22 - Pi My Life Up](https://pimylifeup.com/raspberry-pi-humidity-sensor-dht22/)

## Notes
* Using Raspberry Pi Zero W
* Started with 
* Wireless enabled
* System updated
* alias python=‘/usr/bin/python3’

## Homekit
* https://nodejs.org/dist/latest-v9.x/node-v9.11.2-linux-armv6l.tar.gz
	* [Install Node.js on a Raspberry Pi - DEV Community 👩‍💻👨‍💻](https://dev.to/vorillaz/install-nodejs-on-a-raspberry-pi-4hd5)
* [GitHub - nfarina/homebridge: HomeKit support for the impatient](https://github.com/nfarina/homebridge)
* sudo npm install -g homebridge-dht
	* [homebridge-dht  -  npm](https://www.npmjs.com/package/homebridge-dht)
* node-dht-sensor
	* issue installing
	* new thing
```
*pi@raspberrypi*:*~/.homebridge $* sudo npm install -g node-dht-sensor

> node-dht-sensor@0.3.0 install /usr/local/lib/node_modules/node-dht-sensor
> node-gyp configure

gyp WARN EACCES user “root” does not have permission to access the dev dir “/root/.node-gyp/9.11.2”
gyp WARN EACCES attempting to reinstall using temporary dev dir “/usr/local/lib/node_modules/node-dht-sensor/.node-gyp”
```
	* add “—unsafe-perm” option
