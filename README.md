## BSON encoder/decoder from the [Vitess] project

[Vitess]: https://github.com/youtube/vitess

### Installation
```
go get -u github.com/missionMeteora/vitess-bson
```

### Benchmark
```
$ go test -bench=.
PASS
BenchmarkMarshalJSON	  100000	     18042 ns/op
BenchmarkUnmarshalJSON	  100000	     23108 ns/op
BenchmarkMarshal	  200000	     11829 ns/op
BenchmarkUnmarshal	  200000	     13735 ns/op
BenchmarkEncodeField	  500000	      3964 ns/op
BenchmarkEncodeInterface	 1000000	      2478 ns/op
ok  	github.com/missionMeteora/vitess-bson	14.458s
```

### Note
http://gopkg.in/mgo.v2/bson sucks at speed and can't encode uint64.

