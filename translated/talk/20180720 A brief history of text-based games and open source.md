[#]: collector: (lujun9972)
[#]: translator: (cycoe)
[#]: reviewer: ( )
[#]: publisher: ( )
[#]: url: ( )
[#]: subject: (A brief history of text-based games and open source)
[#]: via: (https://opensource.com/article/18/7/interactive-fiction-tools)
[#]: author: (Jason Mclntosh https://opensource.com/users/jmac)

关于文字游戏与开源的简史
======

![](https://opensource.com/sites/default/files/styles/image-full-size/public/lead-images/compass_map_explore_adventure.jpg?itok=ecCoVTrZ)

[互动小说技术基金会（IFTF: Interactive Fiction Technology Foundation）][1] 是一个非营利组织，致力于保护那些用来生成我们称之为互动小说的数字艺术形式的技术。当 Opensource.com 的一位社区版主提出一篇关于 IFTF、它支持的技术与服务，以及它如何与开源相交织的文章时，我发现这对于我经常讲的几十的故事来说，是个新颖的视角。互动小说的历史比自由及开源软件（FOSS: Free and Open Source Software）运动的历史要长，但同时也与之密切相关。希望你们能喜欢我在这里的分享。

### 定义和历史

对于我来说，交互式小说这个术语包括了读者主要通过文本与之交互的任何视频游戏或数字化艺术作品。这个术语起源于 20 世纪 80 年代，当时由语法解析器驱动的文本冒险游戏在美国主要体现在，[魔域][2]、[银河系漫游指南][3]，以及 [Infocom][4] 正规定义的家用电脑娱乐。在 20 世纪 90 年代，它的主流商业价值被挖掘出来，但在线爱好者社区还是依照传统，发布游戏和游戏创建工具。

在四分之一个世纪之后的今天，互动小说包括了品种繁多并且妙趣橫生的作品，如从充满谜题的文字冒险游戏到衍生改良的超文本类型。定期的在线竞赛和节日为品鉴试玩新作品提供了个好地方---英语互动小说世界每年都会举办一次活动，包括 [Spring Thing][5] 和 [IFComp][6]。后者是自 1995 年以来现代互动小说的核心活动，这也使它成为在同类型中持续举办时间最长的游戏展示活动。[IFComp 从 2017 年开始的评选和排名记录][7] 展示了如今基于文本的游戏在形式、风格和主题方面的惊人多样性。

(作者注：以上我特指英语，因为可能出于写作方面的技术原因，互动小说社区倾向于按语言进行区分。当然也有 [法语][8] 或 [意大利语][9] 的互动小说年度活动，比如我就听说过至少一届中文互动小说节。幸运的是，这些边界易于打破。在我管理 IFComp 的四年中，我们很欢迎来自国际社区的英语翻译作品。)

![”假冒的猴子“游戏截图][11]

在解释器 Lectrote 上启动 Emily Short 的”假冒的猴子“新游戏（二者皆为开源软件）。

此外由于互动小说专注于文本，它为玩家和作者都提供了最方便的平台。几乎所有能阅读数字化文本的人（包括能通过文字转语音软件等辅助技术阅读的用户）都能玩大部分的互动小说作品。互动小说创作对所有愿意学习和使用其工具和技术的作家开放。

这使我们了解了互动小说与开源的长期关系，以及从它的全盛时期以来，对于艺术形式可用性的积极影响。接下来我将提供现代开源互动小说创建工具的概览，并讨论关于共享源代码这个古老且有点稀奇的互动小说作品传统。

### 开源互动小说工具的世界

一些开发平台（其中大部分是开源的）可用于创建传统的语法解析器驱动互动小说，其中用户可通过输入命令（如 `向北走`、`拾取提灯`、`收养小猫` 或 `向 Zoe 询问量子机械学`）来与游戏世界交互。20 世纪 90 年代初期出现了几个黑客（此处指拥有友好的语法解析器）游戏开发工具箱，其中目前还在使用的有 [TADS][12]、[Alan][13] 和 [Quest][14]，它们都是开源的，并且后两者兼容 FOSS 许可证。

其中最出名的是 [Inform][15]，1993 年 Graham Nelson 发布了第一个版本，目前由 Nelson 领导的一个团队进行维护。Inform 的源代码是半开源的：Inform 6 是前一个主要版本，[它通过 Artistic 许可证开放源码][16]。这其中蕴涵比我们所看到的更直接的相关性，因为其它专有的 Inform 7 将 Inform 6 作为其核心，在让它将作品编译为机器码之前，将其 [杰出的自然语言语法][17] 翻译为其前身那种更类似 C 的代码。

![inform 7 集成式开发环境截图][19]

包含文档以及一个示例项目的 Inform 7 集成式开发环境

Inform 游戏运行在虚拟机上，这是 Inform 时代的遗留产物。当时的发行者为了让同一个游戏运行在 Apple II、Commodore 4、Atari 800 以及其它种类的“[家用计算机][20]”上，将虚拟机作为解决方案。这些原本流行的操作系统中只有少数至今仍存在，但 Inform 的虚拟机使得 Inform 创建的作品能够通过 Inform 解释器运行在任何的计算机上。这些虚拟机包括相对现代的 [Glulx][21]，或者通过对 Inform 过去的虚拟机进行逆向工程克隆得到的可爱的古董 [Z-machine][22]。现在，流行的跨平台解释器包括如 [lectrote][23] 和 [Gargoyle][24] 等桌面程序，以及如 [Quixe][25] 和 [Parchment][26] 等基于浏览器的程序。以上所有均为开源软件。

如其它的流行开源项目一样，如果 Inform 的发展进程随着它的成熟而逐渐变缓，它为我们留下的最重要的财富就是其活跃透明的生态环境。对于 Inform 来说，（这些财富）包括前面提到的解释器、[语言扩展集合][27]（通常混合使用 Inform 6 和 Inform 7 写成），当然也包括所有用它们写成并分享于世界的作品，有的时候也包括那些源代码。（在这篇文章的后半部分我会回到这个话题）

互动小说创建工具在 21 世纪被发明，力求在传统的语法解析器之外探索一种新的玩家交互方式，即创建任何现代 Web 浏览器都能加载的超文本驱动作品。其中的领头羊是 [Twine][28]，原本由 Klimas 在 2009 年开发，目前作为 [GNU 许可证开源项目][29] 由许多贡献者进行活跃开发。（事实上，[Twine][30] 的开源软件血统可追溯到 [TiddlyWiki][31]，一个由 Klimas 最初继承的项目）

对于互动小说开发来说，Twine 代表一系列最开放及最可用的方法。由于它的 FOSS 天性，它通过完备的网页来展示渲染输出，不依赖于需要进一步特殊编译的机器码，而是使用开放并且成熟的 HTML、CSS 和 JavaScript 标准。作为一个创建工具，Twine 能够根据创建者的技能等级，暴露与之相匹配的复杂度。拥有很少或没有编程知识的用户能够创建简单但是可玩的互动小说作品，但那些拥有更多编码和设计技能（包括通过开发 Twine 游戏获得的技能提升）的用户能够创建更复杂的项目。近几年 Twine 在教育领域的可见度和流行度有不小的提升，对此你不要感到太惊讶哦。

另一些值得注意的开源互动小说开发项目包括由 Ian Millington 开发的以 MIT 许可证发布的 [Undum][32]，以及由 Dan Fabulich 和 [Choice of Games][34] 团队开发的 [ChoiceScript][33]，两者也专注于将 Web 浏览器作为游戏平台。除了以上严格的开发系统以外，基于 Web 的互动小说也呈现给我们以开源作品的丰富、变幻的生态。比如 Furkle 的 [Twine 扩展工具集][35]，以及 Liza Daly 为自己的互动小说游戏创建的名为 [Windrift][36] 的 JavaScript 框架。

### 程序、游戏，以及游戏程序

Twine 受益于 [一个致力于提供支持的长期 IFTF 计划][37]，它允许公众为其维护和发展提供资助。IFTF 还直接支持两个长期公共服务，IFComp 和互动小说归档，这两个服务都依赖并回馈开放软件和技术。

![Harmonia 开场截图][39]

由 Liza Daly 开发的“Harmonia”的开场画面，该游戏使用 Windrift 开源互动小说创建框架创建。

自 2014 年以来，用于运行 IFComp 网站的基于 Perl 和 JavaScript 的应用程序一直是 [一个共享源代码项目][40]，它反映了 [互动小说特有子组件使用的 FOSS 许可证是个大杂烩][41]，其中包括那些允许解析器驱动的竞争条目在 Web 浏览器中运行的各式各样的代码库。在 1992 年上线并 [在 2017 年成为一个 IFTF 项目][43] 的 [互动小说归档][42]，是一套完全基于古老且稳定的互联网标准的镜像仓库，只使用了 [一点开源 Pyhon 脚本][44] 用来处理索引。

### 最后，也是最有趣的部分，让我们聊聊开源文字游戏

归档的主体 [由游戏组成][45]，当然，是那些历经岁月的游戏。它们反映了数十年来不断发展的游戏设计趋势和互动小说工具发展。

许多互动小说作品都共享其源代码，社区对于找到它们的快速入门解决方案很简单---[在 IFDB 中搜索标签“source available”][46]。IFDB 是另一个长期运行的互动小说社区服务，由 TADS 的创立者 Mike Roberts 私人运营。对更加简单的界面感到舒适的用户，也可能希望浏览互动小说归档的 [`games/source` 目录][47]，该目录按开发平台和编写语言对内容运行分组（也有很多作品，由于太繁杂或太古老而无法分类，只能浮于列表的开头）。

对这些代码共享游戏随机抽取的几个样本，揭示了一个有趣的窘境：与更广阔的开源软件世界不同，互动小说社区缺少一种普遍认同的方式来授权它生成的所有代码。与软件工具（包括我们用来创建互动小说的所有工具）不同的是，从字面意思上讲，交互式小说游戏是一件艺术作品。这意味着，将面向软件的开源许可证用于交互式小说游戏，并没有比用于其它像散文或诗歌作品更适合。但同样，互动小说游戏也是一个软件，它展示了创建者希望合法地与世界分享的源代码模式和技术。一个拥有开源意识的互动小说创建者会怎么做呢？

有些游戏通过将其代码传递到公共领域来解决这一问题，或者通过明确的许可证，亦或者如 [42 年前由 Crowther 和 Woods 开发的”冒险之旅“][48] 一样通过社区发布。一些人试图将其中的不同部分分开，应用他们自己的许可证，允许免费复用游戏公开的业务逻辑，但禁止针对其散文内容的再创作。这是我在开源自己的游戏 [莺巢][49] 时采取的策略。天知道这是否能在法律上站得住脚，但我当时没有更好的主意。

当然，你会发现一些作品对所有部分使用单一的许可证，而不介意反对者。一个突出的例子就是 [Emily Short 的史诗作品”假冒的猴子“][50]，其全部采用 Creative Commons 4.0 许可证发布。[CC 对其应用于代码感到不满][51]，但你可以认为 [Inform 7 源码这种不寻常的散文风格特性][52] 至少比传统的软件项目更适合 CC 许可证。

### 接下来要做什么呢，冒险者？

如果你希望开始探索互动小说的世界，这里有几个链接可供你参考：


+ 如上所述，IFDB 和互动小说归档都提供了可浏览的界面，用于浏览超过 40 年价值的互动小说作品。其中大部分可以在 Web 浏览器中播放，但有些需要额外的解释器程序。IFDB 能帮助你找到并安装它们。

  IFComp 的年度结果页面展现了另一个视图，帮助你了解最佳的免费和归档可用作品。

+ 互动小说技术基金会是一个非营利的慈善组织，主要帮助并支持 Twine、IFComp 和互动小说归档的发展，以及提升互动小说的无障碍功能、探索互动小说在教育领域中的应用等等。加入其邮件列表，可以接收 IFTF 的每月资讯，浏览其博客，亦或浏览一些主题商品。

+ 在今年的早些时候，John Paul Wohlscheid 写了这篇关于开源互动小说工具的文章。它涵盖了一些这里没有提及的平台，所以如果你还想了解更多，请看一看这篇文章。

--------------------------------------------------------------------------------

via: https://opensource.com/article/18/7/interactive-fiction-tools

作者：[Jason Mclntosh][a]
选题：[lujun9972](https://github.com/lujun9972)
译者：[cycoe](https://github.com/cycoe)
校对：[校对者ID](https://github.com/校对者ID)

本文由 [LCTT](https://github.com/LCTT/TranslateProject) 原创编译，[Linux中国](https://linux.cn/) 荣誉推出

[a]:https://opensource.com/users/jmac
[1]:http://iftechfoundation.org/
[2]:https://en.wikipedia.org/wiki/Zork
[3]:https://en.wikipedia.org/wiki/The_Hitchhiker%27s_Guide_to_the_Galaxy_(video_game)
[4]:https://en.wikipedia.org/wiki/Infocom
[5]:http://www.springthing.net/
[6]:http://ifcomp.org/
[7]:https://ifcomp.org/comp/2017
[8]:http://www.fiction-interactive.fr/
[9]:http://www.oldgamesitalia.net/content/marmellata-davventura-2018
[10]:/file/403396
[11]:https://opensource.com/sites/default/files/uploads/monkey.png (counterfeit monkey game screenshot)
[12]:http://tads.org/
[13]:https://www.alanif.se/
[14]:http://textadventures.co.uk/quest/
[15]:http://inform7.com/
[16]:https://github.com/DavidKinder/Inform6
[17]:http://inform7.com/learn/man/RB_4_1.html#e307
[18]:/file/403386
[19]:https://opensource.com/sites/default/files/uploads/inform.png (inform 7 IDE screenshot)
[20]:https://www.youtube.com/watch?v=bu55q_3YtOY
[21]:http://ifwiki.org/index.php/Glulx
[22]:http://ifwiki.org/index.php/Z-machine
[23]:https://github.com/erkyrath/lectrote
[24]:https://github.com/garglk/garglk/
[25]:http://eblong.com/zarf/glulx/quixe/
[26]:https://github.com/curiousdannii/parchment
[27]:https://github.com/i7/extensions
[28]:http://twinery.org/
[29]:https://github.com/klembot/twinejs
[30]:/article/18/7/twine-vs-renpy-interactive-fiction
[31]:https://tiddlywiki.com/
[32]:https://github.com/idmillington/undum
[33]:https://github.com/dfabulich/choicescript
[34]:https://www.choiceofgames.com/
[35]:https://github.com/furkle
[36]:https://github.com/lizadaly/windrift
[37]:http://iftechfoundation.org/committees/twine/
[38]:/file/403391
[39]:https://opensource.com/sites/default/files/uploads/harmonia.png (Harmonia opening screen shot)
[40]:https://github.com/iftechfoundation/ifcomp
[41]:https://github.com/iftechfoundation/ifcomp/blob/master/LICENSE.md
[42]:https://www.ifarchive.org/
[43]:http://blog.iftechfoundation.org/2017-06-30-iftf-is-adopting-the-if-archive.html
[44]:https://github.com/iftechfoundation/ifarchive-ifmap-py
[45]:https://www.ifarchive.org/indexes/if-archiveXgames
[46]:http://ifdb.tads.org/search?sortby=ratu&searchfor=%22source+available%22
[47]:https://www.ifarchive.org/indexes/if-archiveXgamesXsource.html
[48]:http://ifdb.tads.org/viewgame?id=fft6pu91j85y4acv
[49]:https://github.com/jmacdotorg/warblers-nest/
[50]:https://github.com/i7/counterfeit-monkey
[51]:https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software
[52]:https://github.com/i7/counterfeit-monkey/blob/master/Counterfeit%20Monkey.materials/Extensions/Counterfeit%20Monkey/Liquids.i7x