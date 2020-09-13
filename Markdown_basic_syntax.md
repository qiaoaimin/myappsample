# Markdown基本语法

Markdown是一种轻量级的标记语言，它的优点很多，目前也越来越被写作爱好者，撰稿者广泛使用。看到这里请不要被[标记]、[语言]所迷惑，Markdown的语法十分简单。常用的标记符号也不超过十个，这种相对于更复杂的HTML标记语言来说，Markdown可谓是十分轻量的，学习成本也不需要太多，且一旦熟悉这种语法规则，会有一劳永逸的效果。
废话不多说，直接开干，来看看Markdown的基本语法规则。

## 标题

标题是每篇文章都需要也是最常用的格式，在Markdown中，如果这段文字被定义为标题，只须在这段文字前加#号即可。
例：

```txt{class=line-numbers}
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

效果：

# 一级标题

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题

以此类推，总共六级标题，建议在#号后加一个空格，这是最标准的Markdown语法。特别的，还可使用`=`（高阶标题）和`-`（次阶标题）标记一级和二级标题。
例：

```{class=line-numbers}
这是高阶标题（效果和一级标题一样）
=
这是次阶标题（效果和二级标题一样）
```

效果：

这是高阶标题（效果和一阶标题一样）
=

这是次阶标题（效果和二阶标题一样）
-

**注意：**`=`和`-`标记标题时，`=`和`-`的个数在不同的编辑器中有可能不同。

## 段落

段落的前后要有空行，所谓的空行是指没有文字内容。若想在段内强制换行的方式是使用两个或以上空格加上回车（引用中换行省略回车）。

## 列表

熟悉HTML的同学肯定知道有序列表与无序列表的区别，在Marketdown下，列表的显示只需要在文字前加上`-`、`+`或`*`即可表示无序列表，有序列表则直接在文字前加`1.` `2.` `3.`，符号和文字之间加上一个空格。

例1，有序列表

```{class=line-numbers}
1. 第一点
2. 第二点
4. 第三点
```

效果：
1. 第一点
2. 第二点
4. 第三点

例2，无序列表

```{class=line-numbers}
- 这是无序列表项目
+ 这是无序列表项目
* 这是无序列表项目
```

效果：

- 这是无序列表项目
- 这是无序列表项目

+ 这是无序列表项目
+ 这是无序列表项目

* 这是无序列表项目
* 这是无序列表项目

两个列表之间不能相邻，否则解释为列表的嵌套。下面这是嵌套的列表。
例3：
+ 呵呵呵
    * 哈哈哈
    - 嘻嘻嘻
    - 吼吼吼
        - 咚咚咚
        + 噫噫噫
* 突突突
  
**注意：**

1. 标记后面最少有一个`空格`或`制表符`。
2. 若不在引用区块中，必须和前方的段落之间存在空行，后面最好还是空一行，否则会解释为嵌套的列表。
3. 有序列表标记不是按照你写的数字进行显示的，而是根据当前有序列表标记所在位置显示
4. 无序列表的项目符号是按照实心圆、空心圆、实心方格的层级关系递进的，如例3所示。通常情况下，同一层级使用同一种标记表示，便于自己查看和管理。

## 引用

如果你需要引用一小段别处的句子，那么就要用引用的格式。只需要在文本前加上`>`这种尖括号（大于号）即可。

例：
```{class=line-numbers}
> 这是引用
```

效果：
> 这是引用

引用还可以嵌套，如：
```{class=line-numbers}
> 这是一级引用
>> 这是二级引用
>>> 这是三级引用

> 这是一级引用
```

效果：

> 这是一级引用
>> 这是二级引用
>>> 这是三级引用

> 这是一级引用


再如：

```{class=line-numbers}
> 这是一级引用
>> 这是二级引用
>>> 这是三级引用
> 这是一级引用
```

效果：

> 这是一级引用
>> 这是二级引用
>>> 这是三级引用
> 这是一级引用

**注意：**

1. 从上面两列可以看出来，如果`>` `>>` `>>>`嵌套使用的话，从`>>>`倒退`>`时，必须之间加上一个`空行`作为过渡，否则默认为下一行和上一行是同一级别的引用。如上例所示。
2. 引用完成之后，必须再加一个空行，重新一个新的开始，否则，以后的文字都将在引用的范围内。

## 代码块

使用```表示代码块。如：

``` javascript {class=line-numbers}

"``` javascript"
var canvas = document.getElementById("canvas");
var context = canvas.getContext("2d");
"```"
```

## 行内代码

```{class=line-numbers}
这是`java`代码。
```

效果：
这是`java`代码。

## 链接

链接可以使用两种形式生成，**行内式**和**参考式**。

- 行内式链接，使用`[](link "optional title")`表示行内链接。其中

  1. `[]`内的内容为要添加链接的文字；
  2. `link`为链接地址；
  3. `Optional title`为显示标题。显示效果为在你将鼠标放到链接上后，会显示一个小框提示，提示的内容就是`Optional title`里的内容。

例：
```{class=line-numbers}
这就是行内链接：[Qiaoaimin's Markdown note](http://www.zhiwuzhi.org "乔爱民的Markdown笔记")
```

这就是行内链接：[Qiaoaimin's Markdown note](http://www.zhiwuzhi.org "乔爱民的Markdown笔记")

- 参考式链接

例：

```javascript {class=line-numbers}
这里是我们的参考
1. [Javascript | MDN][1]
2. [ECMAScript 6 入门 阮一峰][2]
3. [Info! JavaScript][3]
[1]: http://developer.mozilla.org/zh-CN/docs/Web/JavaScript
[2]: http://es6.ruanyifeng.com
[3]: http://www.infoq.com/cn/javascript/?utm_source=infoq&utm_medium=header_graybar&utm_campaign=topic_cl
```

这里我们参考：

1. [Javascript | MDN][1]
2. [ECMAScript 6 入门 阮一峰][2]
3. [Info! JavaScript][3]

[1]: http://developer.mozilla.org/zh-CN/docs/Web/JavaScript
[2]: http://es6.ruanyifeng.com
[3]: http://www.infoq.com/cn/javascript/?utm_source=infoq&utm_medium=header_graybar&utm_campaign=topic_cl

**注意：** 上述的`[1]: http://developer.mozilla.org/zh-CN/docs/Web/JavaScript`不出现在区块中。

## 图片

插如图片与插入链接的语法很象，区别在一个`!`号，而且也有行内式和参考式两种。
插入图片语法为：`![Alt text](/path/to/umg,jpg "Optional title")`

- `Alt text`为如果图片无法显示时显示的文字。
- `/path/to/img.jpg`为图片所在路径。
- `Optional title`为显示标题。显示效果为在你将鼠标放到图片上后，会显示一个小框提示，提示的内容就是`Optional title`。

例，行内式：

```{class=line-numbers}
### 插入图片
![百度logo](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png)
```

效果：
![百度logo](https://www.baidu.com/img/PCtm_d9c8750bed0b3c7d089fa7d55720d6cf.png)

例，参考式：

```{class=line-numbers}
[图灵社区][4]
![图灵社区logo][5]
[4]: http://www.ituring.com.cn
[5]: http://www.ituring.com.cn/Content/img.Turing.gif
```

[图灵社区][4]
![图灵社区logo][5]
[4]: http://www.ituring.com.cn
[5]: http://www.ituring.com.cn/Content/img.Turing.gif

## 强调

使用`**`或`__`表示粗体。
使用`*`或`_`表示斜体。
使用`~~`表示删除线。

例：
```{class=line-numbers}
**粗体1**  __粗体2__
**斜体1**  __斜体2__
~~这行文字删除~~
```
**粗体1**  __粗体2__
*斜体1*  _斜体2_
~~这行文字删除~~

## 表格

表格用`|`表示竖线，表头和表格内容之间用`-`隔开，并用`:`进行对齐设置。
详细说明如下：
- ----: 右对齐
- :---- 左对齐
- :----: 居中对齐
- ---- 默认左对齐
  
``` javascript {class=line-numbers}
| 序号 | 交易名 | 交易说明         | 备注                                           |
| ---: | :----: | :--------------- | ---------------------------------------------- |
|    1 | prfcfg | 菜单配置         | 可以通过次交易查询到所有交易码和菜单的对应关系 |
|    2 | gentmo | 编译所有交易     |                                                |
|   30 | sysdba | 数据库表模型汇总 |
``` 

| 序号 | 交易名 | 交易说明         | 备注                                           |
| ---: | :----: | :--------------- | ---------------------------------------------- |
|    1 | prfcfg | 菜单配置         | 可以通过次交易查询到所有交易码和菜单的对应关系 |
|    2 | gentmo | 编译所有交易     |                                                |
|   30 | sysdba | 数据库表模型汇总 |

## 分割线

分割线最常使用的就是三个或以上的`*`，还可以使用`-`和`_`。

```{class=line-numbers}
***
---
___
```

***
---
___

**注意：**

1. 只要`*`或者`-`大于等于三个就可以组成一条平行线。
2. 使用`---`作为水平分割线时，要在它的前后都空一行，防止`---`被当成标题标记。

## 反斜杠

用\表示反斜杠，相当于**反转义**作用。在你不想显示Markdown标记时可以使用反斜杠。Markdown支持的转义字符列表：
```javascript{class=line-numbers}
\   反斜线
`   反引号
*   星号
_   底线
{}  大括号
[]  中括号
()  小括号
#   井号
+   加号
-   减号
.   英文句号
!   叹号
```

## 注脚

使用`[^footer1]`表示注脚。

```{class=line-numbers}
这是第一个注脚测试[^footer1]
这是第二个注脚测试[^footer2]
[^footer1]:这是第一个注脚测试的解释；
[^footer2]:这是第一个注脚测试的解释；
```

这是第一个注脚测试[^footer1]
这是第二个注脚测试[^footer2]
[^footer1]:这是第一个注脚测试的解释；
[^footer2]:这是第一个注脚测试的解释；

## 标签分类

内容待补充

## 锚点

内容待补充
