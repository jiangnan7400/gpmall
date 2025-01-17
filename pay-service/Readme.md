# 支付系统

## 分支管理

> 说明：该流程为根据通用的git分支管理并结合公司环境简化后的流程。       
> 要理解git分支管理需要摒弃svn分支管理的思维，两者区别很大。        
> 参考：[git分支管理最佳实践](http://blog.jobbole.com/109466/)   
> 飞机票： [项目地址](https://github.com/2227324689/gpmall )  

### 分支命名规范

1. 分支名必须符合规范，规范为<code>项目名大写\_branch\_时间_qq_分支的描述</code>或<code>master</code>。 
2. 如果不需要部署，如开发分支，只用来开发，测试时使用测试分支部署
3. 常用命名方式： feature/特性分支名，hotfix/bug修复分支名

### 开发规范
1.写代码，参考以后代码的标准来写，可以优化，但是不能加各种代码
2.如果要增加一些通用的功能，那么请把这个通用的功能在整个项目中全部集成，比如swagger
3. Mic会每周合并一次版本，并且打一个tag
4. 每个人提交的代码，必须要在提交备注中注明qq号码，方便联系
5. 每天更新代码之前，必须要先pull，再push，如果遇到分支冲突，请根据qq号码找到对应的同学确认好再合
6. 为保证代码质量，各位请安装ali编码规约扫描插件。

**tips**：   



## 常用git命令
~~~
// 添加所有已追踪文件到暂存区
git add .
// 提交到本地仓库
git commit -m "注释"
// 添加所有已追踪文件到暂存区，然后提交到本地仓库
git commit -am "注释"
// 推送到远程仓库
git push
// 拉取远程仓库内容并合并到本地仓库
git pull
// 切换分支
git checkout 分支名
// 合并分支到当前分支
git merge origin/要合并过来的分支名
// 拉取远程仓库内容，如果远程仓库删除了分支，使用pull不会更新已删除分支，
// 也就是已删除分支在本地还能看到。使用git fetch --prune不会这样
git fetch --prune
~~~