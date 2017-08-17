浪潮FED项目目录规范
==========================

此为前端开发团队遵循和约定的**浪潮FED项目目录规范**，意在实现浪潮项目目录结构的一致性。

## 说明
文档中使用的关键字「MUST」,「MUST NOT」,「REQUIRED」,「SHALL」,「SHALL
NOT」,「SHOULD」,「SHOULD NOT」,「RECOMMENDED」,「MAY」和「OPTIONAL」在[RFC2119](http://oss.org.cn/man/develop/rfc/RFC2119.txt)中被说明。

## 目录规范

参加的目录结构为：

```
.
├── .editorconfig
├── .babelrc
├── .eslintrc.js
├── .gitingore
├── package.json
├── bin
├── build
├── config
├── dev
├── dist
├── server
├── node_modules
├── src
    ├── assets
        ├── img
        ├── styles
├── static
├── README.md
├── src
```

### README.md

每个项目都必须「MUST」包含一个`README.md`文件，此文件中应当「SHOULD」概要描述此项目的功能和特点等信息。

### .editorconfig

每个项目应当「SHOULD」包含`.editorconfig`，用来统一配置编辑器的换行、缩进存储格式，使用方式请参考[editorconfig是什么？](https://github.com/fex-team/styleguide/blob/master/editorconfig.md)。

### .babelrc

每个项目应当「SHOULD」包含`.babelrc`，用来统一配置转码的规则和插件的，使用方式请参考[babelrc是什么？](http://www.ruanyifeng.com/blog/2016/01/babel.html)

### .eslintrc.js

### [注意] 所有的文件必须`eslint`验证通过方能提交

每个项目应当「SHOULD」包含`.eslintrc`，用来统一配置代码规范的验证规则，使用方式请参考[eslint是什么？](http://www.jianshu.com/p/2bcdce1dc8d4)


### node_modules

项目中所有 前端第三方仓库 应当「SHOULD」存放在此目录下。

### server

项目中所有 前端SERVER 源码应当「SHOULD」存放在此目录下。

### src

项目中所有 前端JS 源码应当「SHOULD」存放在此目录下，且所有JS文件编写应当「SHOULD」遵循[Javascript 编码规范](https://github.com/fex-team/styleguide/blob/master/javascript.md)。

### src/assets

样式类文件存放应当「SHOULD」遵循以下规律，且文件编写应当「SHOULD」遵循[CSS 编码规范](https://github.com/fex-team/styleguide/blob/master/css.md)。

* 样式文件应当「SHOULD」统一存放在 styles 目录下面。
* 带主题的样式文件应当「SHOULD」根据主题个数存放对应个数的主题样式文件。
* 样式中对应图片文件应当「SHOULD」存放在样式文件所在的主题目录下的 `images` 目录下。

### doc

所有项目应当「SHOULD」包含一个 `doc` 目录，用来存放详细的 API 使用文档。

### dev

dev 作为项目开发调试目录，所有开发调试使用的文件应当「SHOULD」存放在此目录。

### dist

dist 作为项目输出目录，所有编译生成、提供给用户使用的文件应当「SHOULD」存放在此目录。

为了让不太擅长 node.js 的用户可以正常使用编译后的代码，dist 目录应当「SHOULD」包含基本输出结果并提交在 github 中。

### build config

所有工具类脚本应当「SHOULD」放在此目录。

### test

所有测试相关代码应当「SHOULD」放在此目录。

### src_cov

为了测试代码覆盖率，所有为测试覆盖率生成的新 JS 文件应当「SHOULD」存放在此目录下面。
