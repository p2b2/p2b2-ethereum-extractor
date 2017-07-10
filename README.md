# Data extractor

Extracts data from given database connectors.

Each connector needs at least the following exported methods:

```javascript
function connect(cb) {
	//connect to database, return callback with (null,true) if successful
	cb(null, true)
}
```

```javascript
function insert(object, cb){
    //...
    //insert object into db
    cb(null, success);
}
```

```javascript
function getLastBlock(cb){
    //check db for highest block number inserted
    //return blocknumber or -1 if nothing is inserted yet.
}
```

```javascript
function disconnect(){
    //close db connection
}
```
