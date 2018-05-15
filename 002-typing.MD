# 代码排版:
> 统一格式，方便git等版本工作来diff
+以现有格式排版，方便阅读

# 版本管理(推荐使用GIT)
> 以下所有的规范，示例都是以git进行

## 工具：
+ 统一使用git （可以使用界面化工具如：tortoiseGit）
+ mac版GUI工具，推荐sourceTree
+ windows版也可以用sourceTree

## 版本管理方案：
+ master:一般线上运行稳定的代码会在master上，但不保证最新
+ develop:测试分支
+ dev_1.0.0 会根据版本演进, 版本号按 dev_1.0.0 -> dev_1.0.1 方式手动更新
+ tag 每个版本上线，更新tag，命名参考：v1.0.0

## 版本号(默认写3位)：
+ 第1位：大的版本，大的功能更新 (dev_1.0.0 --> dev_2.0.0)
+ 第2位：一般的版本，功能新增 (dev_1.1.0 --> dev_1.2.0)
+ 第3位：一般是bug的更新，或者很小的功能迭代，需要快速上线，上线周期小于7天的迭代  (dev_1.1.1 --> dev_1.1.2)
+ 第4位：线上项目有bug需要立即修复  (dev_1.1.2 --> dev_1.1.2.1)

## 版本测试分支操作步骤
+ 将开发分支merge到develop分支，利用ci构建发布测试

## 版本上线分支操作步骤（如：当前版本为1.0.3）
+ merge当前分支代码至release分支，release版本同上版本管理方案，发布至预发布环境（ci构建）
+ 和测试确认，通过； merge代码到master上
+ 切换到master分支（确认在这里），打tag，标注版本号同上版本管理方案
+ 下次新的开发task，从master上拉取新的branch

## 关于提交git的一些备注信息：原则上，必须
> [v版本号(去掉点的-统一四位)]动词:  备注信息/bug-编号

+ 功能相关：[issue/feature]
```conf
[v1022]issue: add validation for add lot
[v1022]issue: xxx
```
+ bug修复：[bugfix]
```conf
[v1020]bugfix: bug-6512
[v1020]bugfix: ios7 crash when images too much.
```
+ 性能优化：[optimize]
```conf
[v1023]optimize: lazyLoading for swiper
[v1023]optimize: bug-6752
```

# code Review:
> 高质量的代码，方便管理，迭代，养成一个良好的习惯，有助技术的提高
+ 可以使用一些辅助工具如：code Runner
+ 前端代码验证：eslint/jslint

## 互相Review
+ 推荐团队成员互相review代码
+ 一个功能模块完成后，自己先review

# 语句
> 看起来没多大意义，实则很有用，特别是实际的工程中

## if..else/for/whire都推荐带{}
+ 常规的风格
```javascript
if(condition){

}else{

}
```


+ 团队不推荐的风格
```javascript
if(condition)
//
else
//
```

## swich/case
+ 这个语句可以帮助写出清晰的分支，强制写default

## 三元表达式：
+ 一般最多一层嵌套
+ 原则上：不要做编译器，或者压缩工作帮你做的事情


## 参考：
+ https://github.com/GreatPersonal/fe-style-guide/blob/master/JavaScript.md

# 框架相关：
> react、vue、angular项目

## 通用组件：
+ 来源github 或者 npm
+ 采用之前评估在项目中的可用程度，如可用性不高又没有好的第三方组件，可自行封装发布

## 业务组件：
+ 统一编码用es6 class extends方式：

##模块化规范：
+ require / exports
+ import / exports(推荐，因为是ES2015标准)


## 脚手架：
+ commands:
  +  npm or yarn
```bash
yo project-multipage:component
yo project-multipage:module
yo project-multipage:module-multi
yo project-multipage:service
```

# 代码重构
> DON'T REPEAT YOURSELF.

## 写完即重构
+ 推荐团队成员完成一个模块即对自己完成的模块重构
+ 边开发，边重构


# 部署上线(dev/beta/prd)
> 目前采用的是shell脚本

+ 统一的执行虚拟机脚本
+ jenkins-ci 方案 ?

# 数据模拟
>  mockjs

# 注释
> 真的很重要，（个人习惯问题，至少让别人可以看懂你的代码）

# 测试
> 每完成一个功能的需求。首先自测，不要反反复复的发测试版本改bug,提高效率

# 编辑器
> 工欲善其事必先利其器

## 工作 Vs 个人项目
+ 工作中，可以使用webstorm/phpstorm系工具
+ 轻量级的atom/vscode/vim

# 第三方包管理
> vendor/lib/package

## 原则：
+ 找github star多的，稳定的
+ 不建议使用自己未经项目验证过的包
+ 引入新的库，建议互相告知

# semver语义化版本控制规范
> About version number

## description:
> 版本格式：主版本号.次版本号.修订号，版本号递增规则如下：

- 主版本号：当你做了不兼容的 API 修改
- 次版本号：当你做了向下兼容的功能性新增
- 修订号：当你做了向下兼容的问题修正
- 紧急BUG修复：当你线上有重大紧急BUG修正

## resources:
+ http://semver.org/lang/zh-CN/


# docker-build-solution（参考）
> 利用docker，配置，搭建一个统一的前端的build/prd/本地，虚拟机持续集成(CI)环境

## resouces:
+ https://www.zhihu.com/question/30129756
+ http://www.jianshu.com/p/653f99c32f66
+ https://segmentfault.com/a/1190000007336706
+ http://www.cnblogs.com/freefei/p/5311294.html
+ http://www.cnblogs.com/52fhy/p/5991344.html
+ http://dockone.io/article/834


# jenkins
> 集成webpack压缩打包工具，建议发布生产环境时压缩打包代码


# Workflow
> 迭代


## 新迭代
1. 从master 拉取新的分支，如（dev_1.0.7）
2. 切换到dev_1.0.7分支
3. 在docs目录下，建立新的dev_1.0.7.md的release notes文件
4. 开始第一次提交


## 上线封包 tag
1. 测试同学确认没有问题之后，代码合并至release
2. 通知相关人员，关闭预发布自动更新，上线预发布环境
3. 上线后，测试同学测试，如果有紧急问题，回滚版本，修复紧急bug，重新提交
4. 封包，合代码到master： 如果上述流程没有问题，上线稳定之后，就可以合并代码到master分支
5. 打tag: 封包之后，打tag 


# API
>遵照后端定义api
## 关于分页：
+ page 从 1 开始，而不要从0开始
+ 入参及出参的规则：
```js
//传给后端：
{
  page:1,
  size:10
}
```

# 前端参数的要求，多传，后端统一处理


# 关于readme的作用
> 一般用一个reame file对这个项目进行简单的描述.


## 关于readme的文件标准写法：
+ 以这个名字 README.md 标准命名
