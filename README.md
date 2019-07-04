# InterMine Webservice Client 3.0 Examples

3 July 2019

This Java client library is for use with Web services
attached to InterMine data-warehouses. It abstracts
and simplifies techniques for making structured
queries on remote databases using the InterMine
REST interface.

We provide the following sample programs to demonstrate ways to use the services:

## Query client

The QueryClient demonstrates the use of the InterMine Query Web Service.
This resource can be used to perform arbitrary, complex queries over
the full set of data in the InterMine data warehouse.

This example displays the first 100 Drosophila melanogaster genes sorted by the FlyBase identifier.

```
 ./gradlew execute -PmainClass=samples.QueryClient
```

## Template client

The TemplateClient demonstrates the use of the InterMine Template Web Service. 
This resource can be used to automate access to the predefined queries 
which an InterMine data warehouse has made available.
   
This example returns the first 100 predicted orthologues between two organisms sorted by FlyBase gene identifier.

```
 ./gradlew execute -PmainClass=samples.TemplateClient
```

## List client

The ListClient demonstrates the use of the InterMine List Web Service. 

This example fetches all public lists containing the FBgn0000606 gene.

```
 ./gradlew execute -PmainClass=samples.ListClient
 ```

## Overlaps example

This example demonstrates how you can query for overlapping features for the given coordinates.

```
./gradlew execute -PmainClass=samples.OverlapsExample --args="2L:14615455..14619002 2R:5866646..5868384 3R:2578486..2580016"
```

## GenesFinder client


The GenesFinder demonstrates the use of command line arguments,
with a query client fetching Genes or
SequenceFeatures located at specific positions with some tolerance. You can use
the included sample-input.txt to try this client:

```
 ./gradlew execute -PmainClass=samples.GenesFinder --args="--sample-data"
 ```

## Documentation

* [source code](https://github.com/intermine/intermine-ws-java/) 
* [javadoc](http://intermine.org/intermine-ws-java/javadoc/)


