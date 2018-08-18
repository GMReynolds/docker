# Neo4j
The docker command creates a virtual environment which produces a UI so that queries can be run on a graphical database

## Cypher
Cypher is the graphical querying language used by Neo4j
Documentation for cypher: [https://neo4j.com/docs/developer-manual/3.2/cypher/]

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
