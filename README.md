## Fries Output Converter and Reach Results Loader

This is a public code repository of the Computational Language Understanding (CLU) Lab led by [Mihai Surdeanu](http://surdeanu.info/mihai/) at [University of Arizona](http://www.arizona.edu).

Author: [Tom Hicks](https://github.com/hickst)

Purpose: Converts triples of FRIES-format JSON files, containing Reach results, into a simpler
format for ingestion into an ElasticSearch datastore, from which they will be later queried.

## Installation

This software requires Java 1.8, Gradle 2.7, Groovy 2.4.x+, and ElasticSearch 2.4.1.
An accessible ElasticSearch cluster must be running simultaneously with this program.

To build the standalone JAR file in the build/libs subdirectory:

```
   > gradle clean shadowJar
```

To run the JAR file:

```
   > java -jar friolo-2.5.0.jar -v /input/dir/path
```

Run Options:

```
Usage: friolo [-h] [-b N] [-c clusterName] [-i indexName] [-t typeName] directory
 -b,--bulk <N>        Use bulk loading with N additional processes (default: no bulk loading)
 -c,--cluster <arg>   ElasticSearch cluster name (default: reach)
 -h,--help            Show usage information
 -i,--index <arg>     ElasticSearch index name (default: results)
 -t,--type <arg>      ElasticSearch type name (default: conn)
 -v,--verbose         Run in verbose mode (default: non-verbose)
```

## License

Licensed under Apache License Version 2.0.

(c) The University of Arizona, 2015
