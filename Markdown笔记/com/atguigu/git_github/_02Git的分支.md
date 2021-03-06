# 分支作用

```
在版本控制过程中,同时推进多个任务
	本地库初始化之后,就会有一个 master 分支
```

* 同时推进多个功能开发,提高开发效率
* 各个分支同时开发,如果一个分支开发 失败,不会对其他分支有任何影响,失败的分支重新开始即可

# 分支操作

### 指定分支更改

1. 切换到需要修改的分支
2. 使用命令接收想就收的分支修改

| 命令 | 作用 |
|---|---|
| git branch -v | 查看已有的分支 |
| git branch name | 创建分支 |
| git checkout name | 切换分支 |
| git merge name | 指定接收分支更改 |

# 分支产生冲突解决

### 为什么会产生冲突

```
对于 git ,不能顾此失彼,必须认为决定处理冲突
	假设:
		两个同事修改了一行数据
			git则会进入选择阶段,提示哪个文件发生了冲突
			对文件进行编辑
			
				<<< HEAD 
					当前文件内容
				=====
					需合并分支内容
				>>> 分支名
				
			保留需要的数据,就需要人为进行操作了
				1. 去掉特殊标记,保留想要的数据
				2. (告知是未合并路径),通过 git add file 标记为已解决
				3. 使用 git commit (不带文件) 提交到本地库,至此合并完成
```

