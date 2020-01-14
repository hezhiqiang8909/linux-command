# kexec

从当前正在运行的内核引导到一个新内核

## 补充说明

**kexec命令** 是Linux内核的一个补丁，让您可以从当前正在运行的内核直接引导到一个新内核。在上面描述的引导序列中，kexec跳过了整个引导装载程序阶段（第一部分）并直接跳转到我们希望引导到的内核。不再有硬件的重启，不再有固件操作，不再涉及引导装载程序。完全避开了引导序列中最弱的一环 -- 固件。这一功能部件带来的最大益处在于，系统现在可以极其快速地重新启动。

**kexec的好处：** 要求高可用性的系统，以及需要不断重新启动系统的内核开发人员，都将受益于kexec。因为 kexec跳过了系统重新启动过程中最耗时的部分（也就是固件初始化硬件设备的阶段），所以重新启动变得非常快，可用性得到了提高。

### 语法

```text
kexec(选项)
```

### 选项

```text
-l：指定内核映像文件；
-e：允许当前被加载的内核；
-f：强制立即调用系统调用“kexec”，而不调用“shutdown”；
-t：指定新内核的类型；
-u：卸载当前的kexec目标内核。
```
