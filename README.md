## 简介

一个一站式的博客系统。刚达到一个可以用的状态，文档慢慢补吧。。目前自用中。

## 架构

采用了微服务架构，对应了 `packages` 目录下的文件夹（除了 `SDK` ，这个还没开发）。

- server： 对接数据库，整个博客系统的后台服务。（目前数据库只对接了 mongoDB)（基于 nest.js)
- admin: 后台管理系统的前端，基于 `antd pro`
- website: 博客前台，基于`next.js`，采用 `SSG` 静态生成网页，并支持 增量渲染（会在你修改后几秒钟内重新渲染出来），这样比较好对接 `CDN`
- proxy: 一个很简单的 nginx 反代容器，作为对外的出口和网关。

## docker-compose 部署

有一些配置可能会看不懂，部署文档等功能稳定了就补上，暂时部署遇到问题可以提 `issue`。

看不懂编排的话等正式文档就好了。

目前只做了 `docker-compose` 部署的教程，以后慢慢加。

编排文件在 `docker-compose` 文件夹中。

## 更新记录

以下是我自己看的。。等稳定后会出一个正式的文档，并确定正式的版本号。

2022-07-21

- [] 站点运行时间实时更新
- [] 增加文章更新时间
- [x] 目录下面大一点
- [] 增加手动触发构建功能（只能指定某个 目录，没啥意思）
- [x] 移动端无法打赏
- [] 后台保存页码
- [x] 每日增长计数（缺少后端）
- [x] SEO 优化
- [x] 侧边栏点击没反应
- [x] 搜索卡片关闭后依然有遮罩
- [x] mogodb 文章溢出
- [] 返回按钮不对劲 （暂时搁置）

2022-07-21 1.0 补充

- [] 替换默认 404 页面
- [x] 手机端点完侧边栏收起来
- [x] 环境变量传入图片允许 URL
- [] 导入关于报错
- [x] 顶部菜单可配置化
- [x] proxy 镜像通过环境变量传入参数
- [x] 工具站跳转为外部链接
- [x] 主题切换闪烁
- [x] 评论系统报错（需要配置安全域名）
- [x] 主题切换还是闪烁
- [x] 某些文章会撑大
- [x] 老图床替换新图床
- [x] 后台文章顶置筛选
- [] 后台列表样式
- [x] 草稿发布后报错
- [x] 后台编辑器全屏样式
- [x] more 标记无法保存
- [x] 前端 markdown 间距奇怪
- [x] 移动端打不开打赏
- [x] 移动端点完导航收回去。
- [x] 复制代码按钮位置骗了

2022-07-19 todo

- [x] 小尺寸时间线选项溢出
- [x] 搜索框暗色主题
- [x] 复制成功弹窗
- [x] 评论表情搜索暗色
- [x] hover 优化
- [x] 后台搜索标签优化
- [x] 网站图标
- [x] 搜索结果太宽泛 (参考链接搜出来了。。。)
- [x] 增加联系方式
- [x] 增加 GA 和百度分析
- [x] 增加访问人数统计
- [x] 文章卡片小标题改成 logo 的
- [x] 搜索可 Esc 推出
- [x] 增加快捷键图标
- [x] 快速搜索快捷键
- [x] 搜索卡片默认聚焦
- [x] icon 都统一颜色
- [x] 搜索卡片点击后不关闭的 bug
- [x] markdown 支持数学公式和 html
- [x] 目录超长的溢出展示
- [x] 代码全部高亮

- [] markdown 颜色字体大小样式
- [x] 可能存在的搜索点击后无法滑动 bug

---

1.0 必须有的

- [x] 后台 logo 修改
- [x] 后台概览页面
- [x] 文章顶置功能
- [x] docker 部署方案
- [x] API 开发 proxy
- [x] 简单的 README
- [x] 滚动条优化
- [x] 导入导出
- [x] 增加自动主题切换 mode
- [x] 黑暗模式备用 logo
- [x] 黑暗模式备用 作者 logo
- [x] 黑暗模式备用 支付二维码
- [x] 不启用 waline 的配置
- [x] 暗色模式微信二维码

---

2.0

- [] 支持草稿预览（next.js)
- [] 移动端滚动的极限情况
- [] markdown 标题 hash
- [ ] 代码高亮探测 (没搞定)
- [] 搜索可以快捷键选择
- [] 后台黑暗模式
- [ ] 最近评论展示
- [ ] 联系方式展示
- [ ] 友情链接展示
- [ ] 捐赠信息展示
- [ ] 支持导入导出的备份功能
- [ ] 密码文章
- [ ] 可配置的导航菜单，包括二级菜单
- [] 前台图片优化（放大展示+缓存）
