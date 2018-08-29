整理有用的前端技术及文档，工作中的一些经验，供以后查阅。欢迎 developer 补充
### 前端工具
- Git
1. 猴子都能懂的Git入门， [Git 入门教程](https://backlog.com/git-tutorial/cn/intro/intro1_1.html)
1. 廖雪峰的官方网站，[浅显易懂的Git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)  
面向初学者，实用性超强，边学边练。没有接触过版本控制概念的读者也可以轻松入门，文字加图片，还有视频！
2. Git使用官方文档 [Git 简体中文官网](https://git-scm.com/book/zh/v2)
- 图片
1. 占位图  
在开发中，我们常常需要临时用一张图片来占位，可以使用 [占位图片](https://placeholder.com/) 网站中介绍的方法，只要把你的图像大小放在我们的URL后面，你就会得到一个占位图像。  如 [350*150的占位图片](https://via.placeholder.com/350x150) 将会得到一个长为350px，宽为150px的纯灰色图。  
2. 图片压缩  
生产环境中需要使用几张图片，必须压缩，节省带宽和加载时间。可以使用 [微型压缩网站](https://tinypng.com/ ) 一次最多上传20张图片，最大5M。采用“量子化”的技术，减少颜色数量和删除不必要的元数据
3. 图片编辑  
有时候我们需要编辑一张图片，但是没安装PS，或者电脑卡的缘故，可以使用 [在线图片编辑器](http://www.uupoop.com/)，功能强大。
- 图标
1. 现代网页对于简单的图形，都不需要再使用图片了，可以减少http请求，同时更改颜色和大小也极为方便。例如微博和微信图标，我们可以通过 [阿里巴巴矢量图标库](http://iconfont.cn/) 来加载，[使用指南](http://iconfont.cn/help/index?spm=a313x.7781069.1998910419.12)
2. Font Awesome 图标 [Font Awesome中文网](http://www.fontawesome.com.cn/)  
Font Awesome 是一套绝佳的图标字体库和CSS框架。Font Awesome 字体为您提供可缩放矢量图标,它可以被定制大小、颜色、阴影以及任何可以用CSS的样式。
3. Glyphicons 字体图标  
Glyphicons Halflings 一般是收费的，但是他们的作者允许 Bootstrap 免费使用。是 Bootstrap 的默认字体图标。通过 Bootstrap 来使用是免费的，其他途径是收费的。
4. [one-div](http://www.one-div.com/) (该网站在编辑这篇文章时，暂时打不开了) 使用一个 div 并充分利用伪元素，制作出了很多小图标，例如视频、杯子、手机、眼睛等。
- 工具
1. Can I Use 一款前端兼容性自查工具  
 前端开发时常需要检查浏览器的兼容性，在这里推荐 [Can I Use](https://caniuse.com/) 这个是一个针对前端开发人员定制的一个查询CSS、Js在个中流行浏览器钟的特性和兼容性的网站，可以很好的保证网页的浏览器兼容性。有了这个工具可以快速的了解到代码在各个浏览器钟的效果。
- IDE/编辑器
1. WebStorm 最智能的JavaScript IDE  
[官网下载地址](http://www.jetbrains.com/webstorm/download)，网速慢的可以通过[百度网盘下载 WebStorm 2018.2.2](https://pan.baidu.com/s/1GH4Id-RpRx5sMjjgMnIt_g)  
曾经因为 WebStrom 一项很友好的提示而喜欢上它，那时候在做一个 Angular 项目，用的 WebStorm。
初始代码：
```
  selectRemind(chars, isLeastOne):boolean {
    if (chars.length === 0) {
      isLeastOne = false;
    } else {
      isLeastOne = true;
    }
    return isLeastOne;
  }
  this.isTypeLeastOne = this.selectRemind(this.projectType, this.isTypeLeastOne);
```
在 if 那里有黄底提示代码可以精简，并且给出示例，改进后代码：
```
  selectRemind(chars):boolean {
    return (chars.length === 0) ? false : true;
  }
  this.isTypeLeastOne = this.selectRemind(this.projectType);
```
少传一个参数，并且函数体代码 6 行变 1 行，还是有黄底提示，进一步精简如下：
```
  selectRemind(chars):boolean {
    return (chars.length !== 0);
  }
  this.isTypeLeastOne = this.selectRemind(this.projectType);
```
- 样式
1. LeSS （Leaner Style Sheets 的缩写） 是一门向后兼容的 CSS 扩展语言。[Less 入门及语法](http://www.bootcss.com/p/lesscss/) LESS 将 CSS 赋予了动态语言的特性，如 变量， 继承， 运算， 函数. LESS 既可以在 客户端 上运行 (支持IE 6+, Webkit, Firefox)，也可以借助Node.js或者Rhino在服务端运行。
2. SCSS 成熟、稳定、强大的 CSS 扩展语言解析器。[SCSS中文网](https://www.sass.hk/)
3. CSS CSS的书籍市面上并不多，如果你是一个CSS初学者，可以购买《CSS权威指南》,如果你想进阶，可以学习《CSS揭秘》和《CSS世界》,[CSS揭秘](http://book.cssmagic.net/)是进阶技巧，CSS世界是进阶基础，《CSS世界》是张鑫旭所写，剖析得很深入，同时可以查看 [张鑫旭博客网站](https://www.zhangxinxu.com/) 看这两本书能让你的CSS写得更少，做得更多。
- 脚本
1. ES5 [网道(互联网文档计划)](https://wangdoc.com/javascript/)  
该教程全面介绍 JavaScript 核心语法，从最简单的开始讲起，循序渐进、由浅入深，力求清晰易懂。所有章节都带有大量的代码实例，便于理解和模仿，可以用到实际项目中，即学即用。该教程适合初学者当作 JavaScript 语言的入门教程，也适合当作日常使用的参考手册。
2. ES6 [ECMAScript 6 入门](http://es6.ruanyifeng.com/)   
《ECMAScript 6 入门》是一本开源的 JavaScript 语言教程，全面介绍 ECMAScript 6 新引入的语法特性。由JS专家，前端“布道者”阮一峰老师编写。

