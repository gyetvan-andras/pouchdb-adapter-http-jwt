pouchdb-adapter-http-jwt
======

PouchDB adapter using HTTP with [JSON Web Token](https://jwt.io) support (e.g. a remote CouchDB or CouchDB-like database with JWT authorization) as its data store. 

It is forked from the original ```pouchdb-adapter-http```

Tested against [express-jwt-pouchdb](https://github.com/tyler-johnson/express-jwt-pouchdb)
### Usage

```bash
npm i https://github.com/gyetvan-andras/pouchdb-adapter-http-jwt.git
```

```js
var PouchDB = require('pouchdb-core')
  .plugin(require('pouchdb-adapter-http-jwt'))
  .plugin(require('pouchdb-mapreduce'))
  .plugin(require('pouchdb-replication'));

const _token = () => {
    return 'my secret token'
}

var db = new PouchDB('http://127.0.0.1:5984/mydb',{jwtauth: {token:_token}})
db.allDocs().then((res) => {
    res.rows.forEach((row) => {
        console.log(row)
    })
}).catch((err) => {
    console.log('Error', err)
})

```
