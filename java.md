Java规范
==========================

此为Java开发团队遵循和约定的**命名规范**，意在实现命名的一致性。

### Api接口

#### [强制] `Api接口` 使用 `Restful` 风格
> [推荐] [Restful API 设计参考](https://github.com/aisuhua/restful-api-design-references) 

#### [强制] `Api接口` 返回格式统一封装
> [推荐] 

> 示例

```
{
  code: 0, //code为0表示成功，其他则为具体错误码
  data: [],
  msg: ""
}
```


#### [强制]错误码规范统一
> [推荐] 按照功能模块进行分类

> 示例：

```
  1000X  用户中心模块错误码
  2000X  统一账单模块错误码
  3000X  统一订单模块错误码
```

---

### 命名

#### [强制] 代码中的命名均不能以`下划线或美元符号`开始,也不能以`下划线或美元符号`结束

> 示例：

```
// bad
_name / __name / $name / name_ / name$ / name__
```

#### [强制] 代码中的命名严禁使用拼音与英文混合的方式,更不允许直接使用中文的方式

> 说明: 正确的英文拼写和语法可以让阅读者易于理解,避免歧义。注意,即使纯拼音命名方式 也要避免采用。

> 示例：
```
//good
alibaba / taobao / youku / hangzhou 等国际通用的名称,可视同英文。

// bad
DaZhePromotion [打折] / getPingfenByName() [评分] / int 某变量 = 3
```

#### [强制] 类名使用 UpperCamelCase 风格,但以下情形例外:DO / BO / DTO / VO / AO / PO / UID等。
> 示例：
```
//good
MarcoPolo / UserDO / XmlService / TcpUdpDeal / TaPromotion

// bad
macroPolo / UserDo / XMLService / TCPUDPDeal / TAPromotion
```

#### [强制] 方法名、参数名、成员变量、局部变量都统一使用 lowerCamelCase 风格,必须遵从 驼峰形式。
> 示例：
```
//good
localValue / getHttpMessage() / inputUserId
```

#### [强制] 常量命名全部大写,单词间用下划线隔开,力求语义表达完整清楚,不要嫌名字长。
> 示例：
```
//good
MAX_STOCK_COUNT

//bad
MAX_COUNT
```

#### [强制] 包名统一使用`小写`,点分隔符之间有且仅有一个自然语义的英语单词。包名统一使用`单数`形式,但是类名如果有`复数`含义,类名可以使用`复数`形式。
> 示例：
```
//good
应用工具类包名为  com.dimpt.cbuni.util、类名为 MessageUtils(此规则参考 spring 的框架结构)
```

#### [强制] 杜绝完全不规范的缩写,避免望文不知义

> 示例：
```
//bad
AbstractClass“缩写”命名成 AbsClass; condition“缩写”命名成 condi,此类随 意缩写严重降低了代码的可阅读性
```

#### [强制] 对于 Service 和 DAO 类,基于 SOA 的理念,暴露出来的服务一定是接口, 接口类用I前缀标示,内部的实现类用 Impl 的后缀与接口区别

> 示例：
```
//good
CacheServiceImpl 实现 ICacheService 接口
```

--- 
### 注释

#### [强制] 使用JavaDoc规范
>【参考】对于注释的要求:第一、能够准确反应设计思想和代码逻辑;第二、能够描述业务含 义,使别的程序员能够迅速了解到代码背后的信息。完全没有注释的大段代码对于阅读者形同 天书,注释是给自己看的,即使隔很长时间,也能清晰理解当时的思路;注释也是给继任者看 的,使其能够快速接替自己的工作。
> 【参考】好的命名、代码结构是自解释的,注释力求精简准确、表达到位。避免出现注释的一个极端:过多过滥的注释,代码的逻辑一旦修改,修改注释是相当大的负担。

---
### Maven规范
> TODO

---
### MySql数据库规范

#### [强制] 存储引擎使用InnoDB，字符编码utf8-unicode-ci

#### [强制] 表名使用下划线分割（蛇形法）
> 示例：
```
//good
t_user, t_info
```
#### [强制] 表名、字段名必须使用小写字母或数字,禁止出现数字开头,禁止两个下划线中间只 出现数字。
> 说明:MySQL 在 Windows 下不区分大小写,但在 Linux 下默认是区分大小写。因此,数据库名、 表名、字段名,都不允许出现任何大写字母,避免节外生枝。 

> 示例：
```
//good 
aliyun_admin,rdc_config,level3_name

//bad
AliyunAdmin,rdcConfig,level_3_name
```
#### [强制] 表名不使用复数名词。
> 说明:表名应该仅仅表示表里面的实体内容,不应该表示实体数量,对应于 DO 类名也是单数 形式,符合表达习惯。

#### [强制] 主键索引名为 pk_字段名;唯一索引名为 uk_字段名;普通索引名则为 idx_字段名。
> 说明:pk_ 即 primary key;uk_ 即 unique key;idx_ 即 index 的简称。






