IMPORTANT!!! It is not working yet!!!!
======
pouchdb-adapter-http-jwt
======

PouchDB adapter using HTTP with JWT support (e.g. a remote CouchDB or CouchDB-like database) as its data store. Designed to run in either Node or the browser. Its adapter name is `'http'` or `'https'` depending on the protocol.

### Usage

```bash
npm install pouchdb-adapter-http-jwt
```

```js
PouchDB.plugin(require('pouchdb-adapter-http-jwt'));
var db = new PouchDB('http://127.0.0.1:5984/mydb');
```
