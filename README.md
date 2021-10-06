don't work now
Check here for details [it](# error)
# what's this repository

This is a tutorial to get data from mysql with presto and save it in mino.


feature
- without hivemetastore 
- use s3 select


## setup

1. minio
```
docker run -p 9000:9000 -p 9001:9001 \
  quay.io/minio/minio server /data --console-address ":9001" 
```


2. mysql

```
docker run -it --name test-wolrd-mysql -e MYSQL_ROOT_PASSWORD=mysql -d mysql:latest
```

add same data....


3. download presto

- presto-cli
- presto-jdbc
- presto-server

## error

```
presto:games> create table minio.games.akiyoshi as select * from mysql.games.article;
CREATE TABLE: 5 rows

Query 20211002_061531_00023_gwsij, FAILED, 1 node
Splits: 19 total, 19 done (100.00%)
0:02 [5 rows, 0B] [2 rows/s, 0B/s]

Query 20211002_061531_00023_gwsij failed: URI scheme is not "file"

```
