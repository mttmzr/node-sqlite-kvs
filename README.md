# node-sqlite-kvs
Key-Value Store for Node.js using SQLite3, forked from [kujirahand/node-sqlite-kvs](https://github.com/kujirahand/node-sqlite-kvs)

# install

```shell
$ npm install sqlite-kvs
```

# example

```js
const KVS = require('sqlite-kvs');

//
// create
const db = new KVS();

try{
  //
  // open
  await db.open(':memory:');

  //
  // put and get
  await db.put("neko", "nya-");
  const result = await db.get("neko");
  console.log("neko is", result);

}catch(err) {
  console.log(err);
}
```

# api

## await db.open(path)

open database

## await db.get(key)

get value from key.

## await db.has(key)

check if has key.

## await db.put(key, value)

put value to key.

## await db.delete(key)

delete key.

## await db.purge(prefix)

delete all keys with prefix.

## await db.all()

get all values.

## await db.find(prefix)

find values.










