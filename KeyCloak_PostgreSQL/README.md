# Keycloak + MySQL

## Running
$ sudo docker-compose up

## SampleApp
- Import SampleApp/realm-import.json
- Import Client for Vanilla HTML + JS: SampleApp/vanilla-client-import.json
- Import Client for NodeJs: SampleApp/nodejs-client-import.json

### NodeJs
$ npm run install
$ npm run start

### Vanilla
$ sudo npm install http-server -g
$ http-server --port 3002