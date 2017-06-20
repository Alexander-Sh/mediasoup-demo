# mediasoup-demo-server


## Installation

* Clone the project:

```bash
$ git clone https://github.com/nat-mobile/mediasoup-demo
$ cd mediasoup-demo
```

* Set up the server:

```bash
$ npm install
```


```

* Globally install `gulp-cli` NPM module (may need `sudo`):

```bash
$ npm install -g gulp-cli
```


## Run it locally

* Run the Node.js server application in a terminal:

```bash
$ cd server
$ node server.js
```


* Upload the entire `server` folder to your server and make your web server (Apache, Nginx...) expose the `server/public` folder.

* Edit your `server/config.js` with appropriate settings (listening IP/port, logging options, **valid** TLS certificate, etc). Also set the proper remote WebSocket port in `client/config.js`.

* Within your server, run the server side Node.js application. We recommend using the [forever](https://www.npmjs.com/package/forever) NPM daemon launcher, but any other can be used:

```bash
$ forever start PATH_TO_SERVER_FOLDER/server.js
```
