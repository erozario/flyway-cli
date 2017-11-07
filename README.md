# flyway-cli
[![Docker Build Status](https://img.shields.io/docker/build/eduardoagrj/flyway-cli.svg)](https://hub.docker.com/r/eduardoagrj/flyway-cli/builds/)

Dockerized [flyway command-line tool](https://flywaydb.org/getstarted/firststeps/commandline) with options to use:

- MariaDB
- MySQL
- Oracle

## Getting started

`docker run eduardoagrj/flyway-cli [flyway cli arguments here]`

## Example

Add a file named `V1__Initial.sql` with following contents:

```
CREATE TABLE MyTable (
    MyColumn VARCHAR(100) NOT NULL
);

```
                                                             
### Usage
`docker run --rm -v $(pwd):/flyway/sql eduardoagrj/flyway-cli -url=jdbc:mysql://mydb -user=root -password=pass123 migrate`

