# Touchstone-appendix
Touchstone+实验附录
如图5所示，这组工作负载包括两个表和四个查询，图中的表格展示了这两张表的基本信息，包括各个属性列，键列，每个列的基数大小（键列的基数即为表的大小）和字符串类型列的平均字符串长度。图中也展示了四个典型的查询，其中包括外连接和内连接。q1是一个左外连接查询，它返回每种类型的零件消耗。 q2是一个右外连接查询，它返回每种产品使用某种特殊零件的数量。q3 是一个全外连接查询，它返回具有特定供应商的零件与SalesVolume大于阈值的产品（即主要产品）之间的关系。q4 是一个内连接查询，它返回使用库存小于阈值的零件的产品ID。


![image](https://github.com/smartgood1/Touchstone-appendix/blob/main/%E5%AE%9E%E9%AA%8C%E8%B4%9F%E8%BD%BD.png)
q1: SELECT Type, SUM (SalesVolume) FROM Part LEFT JOIN Product ON P_Partld=Pr_Partld GROUP BY Type;
