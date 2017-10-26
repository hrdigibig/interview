# 需求说明
现有数据库表结构如下:
```
create table t_user(
    id int not null  comment '主键' auto_increment primary key,
    username varchar(32) not null default '' comment '用户名',
    password varchar(32) not null default '' comment '登陆密码',
    gender tinyint not null default 0 comment '性别,0:男,1:女',
    mobile varchar(11) not null default '' comment '用户手机号码',
    email varchar(32) not null default '' comment '邮箱地址',
    birthday varchar(8) not null default '' comment '生日,格式:yyyyMMdd',
    level tinyint not null default 0 comment '用户等级',
    enable tinyint not null  default 0 comment '状态,0:可用,1:禁用',
    create_time timestamp not null default current_timestamp comment '注册时间',
    last_time timestamp not null default current_timestamp on update current_timestamp  comment '最近修改时间'
)comment '用户信息表';
```
## 请按照以上表结构完成以下接口的开发

- **添加用户**
 - 输入参数列表:

|参数|名称|类型|是否必输|
|----|----|---|-----|
|id|主键标识|int|Y
|username|用户名|string|Y
|gender|性别|int|Y
|mobile|手机号码|string|Y
|email|邮箱|string|Y
|birthday|生日|string|Y

 - 输出参数列表:

|参数|名称|类型|是否必输|
|---------|---------|---------|---------|
|code|应答码|int|Y
|desc|应答描述|string|Y

- **根据ID查询用户信息**
 - 输入参数列表： 

|参数|名称|类型|是否必输|
|---------|---------|---------|---------|
|id|主键标识|int|Y

 - 输出参数列表:

|参数|名称|类型|是否必输|
|----|----|---|-----|
|id|主键标识|int|Y
|username|用户名|string|Y
|gender|性别|int|Y
|mobile|手机号码|string|Y
|email|邮箱|string|Y
|birthday|生日|string|Y
|level|用户等级|int|Y
|enable|用户状态|int|Y
|create_time|注册时间|string|Y
|last_time|最近修改时间|string|Y
- **按ID禁用用户**
 - 输入参数列表：

|参数|名称|类型|是否必输|
|---------|---------|---------|---------|
|id|主键标识|int|Y

 - 输出参数列表：

|参数|名称|类型|是否必输|
|---------|---------|---------|---------|
|code|应答码|int|Y
|desc|应答描述|string|Y

- **查询所有用户列表**
 - 输入参数：
        无
 - 输出参数：

|参数|名称|类型|是否必输|
|----|----|---|-----|
|id|主键标识|int|Y
|username|用户名|string|Y
|gender|性别|int|Y
|mobile|手机号码|string|Y
|email|邮箱|string|Y
|birthday|生日|string|Y
|level|用户等级|int|Y
|enable|用户状态|int|Y
|create_time|注册时间|string|Y
|last_time|最近修改时间|string|Y



## 技术要求
- 必须使用spring
- 必须使用maven
- 完整的事物管理
- 接口输入输出使用json格式


## 加分项
- 接口遵循rest规范
- 单元测试
- 完整的日志输出
- 良好的编程习惯，包括但不限于注释、异常处理等等
- 良好的性能

## 备注
- **开发完成之后请提交Pull Request**