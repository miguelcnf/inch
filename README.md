inch
====

Inch is an InfluxDB benchmarking tool for testing with different tag
cardinalities.

## Heads Up

This fork is a hacked version of inch to fit a very specific test scenario where I wanted to generate high fields cardinality instead of tags.

Build it and use as follows:

```
$ go build -o inch cmd/inch/main.go

$ ./inch -v -c 8 -b 10000 -t 100000,10000 -p 1
```

This uses 8 cores to write 1 billion unique series each with 2 fields (value distribution: 100000,10000) and 1 point per series using batches of 10000.

This fork is not maintained and the upstream [version](https://github.com/influxdata/inch) should be used for everything else instead.
