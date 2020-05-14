---
title: ROLLBACK | TiDB SQL Statement Reference
summary: An overview of the usage of ROLLBACK for the TiDB database.
category: reference
aliases: ['/docs/v3.0/reference/sql/statements/rollback/']
---

# ROLLBACK

This statement reverts all changes in the current transaction inside of TIDB.  It is the opposite of a `COMMIT` statement.

## Synopsis

**Statement:**

![Statement](/media/sqlgram/Statement.png)

## Examples

```sql
mysql> CREATE TABLE t1 (a int NOT NULL PRIMARY KEY);
Query OK, 0 rows affected (0.12 sec)

mysql> BEGIN;
Query OK, 0 rows affected (0.00 sec)

mysql> INSERT INTO t1 VALUES (1);
Query OK, 1 row affected (0.00 sec)

mysql> ROLLBACK;
Query OK, 0 rows affected (0.01 sec)

mysql> SELECT * FROM t1;
Empty set (0.01 sec)
```

## MySQL compatibility

This statement is understood to be fully compatible with MySQL. Any compatibility differences should be [reported via an issue](/report-issue.md) on GitHub.

## See also

* [COMMIT](/sql-statements/sql-statement-commit.md)
* [BEGIN](/sql-statements/sql-statement-begin.md)
* [START TRANSACTION](/sql-statements/sql-statement-start-transaction.md)