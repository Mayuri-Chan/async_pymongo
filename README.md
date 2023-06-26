## async_pymongo
Asynchronous wrapper for pymongo  
[Comparison](https://github.com/Mayuri-Chan/async_pymongo/blob/staging/comparison.png)  

### Installing

``` bash
pip3 install async_pymongo
```

### Usage

``` python
from async_pymongo import AsyncClient

async def main():
	conn = AsyncClient("mongodb://...")
	db = conn["database_name"]
	col = db["collections_name"]
	await col.insert_one({"name": "John Smith", "age": 25})
	async for data in col.find({}):
		print(data["name"])
```
 The rest function are same with pymongo but with await
