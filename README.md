### Mysql基本操作


> #设置客户端连接服务器编码
```
SET NAMES UTF8;
```

> #丢弃数据库(如果存在)tedu\

```
DROP DATABASE IF EXISTS tedu;
```
> #创建数据库tedu

```
CREATE DATABASE tedu CHARSET=UTF8;
```

> #进入数据库

```
USE tedu;
```

> #创建部门表

```
CREATE TABLE dept(
  did TINYINT PRIMARY KEY AUTO_INCREMENT,
  dname VARCHAR(16)
);
```

> #插入数据

```
INSERT INTO dept VALUES(10,'研发部');
INSERT INTO dept VALUES(20,'市场部');
```

> #创建员工表

```
CREATE TABLE emp(
  eid INT PRIMARY KEY AUTO_INCREMENT,
  ename VARCHAR(8),
  sex BOOL,
  birthday DATE,
  salary DECIMAL(7,2),
  deptId TINYINT,
  FOREIGN KEY(deptId) REFERENCES dept(did)
);
```
> #插入数据

```
INSERT INTO emp VALUES(NULL,'Tom',1,'1990-5-5',6000,20);
INSERT INTO emp VALUES(NULL,'Jerry',0,'1991-8-20',7000,10);
INSERT INTO emp VALUES(NULL,'David',1,'1995-10-20',3000,30);
INSERT INTO emp VALUES(NULL,'Maria',0,'1992-3-20',5000,10);
INSERT INTO emp VALUES(NULL,'Leo',1,'1993-12-3',8000,20);
```

