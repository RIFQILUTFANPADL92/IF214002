# TUGAS : 
1. Buat infografik / cheatsheet dari perintah-perintah MySQL di atas (boleh yang mau pake PostgreSQL)

# Browsing 
```python
SHOW DATABASES;
SHOW TABLES;
SHOW FIELDS FROM table / DESCRIBE table;
SHOW CREATE TABLE table;
SHOW PROCESSLIST;
KILL process_number;
```

# Select Join
```python
SELECT ... FROM t1 JOIN t2 ON t1.id1 = t2.id2 WHERE condition;
SELECT ... FROM t1 LEFT JOIN t2 ON t1.id1 = t2.id2 WHERE condition;
SELECT ... FROM t1 JOIN (t2 JOIN t3 ON ...) ON ...
