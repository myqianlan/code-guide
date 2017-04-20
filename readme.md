# 前端代码指导规范

版本：0.1.0

    本规范仅为前端指导规范，在必要的时候可做相应调整，毕竟所有的荆棘都是为了遇见梦想。

unix哲学：( http://www.ruanyifeng.com/blog/2009/06/unix_philosophy.html )

> "简单原则"----尽量用简单的方法解决问题----是"Unix哲学"的根本原则。KISS（keep it simple, stupid）

> "先求运行，再求正确，最后求快。"（Make it run, then make it right, then make it fast.）

## 前端工程构建

### 版本

- node 4 LTS
- npm 建议3+

### 常用基本命令

- npm run dev or local ? 开发
- npm run build-dev  为开发环境编译需要发布的代码
- npm run build-test
- npm run build-prod
- npm run eslint 代码检查
- npm run deploy-dev 部署开发环境代码
- npm run deploy-test 部署测试环境代码
……

### 功能性配置文件

如：.editorconfig .gitignore webpack.config.js fis.js
理论上放在顶层目录下面，可根据不同的代码组织结构做调整

## 文件及目录命名

### 项目命名

项目命名全部采用「小写」格式，以中线分隔。
比如：the-project-name

### 顶层目录名

开发目录 src

发布目录 dist (注：线上文件理论上应该只存这个文件夹下面)

### 目录名

目录名参照项目命名，有复数结构时，可采用复数命名法，比如：scripts, styles, images, modules

### HTML文件命名

所有 HTML 文件名，多个单次组成时，采用「中线」分隔，比如：search-results.html

### CSS/less/scss文件命名

所有 CSS、Less、SCSS 文件名，多个单词组成时，采用「中线」分隔，比如：icons.less, retina-sprites.css

### JavaScript文件命名

所有 JS 文件名，多个单词组成时，采用「中线」分隔，比如：account-model.js

### JSX文件命名
组件以帕斯卡命名，比如：CodeGuide.jsx

### 文件组织结构
分组件目录结构与分功能目录结构等方式可根据项目特点做出选择

## 基本代码规范

- 时刻关注用户体验
- 注意图片的大小
- SPA应延迟加载非首屏业务模块
- 复杂业务逻辑，应辅以相应注释
- 代码格式化（统一使用 WebStorm 的代码格式化即可）
- 书写代码时注意必要的性能影响
- 可维护性大于可重用性
- 尽量避免过度优化
- 尽量让代码简单易懂

## HTML

- 空格等转义字符尽量少用
- 尽量遵循 HTML 标准和语意，但是不应该以浪费实用性作为代价。任何时候都要用尽量小的复杂度和尽量少的标签来解决问题。

## CSS

    参考：https://github.com/Zhangjd/css-style-guide
    
- 鼓励使用 OOCSS 与 BEM
- 在 CSS 中，虽然可以通过 ID 选择元素，但大家通常都会把这种方式列为反面教材。ID 选择器给你的规则声明带来了不必要的高优先级，而且 ID 选择器是不可重用的。
- 正常情况下，请不要让嵌套选择器的深度超过 3 层
- 永远不要嵌套 ID 选择器

## JavaScript

    参考: 
    https://github.com/sivan/javascript-style-guide/blob/master/es5/README.md
    https://github.com/yuche/javascript

- 必要的容错处理
- 不要使用保留字作为键名
- 使用单引号 '' 包裹字符串
- 优先使用 === 和 !== 而不是 == 和 != ，除非你能说出原因
- 条件表达式例如 if 语句通过抽象方法 ToBoolean 强制计算它们的表达式并且总是遵守下面的规则：
    - 对象 被计算为 true
    - Undefined 被计算为 false
    - Null 被计算为 false
    - 布尔值 被计算为 布尔的值
    - 数字 如果是 +0、-0 或 NaN 被计算为 false，否则为 true
    - 字符串 如果是空字符串 '' 被计算为 false，否则为 true
- 必要的空行！
