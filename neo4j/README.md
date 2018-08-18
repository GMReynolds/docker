# Neo4j
The docker command creates a virtual environment which produces a UI so that queries can be run on a graphical database

## Cypher
Cypher is the graphical querying language used by Neo4j
Documentation for cypher: https://neo4j.com/docs/developer-manual/3.2/cypher/
Cheatsheet for cypher: https://neo4j.com/docs/cypher-refcard/3.2/

## Issues with tutorial
Whilst completing the northwind tutorial I found issues with the command to load csvs from an URL.
To resolve this I had to download the csv and copy it accross to the the docker container.

```bash
docker cp ./products.csv neo4j:/var/lib/neo4j/import/products.csv
```

To ensure that it was in the correct folder I bashed into the container using this command:

```bash
winpty docker exec -it neo4j bash
```

### Loading csv command change
In order to read in the csv from the docker container instead of the URL - change command from:

```
LOAD CSV WITH HEADERS FROM "http://data.neo4j.com/northwind/categories.csv" AS row
CREATE (n:Category)
SET n = row
```
to:
```
LOAD CSV WITH HEADERS FROM "file:///categories.csv" AS row
CREATE (n:Category)
SET n = row
```
This looks for files in a predefined directory - being the import folder in the container.
