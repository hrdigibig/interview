# 数多科技机试题
## 需求说明
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
### 请按照以上表结构完成以下接口列表的开发
- 用户添加
- 根据ID查询用户信息
- 按ID禁用用户
- 分页查询

### 技术要点
- 必须使用spring
- 完整的事物管理
- 必须使用maven
- 接口输入输出使用json格式

### 加分项
- 完整的日志输出
- 良好的编程习惯，包括但不限于注释、异常处理等等
- 良好的性能