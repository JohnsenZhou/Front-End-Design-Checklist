![Front-End Design Checklist](/images/front-end-design-checklist-banner.jpg)
<h2 align="center">前端设计清单</h2>

<p align="center">
  <em> 一份详尽的前端设计清单，帮助前端开发者理解和分析web设计，确保前端开发的工作效率。</em>
</p>

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![Join the chat at https://gitter.im/Front-End-Checklist/Front-End-Design-Checklist](https://badges.gitter.im/Front-End-Checklist/Front-End-Design-Checklist.svg)](https://gitter.im/Front-End-Checklist/Front-End-Design-Checklist) [![CC0](https://img.shields.io/badge/license-CC0-green.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

## 目录
* **[1. 设计要求](#1---design-requirements)**
	* [1.1 栅格系统](#11---grid-system)
	* [1.2 颜色](#12---colors)
	* [1.3 字体和文字](#13---fonts-and-texts)
	* [1.4 链接和导航](#14---links-and-navigation)
	* [1.5 图片 / 图标](#15---images--icons)
	* [1.6 表单和按钮](#16---forms-and-buttons)
	* [1.7 响应式网站设计](#17---responsive-web-design)
	* [1.8 风格指南和组件方法](#18---style-guide-and-component-approach)
	* [1.9 文件交付](#19---delivery-files)
* **[2. 分析和前期工作准备](#2---analysis-and-pre-work-phases)**
	* [2.1 页面分析](#21---paper-analysis)
	* [2.2 预开发阶段](#22---pre-development-phase)
* **[3. 验证](#3---validation)**
* **[4. 开发阶段](#4---development-phase)**
* **[5. 预上线阶段](#5---before-production)**

---

> **前端设计清单**是Web设计人员和前端开发人员日常设计和开发中需要考虑的元素的详尽清单，以便于提高两者间的协作效率。一下提到的方面都是基于长期分析网页设计经验的总结。

如果您正在寻找一份网站上线前需要进行测试类目的详细列表，请查看 → [前端开发清单](https://github.com/thedaviddias/Front-End-Checklist).


## 怎样使用前端设计清单?

有些时候当开发人员将设计稿转换到代码的过程中，一些重要的点会被忽略。前端设计清单就是解决这样一些问题的工具，让前端开发人员和设计者们都能进行高效率的开发。

你可以吧这份清单分享给web设计者们，从而减少项目交付的时间。或者使用该清单审核设计者们给到的所有素材，确保在代码集成之前所有的都是正确的。


## 为什么你需要使用前端设计清单?

* 确保设计团队考虑到所有的要点
* 创建规范的文档以确保开发人员和设计者之间有一个良好的交流和工作步调的一致性。
* 当开发时间较短时，很容易忘记一些重要的点。
* 避免在设计团队已经开始另一个项目的开发是出现问题。
* web设计者和前端开发者形成互补。

---

## 1. - 设计要求

由于需要完成的项目不仅仅是一些静态页面，而是一个web系统，所以在设计一个网站或一个webapp是必须需要遵循一些规则。接下来的部分对于任何Web项目都很重要。

### 1.1 - 栅格系统

![Grid system](/images/grid-system.png)

* [ ] 设计中明确提供**栅格系统**， 并且在技术规范中明确标出栅格系统的细节(如宽度, 排数, n列数…)。 web设计者可以将栅格保留在透明层汇总，以便于复用到其他项目中。
	> ℹ️ [Guide Guide][6] 是一个在 Photoshop 中快速生成栅格的插件。

	> ℹ️ 在 Sketch 中，你可以通过 “[Make Grid Tool][7]” 插件快速生成栅格。

* [ ] 熟悉你在项目中使用的栅格系统。大多数情况下，开发人员会忽略某些选项（如对齐，偏移量，嵌套等），并且往往会被不必要的手动填充或边距所取代。
* [ ] 在处理网站中的每个模块之前,你只能使用栅格类来构建每个模块。在开发其他细节内容前搭好页面结构将会让你事半功倍！

```html
<div class="container">
  <div class="row">
    <div class="col-sm">
      <!-- Let empty at first -->
    </div>
    <div class="col-sm">
      <!-- Let empty at first -->
    </div>
    <div class="col-sm">
      <!-- Let empty at first -->
    </div>
  </div>
</div>
```

⚠️ *如果你想确保栅格和设备的宽度能正确适配, 你可能想生成一份自己的PDF栅格文件来指导web设计者。*

__其他资源:__

* 🛠 [Bootstrap Grid System][8] (v4)
* 🛠 [Flexbox Grid][9]
* 📖 [Don't Overthink It Grids | CSS-Tricks][10]

**[⬆ back to top](#table-of-contents)**

### 1.2 - 颜色

![Colors](/images/colors.png)

* [ ] **任何素材中的颜色都需要被命名** ($gray-light, $gray-dark, $green) ，或者基于使用场景命名 ($body-background, $body-copy, $text-paragraph…)。可以将它们导出为ACO文件并与开发人员共享（如果使用Photoshop或用于Sketch的标志页）。

![Color Swatches](/images/color-swatches.jpg)

* [ ] 某些元素（如按钮，链接，输入...）不同状态的颜色需要被指定，这些元素需要在明暗背景和浅色或深色文本的背景下工作。（原文：The different color state of some elements (like buttons, links, inputs...) are defined and worked in the context of a light or dark background and with a light or a dark text.）

* [ ] 设计中使用到的、重要的颜色必须可以正常访问，以便在网站/webapp上进行流畅的导航。

__其他资源:__
* 🛠 [WCAG - Contrast Checker](https://contrastchecker.com/)
* 🛠 [Color Safe - accessible web color combinations](http://colorsafe.co/)
* 🛠 [Coolors.co - The super fast color schemes generator](https://coolors.co/)

**[⬆ back to top](#table-of-contents)**

### 1.3 - 字体和文字

![Fonts](/images/fonts.png)

字体是设计过程中的重要组成部分，必须有足够的辨识力。如果项目选择了错误的字体可能会产生财务和法律问题。

建议请客户充分考虑将来可能出现的问题以及使用条件来购买字体。某些网页字体在浏览量方面有限或者无法托管 ([Understanding Webfont Licensing Structures](https://aeolidia.com/understanding-webfont-licensing-structures/))。

* [ ] 提供用于桌面的字体（一般为TTF或OTF），以及WOFF，WOFF2和TTF格式的网页字体（打包在Zip文件中或者提供购买网站的访问链接）。
	> ℹ️ 用于桌面的TTF字体格式与用于Web的TTF字体格式不同。
	
  __资源:__
	* 📖 [Using @font-face | CSS-Tricks](https://css-tricks.com/snippets/css/using-font-face/)
* [ ] [备用字体](https://en.wikipedia.org/wiki/Fallback_font)需要放文档中提供给前端开发人员（一般放在样式指南中）。

  __资源:__
  * 📖 [CSS Basics: Fallback Font Stacks for More Robust Web Typography | CSS-Tricks](https://css-tricks.com/css-basics-fallback-font-stacks-robust-web-typography/)
  * [Create Your Own @font-face Kits » Font Squirrel](https://www.fontsquirrel.com/tools/webfont-generator)

* [ ] 所有网页字体的总大小不超过1-2 Mb（所有变体包括：斜体，粗体等）。

* [ ] 尽可能以正确的语言版本提供所有文本，而不是以英文的虚拟文本提供(Lorem Ipsum and affiliates)。

	> ℹ️ 如果是多语言网站，请务必考虑到如果文本比以前定义的文本长，设计应该是怎样的展示形式。
	
__其他资源:__
* 📖 [Web Font Optimization  |  Web Fundamentals  |  Google Developers](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/webfont-optimization)
* [`font-display` for the Masses | CSS-Tricks](https://css-tricks.com/font-display-masses/)

**[⬆ back to top](#table-of-contents)**

### 1.4 - 链接和导航

![Links and navigation](/images/links.png)

* [ ] 所有链接都需要明确定义default，hover，focus，active，visited状态 (风格指南是指定这些的最佳文档)。
* [ ] 所有导航状态的备用样式 (hover, active/current page).

### 1.5 - 图片 / 图标

![Images](/images/images.png)

* [ ] 设计者至少提供 512px X 512px PNG格式的favicon图片。使用在线工具可以轻松完成favicon图片的生成。

  __资源:__
  * [Favicon Generator for all platforms: iOS, Android, PC/Mac...](https://realfavicongenerator.net/)

* [ ] 所有icon均以SVG格式提供，each in the same square dimension, in black and in a separated folder.

  __资源:__
  * 🛠 [SVGOMG - SVGO's Missing GUI](https://jakearchibald.github.io/svgomg/)

* [ ] 每个icon必须以小写 `icon-` 做前缀 (没有任何空格并用破折号分隔每个单词)。

__其他资源:__
* 📖 [Essential Image Optimization](https://images.guide/)

**[⬆ back to top](#table-of-contents)**

### 1.6 表单和按钮

![Forms](/images/forms.png)

* [ ] 所有表格都有一个可以用作图例的标题
* [ ] 提供不同输入框状态的示例 (至少包括focus、inactive、disabled状态)。
* [ ] 提供所有错误提示, 文字 (最终以独立文档形式) 的位置和颜色必须在素材中清晰的标示出来，并且保持一致。根据返回的错误类型显示不同的错误样式。
  __资源:__
  * 📖 [Forms Need Validation – UX Collective](https://uxdesign.cc/forms-need-validation-2ecbccbacea1)
* [ ] 提供必需/可选字段的标识。
* [ ] 主要和次要的button需要清晰可辨，按照正常惯例使用。
  __资源:__
  * 📖 [Primary & Secondary Action Buttons – UX Planet](https://uxplanet.org/primary-secondary-action-buttons-c16df9b36150)
* [ ] 提供不同按钮状态的示例 (Normal, hover, focused, pressed, inactive)。
* [ ] 提供带内置加载中显示模块的按钮，并可应用于任何按钮。

__其他资源:__

* 📖 [Design Better Forms – UX Collective](https://uxdesign.cc/design-better-forms-96fadca0f49c)
* 📖 [Design Better Input Fields – UX Collective](https://uxdesign.cc/design-better-input-fields-3d02985a8e24)
* 📖 [Designing Perfect Text Field: Clarity, Accessibility and User Effort](https://uxplanet.org/designing-perfect-text-field-clarity-accessibility-and-user-effort-d03c1e26004b)
* 📖 [Button UX Design: Best Practices, Types and States – UX Planet](https://uxplanet.org/button-ux-design-best-practices-types-and-states-647cf4ae0fc6)
* 📖 [How To Design Better Buttons — Smashing Magazine](https://www.smashingmagazine.com/2016/11/a-quick-guide-for-designing-better-buttons/)
* 📖 [Buttons in Design Systems – EightShapes – Medium](https://medium.com/eightshapes-llc/buttons-in-design-systems-eac3acf7e23)

**[⬆ back to top](#table-of-contents)**

### 1.7 - 响应式网站设计

![Responsive](/images/responsive.png)

* [ ] 移动端版本设计搞在PC端版本之前提供或同时提供。

	> 如果设计团队没有遵循“移动优先”的思想，那么移动端和PC版本之间可能会出现一些不规则和不一致的地方，所以在开始项目开发之前检查并标记这些问题。
* [ ] 某些情况下平板电脑版本的设计稿也应该提供。

⚠️ *目前，完美像素级的概念基本上被弃用，因为不可能有面向大量不同屏幕尺寸的设计。*

__其他资源:__

* 📖 [Official Google Webmaster Central Blog: Mobile-first Indexing](https://webmasters.googleblog.com/2016/11/mobile-first-indexing.html)

**[⬆ back to top](#table-of-contents)**

### 1.8 - 风格指南和组件方法

![Styleguide](/images/styleguide.png)

* [ ]每个页面上设计的组件都需要基于组件设计方法论设计（原子设计方法论-Atomic Design）。否则，可能会在性能、项目的可维护性方面出现问题...

  __资源:__
  * 📖 [Atomic design][16]
  * 📖 [6 Reasons for Component-Based UI Development](https://www.tandemseven.com/technology/6-reasons-component-based-ui-development/)

* [ ] 需要提供样式指南，列出所有元素，组件，样式，尺寸。 [UX Power Tools](https://www.uxpower.tools/)等一些样板工具可以帮助节省时间并保持设计的一致性。

⚠️ *在样式指南丢失的情况下，建立一个[living Style Guide](https://github.com/davidhund/styleguide-generators)来促进你的工作效率是一种很好的做法。例如，像Drupal这样的CMS系统提供了插件，允许使用[Pattern Lab](https://drupal-pattern-lab.github.io/)开发一个生动的样式指南。*

__其他资源:__

* 📖 [Style Guides – Design + Sketch – Medium](https://medium.com/sketch-app-sources/tagged/style-guides)
* 📖 [The CodePen Design Patterns and Style Guide](https://codepen.io/guide)
* 📖 [Lonely Planet Travel Guides and Travel Information](http://rizzo.lonelyplanet.com/styleguide/design-elements/colours)
* 📖 [Styleguide](https://www.yelp.com/styleguide)

#### 在现有项目的情况下:

有时，设计团队需要在现有项目中添加新页面或模块。他们应该有一个所有现有设计元素的列表，并使用已有的设计元素。提供样式指南可以节省大量的工作时间并确保项目的一致性。

**[⬆ back to top](#table-of-contents)**

### 1.9 - 文件交付

![Delivery files](/images/delivery-files.png)

* [ ] 对于所有网站，web设计师至少需要提供2个PSD（移动，桌面和平板电脑）或至少1个Sketch文件(如果你有Photoshop CC 2015及以上版本，我推荐使用 artboards)。

	> ℹ️ 一些web设计师会将每个组件创建对应的PSD文件，然后将多个组件作为“智能层”导入到单个PSD中。在这种情况下，你将有多个PSD链接到一个或两个文件。在Sketch下，由于这些库自47版本以来就存在，因此可以将多个文件与符号链接起来......

* [ ] 设计稿文件在交付给开发人员之前需要整理清楚（需要删除空的和不需要的图层以避免文件过大）。

* [ ] 设计了404错误页面。
* [ ] 所有popins，弹出窗口和alert框都需要提供设计文件，放在一个构图层中。

__其他资源:__

* 📖 [Photoshop Etiquette: A Guide to Discernible Web Design](http://photoshopetiquette.com/)

#### PSD文件的具体规则:

* [ ] 如果在同一PSD内提供多个视图，为避免混淆，需要使用层组来显示每个不同的页面，并检查所有元素的组织是否正确。

**[⬆ back to top](#table-of-contents)**

## 2. - 分析和前期工作准备

![Analysis and phases](/images/phases.png)

在开始分析和前期开发工作阶段以及收到设计稿之后，你还需要检查一些重要元素：

* __*使用哪个版本的Photoshop，Sketch?*__
  某些功能特定于某些版本的Photoshop或Sketch。所以举出与此有关的问题都是非常重要的。
* __*每个PSD或画板的宽度是否正确?*__
  如果在设计的每一页上都添加了一些空间，请确认网站的要展示的精确宽度。
* __*设计稿是否使用了太多的“box-shadow”，“线性或径向渐变（linear or radial gradient）”...?*__
  不要忘记那些可能会影响浏览器绘制性能的效果。
* __*是否提供了一个网站地图（sitemap） / 面包屑（breadcrumb）来理解所有页面的依赖关系和体系结构?*__
* __*网站是否需要显示视网膜图片?*__

**[⬆ back to top](#table-of-contents)**

### 2.1 - 素材分析

![Paper Analysis](/images/analysis.png)

建议使用A3格式打印设计稿素材(如果没有A3格式也可以使用A4格式)。由于页面的高度，你可能需要将一些设计稿打印在多个页面上。

用铅笔在纸上分析设计稿是最好的一种方式（或选择不同的彩色铅笔突出显示不同类型的信息）。

1. 至少在一张打印页面上标注出页面的结构，包括header, section, article, main, footer 等。

2. 找到页面中所有的标题部分，确保H1标签没有在logo部分使用，使用需遵循逻辑顺序。大多数情况下，首页的H1标签会被CSS隐藏，但需要保留。如果你的团队中有专门做SEO的人，这方面的分析工作应该由他来完成。
3. 试着去找出类似的组件并且进行重新组合，根据他们的功能而不是仅仅根据上下文给这些组件加以特定的名称。例如 naming a tab system “

4. 目前，大多数设计稿都可以通过CSS完成，不建议使用图像创建任何布局元素，任何简单的图形元素（如按钮或边框）都应该在CSS中完成，以避免出现性能或可伸缩性问题。

5. 发现一些可能缺乏一致性的东西, 比如设计团队没有提供风格指南。 确保任何关于展示方面的素材(Buttons, Typography, Sliders…)都提供并且归类。它可以帮助您创建自己的CSS / Sass架构，或者从确定的CSS框架中选取需要的组件。

⚠️ *在素材分析阶段之后，你可以邀请设计团队使用[InVision](https://www.invisionapp.com/)等工具，以促进设计团队与开发人员之间的沟通和交流。直接在网站上讨论可以节省时间，并且可以保留修改和决策的历史记录。*

### 2.2 - 预开发阶段

* [ ] 根据规范，所有需要用到的插件都要在早期阶段被定义。在正式开始开发前准备一张可能会在开发过程过用到的插件清单，这会让你在开发是保持专注，不会再画大把时间去研究或寻找插件。当然，一些插件并非拿来就能用，还需要进行相应的定制。

__其他资源:__

* 🛠 [Awesome JS][22]
* 🛠 [BestOfJS][23]


**[⬆ back to top](#table-of-contents)**

## 3. - 验证

验证阶段是在项目大致开发完毕后，准备集成前进行的。通常，客户无需等待技术团队的任何批准即可验证素材。正如前端设计清单中所说的那样，开发人员在开始写代码之前确保交付质量是至关重要的。

## 4. - 开发阶段

* [ ] 在开始开发之前，所有媒体素材都需要被剪切和保存。这可以帮助你避免在切图工具和代码编辑器之间来回切换。

* [ ] 图片文件夹具有清晰的架构，你可以在其中排列布局的图片。这对保持项目之间的一致性非常重要。定义文件夹的结构和文件的命名约定可能会对你有所帮助。


  你可以使用一个前缀来识别每个图像附件可能使用的场景，如下所示。

```bash
.
└── images
    ├── background
    ├── banners
    ├── icons
    └── layout
```

* [ ] 使用命名约定，如为不同类型的图像添加前缀，用于背景的所有图像可以使用前缀`bg-`，图标可以使用前缀`icon-`， banner图可以使用前缀`banner-`等等。


## 5. - 预上线阶段

在发布你的网站前，请务必使用[Front-End Checklist](https://frontendchecklist.io)检查所有的网页！

**[⬆ back to top](#table-of-contents)**

---

## Translations

The Front-End Design Checklist will be soon available in other languages. Don't hesitate if you want to help for forking this repository and start with a translation in your language!

## Support

如果有任何的疑问或建议，请通过以下方式联系我们:

* [Give an UP on Product Hunt](https://www.producthunt.com/posts/front-end-design-checklist)
* [Chat on Gitter](https://gitter.im/Front-End-Checklist][28]/Front-End-Design-Checklist?utm_source=share-link&utm_medium=link&utm_campaign=share-link)
* [Facebook](https://www.facebook.com/frontenddesignchecklist/)
* [Twitter](https://twitter.com/thedaviddias)

## Author

**[David Dias](https://github.com/thedaviddias)**

## Contributors

This project exists thanks to all the people who [contribute!](.github/CONTRIBUTING.md)

## License

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

All icons are provided by [Icons8](https://icons8.com/)

**[⬆ back to top](#table-of-contents)**


[6]:	https://guideguide.me/
[7]:	https://www.sketchapp.com/docs/canvas/rulers-guides-grids/
[8]:	https://getbootstrap.com/docs/4.0/layout/grid/
[9]:	http://flexboxgrid.com/
[10]: https://css-tricks.com/dont-overthink-it-grids/
[11]:	https://www.lifewire.com/aco-file-2619477
[16]:	http://bradfrost.com/blog/post/atomic-web-design/
[22]:	https://js.libhunt.com/
[23]:	https://bestof.js.org/
[28]:	https://gitter.im/Front-End-Checklist/Front-End-Design-Checklist
