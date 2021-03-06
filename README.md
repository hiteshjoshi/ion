# ION

ION is a distributed RTC system written by pure go and flutter

[![Financial Contributors on Open Collective](https://opencollective.com/pion-ion/all/badge.svg?label=financial+contributors)](https://opencollective.com/pion-ion) [![Build Status](https://travis-ci.com/pion/ion.svg?branch=master)](https://travis-ci.com/pion/ion)
![MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
[![slack](https://img.shields.io/badge/join-us%20on%20slack-gray.svg?longCache=true&logo=slack&colorB=brightgreen)](https://pion.ly/slack)
[![Go Report Card](https://goreportcard.com/badge/github.com/pion/ion)](https://goreportcard.com/report/github.com/pion/ion)

### Notice: Please use v0.3.0, master is not stable now


## Wiki

<img src="docs/imgs/ion.jpg" width = "10%" />https://github.com/pion/ion/wiki

## Architecture

![arch](https://github.com/pion/ion/raw/master/docs/imgs/arch.png)

## Contributor

- [adwpc](https://github.com/adwpc) - _Original Author - ion server_
- [cloudwebrtc](https://github.com/cloudwebrtc) - _Original Author - ion server and client sdk_
- [kangshaojun](https://github.com/kangshaojun) - _Contributor UI - flutter and react.js_
- [Sean-Der](https://github.com/Sean-Der) - _ion server and docker file_ 
- [sashaaro](https://github.com/sashaaro) - _docker file_
- [tarrencev](https://github.com/tarrencev) - _audio video process_

## SDK

[ion-sdk-js](https://github.com/pion/ion-sdk-js)

[ion-sdk-flutter](https://github.com/pion/ion-sdk-flutter)

## APP

[ion-app-web](https://github.com/pion/ion-app-web)

[ion-app-flutter](https://github.com/pion/ion-app-flutter)

# Screenshots

## iOS/Android

<img width="180" height="370" src="screenshots/flutter/flutter-01.jpg"/> <img width="180" height="370" src="screenshots/flutter/flutter-02.jpg"/> <img width="180" height="370" src="screenshots/flutter/flutter-03.jpg"/>

## PC/HTML5

<img width="360" height="265" src="screenshots/web/ion-01.jpg"/> <img width="360" height="265" src="screenshots/web/ion-02.jpg"/>
<img width="360" height="265" src="screenshots/web/ion-04.jpg"/> <img width="360" height="265" src="screenshots/web/ion-05.jpg"/>

## How to use

### Local Deployment
#### 1. Clone
```
git clone https://github.com/pion/ion
```

#### 2. Run
Firstly pull images. Skip this command if you want build images locally
```
docker-compose pull
```

```
docker-compose up
```

#### 3. Chat!
Open this url with chrome

```
http://localhost:8080
```

### Online Deployment

#### 1. Clone

```
git clone https://github.com/pion/ion
```

#### 2. Set Env

```
export WWW_URL=yourdomain
export ADMIN_EMAIL=yourname@yourdomain
```

#### 3. Configure docker compose

Enable production ports and Caddy file for web service in `docker-compose.yml`.

#### 4. Expose Ports

Ensure the following ports are exposed or forwarded.

```
80/tcp
443/tcp
5000-5200/udp
```

#### 5. Run

```
docker-compose up
```

#### 6. Chat!

Open this url with chrome

```
https://yourdomain
```

### Docker Tips

The provided docker-compose works for deploying to open usage, and can also be used for local development. It also supports auto-generate of certificates via LetsEncrypt.

It accepts the following enviroment variables.

* `WWW_URL` -- Public URL if auto-generating certificates
* `ADMIN_EMAIL`  -- Email if auto-generating certificates

To run on `conference.pion.ly` you would run `WWW_URL=conference.pion.ly ADMIN_EMAIL=admin@pion.ly docker-compose up`

If `WWW_URL` is set you will access via `https://yourip:8080` OR `http://yourip:8080` if not running with TLS enabled.

## Roadmap

[Projects](https://github.com/pion/ion/projects/1)
Welcome contributing to ion!