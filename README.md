# Python-Tianyancha
----
## 2018-01-31 更新

看到有两位朋友提交了Issues，在这里集中回答一下。
这个项目是本人个人练习的项目，还很不完善，如果遇到问题，请提供详细描述或报错信息，方便大家共同学习。

目前暂时不会放出完整过程，也许回头会写一个。

对于以上声明对您带来的不便，还请见谅。

----
### 天眼查工商注册信息爬虫

采用Excel表格作为输入，根据公司名称查询该公司相关的工商注册信息。包含并不限于：法人名称、公司状态、工商注册号等。
最终结果输出至以运行时间为文件名的Excel文件内。

### 配置与使用

#### 安装依赖

```
pip install -r requirements.txt
```
#### 增加driver

在main.py同级目录下新建lib文件夹，下载对应版本的Firefox浏览器Drvier放置在lib内。
同时计算机上需要安装Firefox浏览器。

#### 配置

将需要批量查询的公司名称存储为Excel表，对文件名并不做规定，代码内默认为`cxgs.xlsx`，如果需要更改，请自行更改对应代码内的文件名。

#### 输出

最终结果会输出至运行时间为文件名的Excel文件内，形如：`2018-01-04 14_27_28.xlsx`

#### 运行代码

如果是Python2环境，执行：
```
python main.py
```

如果是Python3环境，执行：
```
python main3.py
```

### 其他
- 为什么没有使用Phantomjs呢?

由于在开发测试过程中，Phantomjs会出现随机崩溃的现象，根据日志猜测是由于浏览器内存泄漏导致的。

为排除代码问题，使用Firefox替换后运行8小时未出现崩溃现象。

同时增加了浏览器重启代码，在查询一定数量后重启浏览器释放资源。
