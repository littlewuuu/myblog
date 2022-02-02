---
title: SSTEM
date: 2022-01-27
tags: 
-  ECN

categories:
-  cours

toc: true # 是否启用内容索引
sidebar: none # 是否启用sidebar侧边栏，none：不启用
---

# BPMN
## 一些词
la finalié, la mission, les objectif
les parties prenantes
Le client Hervé Durand a **retiré**( 删除 ) tous les "Saint-Emilion" de sa commande.
Yvon Manac'h a décidé de faire valoir ses droits à la retraite（退休）
# 模型
#### 1. Modele entité association（有 1:n 的）
*是概念模型的一种，可以看成 ER 图*
#### 2. Modele logique (把 0:n 转化成箭头)
<div align="center">
<img src ="https://i.imgur.com/FWt6tcv.png" width=40%/>
</div>

#### 3. Modele Physique des Données (加上每个属性的类型，integer，varchar 什么的)
*也是关系模型*
>
<div align="center">
<img src ="https://i.imgur.com/oUSR1rY.png" width=60%/>
</div>

>DATE 只有日期
TIMESTAMP 包括日期和时间


# SQL
## 基本格式
>**SELECT** [ **DISTINCT** ] [ **COUNT( )** / **SUM( )** / **AVG( )** / **MAX( )** / **MIN( )**]
**FROM** [ **NARURAL JOIN** ] 
**WHERE** [ **AND**/**OR**/**NOT**/**BETWEEN AND**/ ] 
[ <> 不等于 ] [ IN(...) ] 
[ LIKE/ILIKE %(remplace quel nombre de caractères),_ (remplace un caractères) ] 
[ IS NOT NULL/IS NULL ] 
[ UPPER nom LIKE UPPER('ass') ] 
[ IN SELECT (是 where 后面的在不在这个 select 里面)]
    <div align="center">
    <img src ="https://i.imgur.com/07VLDTH.png" width=60%/>
    </div>
    **GROUP BY** [ ] 
    **ORDER BY** [ 可以有多个 order by 的对象，ORDER BY 语句默认按照升序对记录进行排序。要按照降序对记录进行排序，可以使用 DESC 关键字。 ]

>**UNION**
>操作符用于合并两个或多个 SELECT 语句的结果集。UNION 内部的每个 SELECT 语句必须拥有相同数量的列。列也必须拥有相似的数据类型。同时，每个 SELECT 语句中的列的顺序必须相同。
UNION 结果集中的列名总是等于 UNION 中第一个 SELECT 语句中的列名。


## 增删查改
### 数据库操作
> **CREATE DATABASE** *nom*
>**DROP DATABASE** *nom*
### 表操作
>**CREATE TABLE**（）
>**INSERT INTO** table_name [ ( 可以选择属性 ) ] **VALUES** ( 属性值 ) 
>**UPDATE** table_name **SET** **WHERE**
>**DELETE** **FROM** teble_name **WHERE** 
>**增删列**
>>**ALTER TABLE** table_name 
>>**ADD** column_name datatype/**DROP COLUMN** column_name
>>**更改属性**
>>>*SQL Server / MS Access：*
**ALTER TABLE** table_name
**ALTER COLUMN** column_name datatype
*My SQL / Oracle：*
**ALTER TABLE** table_name
**MODIFY COLUMN** column_name datatype


**COMMIT**
<div align="center">
<img src ="https://i.imgur.com/d3lnOZj.png" width=60%/>
</div>

**ROLLBACK**
<div align="center">
<img src ="https://i.imgur.com/JazPwdX.png" width=60%/>
</div>