# MongoDB

> The (shitty) non-ACID "document" "store".

## Turning off profiling
By default, `mongo` will log queries that take longer than 100ms.
It's not possible to turn off the logging entirely, but the 100ms duration can be increased:

```
$ mongo
> db.setProfilingLevel(0, { slowms: 100 })
```

* "profiling level" 0 is the least verbose level
* `slowms` is the minimum latency after which queries will be logged
  * Set this to a high number to "disable" excessive logging

