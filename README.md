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
### 请按照以上表结构完成以下接口的开发
- **添加用户**
 - 输入参数列表:
<table>
    <thead>
        <tr>
            <th>参数</th>
            <th>名称</th>
            <th>类型</th>
            <th>是否必填</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>username</td>
            <td>用户名</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>gender</td>
            <td>性别</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>mobile</td>
            <td>手机号码</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>email</td>
            <td>邮箱地址</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>birthday</td>
            <td>生日</td>
            <td>string</td>
            <td>Y</td>
        </tr>
    </tbody>
</table>
 - 输出参数列表:
<table>
    <thead>
        <tr>
            <th>参数</th>
            <th>名称</th>
            <th>类型</th>
            <th>是否必填</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>code</td>
            <td>应答码</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>desc</td>
            <td>应答描述</td>
            <td>string</td>
            <td>Y</td>
        </tr>
    </tbody>
</table>
- **根据ID查询用户信息**
 - 输入参数列表： 
<table>
    <thead>
        <tr>
            <th>参数</th>
            <th>名称</th>
            <th>类型</th>
            <th>是否必填</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td>主键标识</td>
            <td>int</td>
            <td>Y</td>
        </tr>
    </tbody>
</table>
 - 输出参数列表:
<table>
    <thead>
        <tr>
            <th>参数</th>
            <th>名称</th>
            <th>类型</th>
            <th>是否必填</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td>主键标识</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>username</td>
            <td>用户名</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>gender</td>
            <td>性别</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>mobile</td>
            <td>手机号码</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>email</td>
            <td>邮箱地址</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>birthday</td>
            <td>生日</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>level</td>
            <td>用户等级</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>enable</td>
            <td>用户状态</td>
            <td>int</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>create_time</td>
            <td>注册时间</td>
            <td>string</td>
            <td>Y</td>
        </tr>
        <tr>
            <td>last_time</td>
            <td>最近修改时间</td>
            <td>string</td>
            <td>Y</td>
        </tr>
    </tbody>
</table>
- **按ID禁用用户**
 - 输入参数列表：
 <table>
    <thead>
        <tr>
            <th>参数</th>
            <th>名称</th>
            <th>类型</th>
            <th>是否必填</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>id</td>
            <td>主键标识</td>
            <td>int</td>
            <td>Y</td>
        </tr>
    </tbody>
</table>
 - 输出参数列表：<br>

|参数|名称|类型|是否必输|
|---------|---------|---------|---------|
|code|应答码|int|Y
|desc|应答描述|string|Y


### 技术要求
- 必须使用spring
- 必须使用maven
- 完整的事物管理
- 接口输入输出使用json格式
- **开发完成之后必须上传到你的git仓库**

### 加分项
- 接口遵循rest规范
- 单元测试
- 完整的日志输出
- 良好的编程习惯，包括但不限于注释、异常处理等等
- 良好的性能

### 备注
- 可选开发工具eclipse、idea
- 数据库连接参数<br>
    ip:127.0.0.1<br>
    port:3306<br>
    username:root<br>
    password:123456<br>