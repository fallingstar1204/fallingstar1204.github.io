## Four SQL command type
##### DDL (Data Definition Language)
CREATE - to create objects in the database
ALTER - alters the structure of the database
DROP - delete objects from the database
TRUNCATE - remove all records from a table, including all spaces allocated for the records are removed
COMMENT - add comments to the data dictionary
RENAME - rename an object

##### DML (Data Manipulation Language)
SELECT - retrieve data from the a database  (也有說select是DRL: Data Retrieval Language)
INSERT - insert data into a table
UPDATE - updates existing data within a table
DELETE - deletes all records from a table, the space for the records remain
MERGE - UPSERT operation (insert or update)
CALL - call a PL/SQL or Java subprogram
EXPLAIN PLAN - explain access path to data
LOCK TABLE - control concurrency

##### DCL (Data Control Language)
GRANT - gives user's access privileges to database
REVOKE - withdraw access privileges given with the GRANT command

##### TCL (Transaction Control Language)
COMMIT - save work done
SAVEPOINT - identify a point in a transaction to which you can later roll back
ROLLBACK - restore database to original since the last COMMIT
SET TRANSACTION - Change transaction options like isolation level and what rollback segment to use

## 正規化 (normalization)
資料庫正規化就是指把關聯式資料庫的欄位與表單做規劃，讓資料重覆性與相依性能夠降到最低。當然這個"資料重覆性與相依性能夠降到最低"情況下，還必須讓資料庫可以正常運作。

##### 第一正規形式(1NF) - 去除重覆性的問題。
- 刪除各個資料表中的重複群組。
- 為每一組關聯的資料建立不同的資料表。
- 使用主索引鍵識別每一組關聯的資料。

##### 第二正規形式(2NF) - 去除部分功能相依的問題。
- 為可套用於多筆記錄的多組值建立不同的資料表。
- 使用外部索引鍵，讓這些資料表產生關聯。

##### 第三正規形式(3NF) - 去除遞移相依的問題。
- 刪除不依賴索引鍵的欄位。
