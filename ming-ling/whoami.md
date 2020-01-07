# whoami

打印当前有效的用户名称

## 补充说明

**whoami命令** 用于打印当前有效的用户名称，相当于执行`id -un`命令。

### 语法

```text
whoami(选项)
```

### 选项

```text
--help：在线帮助；
--version：显示版本信息。
```

### 实例

```text
[root@localhost ~]# whoami
root

[root@localhost ~]# id -un
root
```

