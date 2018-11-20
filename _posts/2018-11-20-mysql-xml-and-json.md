---
layout: post
title:  "MySQL 的 xml 和 json 支持"
description: ""
category: "MySQL"
tags: ["MySQL", "xml", "json", "Java", "Python"]
date:   2018-11-20 09:00:00 +0800
---

```sql
create table xml(
	id int not null auto_increment,
	xml varchar(255) not null,
	primary key(id)
);

insert into xml(xml) values('<sucess>100</sucess>');
insert into xml(xml) values('<sucess>100</sucess><failure>200</failure>');

select id, extractvalue(xml, 'sucess') as sucess from xml;

+----+--------+
| id | sucess |
+----+--------+
|  1 | 100    |
|  2 | 100    |
+----+--------+
1 row in set (0.00 sec)

select id, extractvalue(xml, 'sucess') as sucess, extractvalue(xml, 'failure') as failure from xml;
+----+--------+---------+
| id | sucess | failure |
+----+--------+---------+
|  1 | 100    |         |
|  2 | 100    | 200     |
+----+--------+---------+
2 rows in set (0.00 sec)

```