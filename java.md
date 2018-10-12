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


#### [强制] 错误码规范统一

> [推荐] 按照功能模块进行分类

> 示例：

```
  // good
  1000X   用户中心模块错误码
  2000X   统一账单模块错误码
  3000X   统一订单模块错误码
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
#### [强制] 抽象类命名使用 Abstract 或 Base 开头；异常类命名使用 Exception 结尾；测试类命名以它要测试的类的名称开始，以 Test 结尾。
> 示例：
```
//good
AbstractCompress    UserNotExistException
```

#### [强制] POJO 类中的任何布尔类型的变量，都不要加is，否则部分框架解析会引起序列化错误。
> 说明：
```
定义为基本数据类型 boolean isSuccess;的属性，它的方法也是 isSuccess()，RPC框架在反向解析的时候，“以为”对应的属性名称是success，导致属性获取不到，进而抛出异常。
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

#### [强制] 枚举类名建议带上 Enum 后缀，枚举成员名称需要全大写，单词间用下划线隔开。枚举其实就是特殊的常量类，且构造方法被默认强制是私有。

> 示例：
```
//good
枚举名字：DealStatusEnum；成员名称：SUCCESS / UNKOWN_REASON。
```

#### [强制] 接口类中的方法和属性不要加任何修饰符号（public 也不要加），保持代码的简洁性，并加上有效的 javadoc 注释。尽量不要在接口里定义变量，如果一定要定义变量，肯定是与接口方法相关，并且是整个应用的基础常量。

> 示例：
```
//good
接口方法签名：void f(); 接口基础常量表示：String COMPANY = "asiainfo";
//bad
接口方法定义：public abstract void f();
```

#### [强制] 不允许出现任何魔法值（即未经定义的常量）直接出现在代码中。

> 示例：
```
//bad
String key="Id#ChinaUnicom_"+tradeId;
cache.put(key, value);
```

#### [强制] long 或者 Long 初始赋值时，必须使用大写的 L，不能是小写的 l，小写容易跟数字 1 混淆，造成误解。

> 示例：
```
//bad
Long a = 200l
//good
Long a = 200L
```

#### [强制] 大括号的使用约定。如果是大括号内为空，则简洁地写成{}即可，不需要换行；如果 是非空代码块则：
	1） 左大括号前不换行。
	2） 左大括号后换行。
	3） 右大括号前换行。
	4） 右大括号后还有 else 等代码则不换行；表示终止右大括号后必须换行。

> 示例：
```
//bad
if ()
{
...
}
//good
if (){
...
} else {
...
}
```

#### [强制] if/for/while/switch/do 等保留字与左右括号之间都必须加空格。

> 示例：
```
//good
if (){
...
}
```

#### [强制] 方法参数在定义和传入时，多个参数逗号后边必须加空格。

> 示例：
```
//good
下例中实参的"a",后边必须要有一个空格。
method("a", "b", "c");
```

--- 
### 注释

#### [强制] 使用JavaDoc规范

#### [强制] 类、类属性、类方法的注释必须使用 javadoc 规范，使用/**内容*/格式，不得使用//xxx 方式。

> 说明：
```
在 IDE 编辑窗口中，javadoc 方式会提示相关注释，生成 javadoc 可以正确输出相应注 释；在 IDE 中，工程调用方法时，不进入方法即可悬浮提示方法、参数、返回值的意义，提高 阅读效率。
```
#### [强制] 所有的抽象方法（包括接口中的方法）必须要用 javadoc 注释、除了返回值、参数、 异常说明外，还必须指出该方法做什么事情，实现什么功能。

> 说明：
```
如有实现和调用注意事项，请一并说明。
```
#### [强制] 所有的类都必须添加创建者信息。

#### [强制] 方法内部单行注释，在被注释语句上方另起一行，使用//注释。方法内部多行注释使 用/* */注释，注意与代码对齐。

#### [强制] 所有的枚举类型字段必须要有注释，说明每个数据项的用途。

---
### Maven规范

#### [强制] 同一项目中所有模块版本保持一致。 

#### [强制] 子模块统一继承父模块的版本。

#### [强制] 统一在顶层模块pom的<dependencyManagement/>节中定义所有子模块的依赖版本号，子模块中添加依赖时不要添加版本号。

#### [强制] 开发测试阶段使用SNAPSHOT，生产发布使用RELEASE。 

#### [强制] 新版本迭代只修改顶层POM中的版本。


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






