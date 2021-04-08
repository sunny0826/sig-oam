---
description: KubeVela 文档翻译流程
---

# KubeVela 文档翻译流程

## 背景

KubeVela v1.0 启用了新的官网架构和文档维护方式，新增功能包括文档版本化控制、i18n 国际化以及自动化流程。但目前 KubeVela 官方文档只有英文版，这提高了学习和使用 KubeVela 的门槛，不利于项目的传播和发展，同时翻译工作也能显著提升语言能力，帮助我们拓宽阅读技术资料的广度，故组织本次活动。

## 活动流程

本次活动主要在 [kubevela.io](https://github.com/oam-dev/kubevela.io) repo 下进行，报名参与和认领任务都在 [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1drZwWF2FWPCbb_HvofzXhZLjtSuhQ-dZgFIPy1tkiYM/edit#gid=2054087633) 中（**请务必在表格中登记信息**）。

### 开始翻译

![翻译流程](https://tva3.sinaimg.cn/large/ad5fbf65ly1gpcbwnnslzj20iy0k20uh.jpg)

参与翻译活动的基本流程如下：
- 任务领取：在 [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1drZwWF2FWPCbb_HvofzXhZLjtSuhQ-dZgFIPy1tkiYM/edit#gid=2054087633) 登记并认领任务；
- 提交：参与人员提交 PR 等待 review；
- 审阅：maintainer 审阅 PR；
- 终审： 对 review 后的内容进行最后确认；
- 合并：merge 到 master 分支，任务结束。

### 参与指南

下面具体介绍参与翻译的具体工作。

#### 准备工作

- 账号：您需要先准备一个 GitHub 账号。使用 Github 进行翻译任务的认领和 PR 提交。
- 仓库和分支管理
  - fork [kubevela.io](https://github.com/oam-dev/kubevela.io) 的仓库，并作为自己仓库的上游： `git remote add upstream https://github.com/oam-dev/kubevela.io.git`
  - 在自己的仓库，也就是 origin 上进行翻译；
  - 一个任务新建一个 branch
- Node.js 版本 >= 12.13.0 （可以使用 `node -v` 命令查看）
- Yarn 版本 >= 1.5（可以使用 `yarn --version` 命令查看）

#### 参与步骤

**Step1：任务浏览**

在 [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1drZwWF2FWPCbb_HvofzXhZLjtSuhQ-dZgFIPy1tkiYM/edit#gid=2054087633) 登记并浏览有哪些任务可以认领。

**Step2：任务领取**

在 [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1drZwWF2FWPCbb_HvofzXhZLjtSuhQ-dZgFIPy1tkiYM/edit#gid=2054087633) 表格中编辑并认领任务。注意：为保证质量，同一译者只能同时认领三个任务，完成后才可继续认领。

**Step3：本地构建和预览**

```shell
# 命令安装依赖
$ yarn install
# 本地运行中文文档
$ yarn run start -- --locale zh
yarn run v1.22.10
warning From Yarn 1.0 onwards, scripts don't require "--" for options to be forwarded. In a future version, any explicit "--" will be forwarded as-is to the scripts.
$ docusaurus start --locale zh
Starting the development server...
Docusaurus website is running at: http://localhost:3000/zh/
✔ Client
  Compiled successfully in 7.54s
ℹ ｢wds｣: Project is running at http://localhost:3000/
ℹ ｢wds｣: webpack output is served from /zh/
ℹ ｢wds｣: Content not from webpack is served from /Users/saybot/own/kubevela.io
ℹ ｢wds｣: 404s will fallback to /index.html
✔ Client
  Compiled successfully in 137.94ms
```
请勿修改 `/docs` 目录下内容，中文文档在 `/i18n/zh/docusaurus-plugin-content-docs` 中，之后就可以在 http://localhost:3000/zh/ 中进行预览了。

**Step4：提交 PR**

确认翻译完成就可以提交 PR 了，注意：为了方便 review 每篇翻译为**一个 PR**，如果翻译多篇请 checkout **多个分支**并提交多个 PR。

**Step5：审阅**

由 maintainer 对 PR 进行 review。

**Step6：任务完成**

翻译合格的文章将会 merge 到 [kubevela.io](https://github.com/oam-dev/kubevela.io) 的 master 分支进行发布。

## 活动主办

本次活动由 KubeVela 社区发起，KubeVela 社区和云原生社区 OAM SIG 共同举办。
