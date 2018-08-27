> # 查看当前表结构
desc table01

> # 赋值
insert into students(name, sex, likes) values('jerry', 'girl', 'game')


> 显示所有已创建的表
show tables;

> 删除表
delete from table02;

> ALTER: 修改表结构

ADD: # 添加字段

alter table students add school_num char(9) first;
 # 向 students表 最前面 添加一个school_num字段

alter table students add s_year year default 1990 after name;
 # 向 students表 name字段后面 添加一个s_year字段

alter table students add email varchar(50), add qq varchar(11);
 # 向 students表 同时添加两个字段

DROP: # 删除字段

alter table students drop sex;
 # 删除 students表 中的 sex字段

alter table students drop sex, age;
 # 删除多条

MODIFY: # 修改字段类型 -> 不允许与已有数据类型冲突

alter table students modify school_num char(9) not null;
 # 学号不允许为空

CHANGE: # 修改字段名或字段类型 -> 不允许与已有数据类型冲突

alter table students change email mail varchar(50);
 # 将email 修改 为 mail

alter table students links loves set('book', 'game', 'music', 'football') not null default 'music, game';
 # 将links 修改 为 loves 并修改默认值






















