# Git Sync 同步脚本

这是一个一键脚本, 作用于快捷快速提交合并代码.



**缘由:**

因本人想推动外包公司使用`git`代替`ftp`管理代码所写.



<br>

**建议:**

配合`vscode`处理异常冲突更香哦~



<br>

**目录:**

- [原理](####原理)

- [操作系统](####操作系统)
- [安装]()
  - [全局安装](####全局安装)
  - [局部安装](####局部安装)
- [使用方法](####使用方法)



<br><br>

#### 原理

> 我用一段伪代码来表示



```bash
if (检查文件是否有改动 == TRUE) {
	// 合并更新推送
	git add .
	git commit -m "用户名 update"  或  "自定义备注"
	git pull origin ${当前分支}
	git push origin ${当前分支}
} else {
	// 更新本地代码
	git pull origin ${当前分支}
}
```







<br>

<br>

#### 操作系统



- Linux 
- Windows (git bash中使用)







<br>

<br>

#### 全局安装

> 任意git仓库目录可用



##### Linux

- 克隆到`/home/gitsync/`, 把目录添加到环境变量
- 或者直接丢到`/usr/local/bin`

<br>

##### Windows

- 复制`gitsync.sh`到`C:\windows\system32\`目录即可







<br>

<br>

#### 局部安装

> 只能在项目根目录使用

- 复制`gitsync.sh`到项目仓库根目录





<br>


#### 使用

**懒人方法**

> 直接提交, 免输入提交说明.  默认为 `git用户名 update`



```shell
$ gitsync.sh
```



<br>

**自定义提交说明**

```shell
$ gitsync.sh "更新了README"
```



