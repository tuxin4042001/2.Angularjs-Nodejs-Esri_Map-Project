# Appropolis Map


## Description

Appropolis Map is an Angular 1.x APP which is built with [ESRI API 4.4](https://developers.arcgis.com/javascript/latest/api-reference/index.html) for 3D view and [Leaflet](https://esri.github.io/esri-leaflet/api-reference/) for 2D view.
This Map application is used to visualize spatial information for users' hardware devices, also provides dashboard that allows users to _**register/edit/delete/view**_ their own devices.

## System requirement
You can use Appropolis 3D map application in desktop web browsers that support WebGL, a web technology standard for rendering 3D graphics. In addition, your hardware must have a graphics card installed that supports WebGL. Make sure your graphics card has the latest drivers installed and has at least 512 MB of video memory. Your computer hardware needs to have a minimum of 2 GB system memory and 4GB recommended. For best performance, it is recommended that you use the latest versions of Chrome or Firefox and that your graphics card have 1 GB or more of video memory. Appropolis 3D map application is not supported on mobile devices.

Appropolis 3D map application should support the following web browsers (not fully test on all):

Chrome (requires webGL 2)
Firefox
Internet Explorer 11*
Edge*
Safari 9 and later*

Use the link below to test the webGL version supported by your system.
http://webglreport.com/

## Development Setup

1. Clone [this repo](http://207.34.103.155:57990/projects/FRON/repos/map_esri/browse) into your laptop.
2. Go to downloaded folder, run `npm install`
3. Run tests before start developing, run `gulp test` or `npm test`, make sure all passed, otherwise find out who breaks the tests and let him/her fix it.
4. Run `gulp start` or `npm start` to start local server, the server will keep watching files changes and reload page.
5. Please write tests when you create any complex logic and make sure tests are passed before pushing code.

**dev/test config will be applied for running `gulp` or `npm start`, if you want to use prod config, please run `npm run start:prod`**

## Testing

-  Run `npm start` to start local dev environment and do some manual UI testing.
-  Add tests when logic is a bit complex or contains `if-else`, `for`, `while` and etc.
-  Run `npm test` to verify functions are working.

## Dependencies
Now this project is depending on **[WEB API](http://10.10.10.6:7990/projects/BCK/repos/nodejs/browse/webapi)**
and **GeoServer**. We call WEB API node server as it's built based on nodejs, and it will provide realtime data, up-to-date spatial info and user account info. For GeoServer, it will provide both 2D & 3D Map Layer info, e.g. graphic locations, 3D modeling, labels and etc.

Dependencies:

```
Angular 1.6.x
Bootstrap 3.3.7
ESRI MAP 4.4
JQuery 3.2.1
ESRI Leaflet 1.0.3
```

Tests dependencies: 

```
Karma as test runner
Mocha + Chai + Sinon as testing framework
```

## Environments

Calgary: 

| Environment | Server Address | Private URL | Public URL |
| ------------- |:-------------:| -----:|-----:|
| Test      | `10.10.10.9` | http://10.10.10.9:9001 | http://207.34.103.154:9001 |
| Prod      | `10.10.10.8` | http://10.10.10.8:9002 | http://207.34.103.154:9002 |

Shanghai:

| Environment | Server Address | Private URL | Public URL|
| ------------- |:-------------:| -----:| -----:|
| Prod      | `180.169.137.162` | http://192.168.100.100:9002 | http://180.169.137.162:9002|

*shanghai.appropolis.com is resolved to `180.169.137.162`, which is public IP for `192.168.100.100`*
*calgary.appropolis.net is resolved to `207.34.103.154`*


## Deployment & Release

Please see `deployment-notes.md` in `docs/` folder.

## Author
- Appropolis Frontend Team


## Known Issues

* streetlampLayer undefined error.
* Hard code in `hook.js` to only allow users whose email is `shanghai_dashboard@appropolis.com` to access Dashboard page.
* *For demo, when encountering loraAppId with `9999`, create dummy data for corresponding layer services.*
