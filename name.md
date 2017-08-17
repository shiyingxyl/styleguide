命名规范
==========================

此为前端开发团队遵循和约定的**命名规范**，意在实现命名的一致性。


## 命名范围

```
.
├── 路由
├── 文件夹
├── 文件
    ├── .JS文件
    ├── 类文件
    ├── .vue文件
    ├── .css文件
    ├── .html文件
    ├── 枚举文件
├── 常量

```

### 路由

#### [强制] 每个路由链接必须「MUST」以单词小写和`（-）`中杠拼接的方式命名。

示例：

```
// good
http://127.0.0.1:8888/ism/index.html#/cloud-monitor/monitor-view/type/server-perf-monitor/routine/1?des=lang.serverPerfMonitor

// bad
http://127.0.0.1:8888/ism/index.html#/cloud-monitor/monitorView/type/serverPerfMonitor/routine/1?des=lang.serverPerfMonitor
```

### 文件夹

#### [强制] `文件夹` 使用 `全部字母小写，单词间中划线分隔` 的命名方式。

示例：

```
// good
cloud-monitor

// bad
cloudMonitor
```

### .js文件

#### [强制] 使用 `Camel命名法`

示例：

```
cloudMonitor.js

```

### 类文件

#### [强制] 使用 `Pascal命名法`

示例：

```javascript
function TextNode(options) {
}
```

### .vue文件

#### [强制] 使用 `Pascal命名法`

示例：

```
// good
CloudMonitor.vue

// bad
cloudMonitor.vue
```
### 枚举文件

#### [强制] `枚举变量` 使用 `Pascal命名法`，`枚举的属性` 使用 `全部字母大写，单词间下划线分隔` 的命名方式。

示例：

```javascript
var TargetState = {
    READING: 1,
    READED: 2,
    APPLIED: 3,
    READY: 4,
    RESULT_FAILED: 'failed'
};
```

### .css文件

#### [强制] `css文件` 使用 `全部字母小写，单词间中划线分隔` 的命名方式。`css类`使用 `全部字母小写，单词间中划线分隔` 的命名方式。

示例：

```
index-blue.css

.panel-default {
  border-color: #dcdfeb;
}

```


### .html文件

#### [强制] 使用 `Camel命名法`

示例：

```
cloudMonitor.html

```


### 常量

#### [强制] `常量` 使用 `全部字母大写，单词间下划线分隔` 的命名方式。

示例：

```javascript
var HTML_ENTITY = {};
```