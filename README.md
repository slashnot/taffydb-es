# taffydb-es
TaffyDB packed as ESM Module

## Usage
```sh
import {taffy  as  TAFFY} from  'taffydb-es'

const friends = TAFFY([
	{"id":1,"gender":"M","first":"John","last":"Smith","city":"Seattle, WA","status":"Active"},
	{"id":2,"gender":"F","first":"Kelly","last":"Ruth","city":"Dallas, TX","status":"Active"},
	{"id":3,"gender":"M","first":"Jeff","last":"Stevenson","city":"Washington, D.C.","status":"Active"},
	{"id":4,"gender":"F","first":"Jennifer","last":"Gill","city":"Seattle, WA","status":"Active"}	
])

// Find all the friends in Seattle
const friendsInSeattle = friends({city:"Seattle, WA"}).get()
console.log(friendsInSeattle)
```

### Register new queries

```sh
TAFFY.registerQueries({ 'endsWith': (mvalue, mtest) => mvalue.toString().endsWith(mtest) })
const taffy = TAFFY(data)

console.log(taffy({
  first_name: {
    'endsWith': 'r'
  },
  last_name:{
    startsWith: 'D'
  },
  gender: 'Male'
}).get())
```


## Documentation
https://taffydb.com/
