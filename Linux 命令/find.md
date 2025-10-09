# find

查找文件

## 语法

```bash
find [路径...] [表达式] [动作]
```

## 常用参数

| 参数  | 含义         |
| ----- | ------------ |
| -name | 匹配文件名   |
| -type | 匹配文件类型 |
| -size | 匹配文件大小 |

## 动作

默认为 `-print`，即打印到标准输出。

## 示例

搜索系统中所有以.conf 结尾的文件

```bash
find / -name *.conf
```

在 `/etc` 目录中搜索所有大于 1MB 的文件

```bash
find /etc -size +1M
```

在 `/var/log` 目录下搜索所有指定后缀的文件

```bash
find /var/log -name "*.log"
```

以上查询的相反结果

```bash
find /var/log ! -name "*.log"
```

搜索系统中所有类型为目录，且权限为 `1777` 的目录文件

```bash
find / -type d -perm 1777
```
