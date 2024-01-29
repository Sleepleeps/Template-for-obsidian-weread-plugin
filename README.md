# Template-for-obsidian-weread-plugin
Template for obsidian weread plugin
# ob-微信读书插件模板大魔改``

你一直在找的微信读书模板:

<mark style="background: #ABF7F7A6;">按照章节排序，按照原文顺序，高亮评论混排，没有高亮的评论(笔记)也能展示，没有高亮、评论的章节不展示“高亮”“评论”的相应板块</mark>……已经完全实现。

▶▶*快速通道:直接查看[内容介绍](#内容介绍)*

我一直想找按照章节和原文顺序排列笔记的模板，一直苦等无果，遂贼心四起，搞起代码，几个月前整出一个雏形❓❓❓，但是发现有一点问题。

作者大人自己有[新版式](https://github.com/zhaohongxuan/obsidian-weread-plugin/discussions/62#discussioncomment-3164134)，可以实现类似功能，不过只能展示已经高亮（划线）的评论，如果做评论的时候没有划线，就也无法展示；这不太方便。

所以我就做了个全新大套件，给大家用用。有问题快来告诉我🌷🌷🌷~
>之前做的那个模板没人用，所以有问题我自己过了几个月才发现呢——主要是章节标题没有按照顺序展示的问题。

接下来你会看到：几个版式，功能详情，以及拓展用法。
# 内容介绍

## 版式
我一共做了三个版本满足不同需求。
1. **美化混排版**
	+ ![[Pasted image 20240129152557.png]]
2. **无格式混排版**
3. **无格式分组版**

|                                  | **美化混排版** | **无格式混排版** | **无格式分组版** |
| -------------------------------- | -------------- | ---------------- | ---------------- |
| 高亮 ^[空板块不生成]                             |🌷             |🌷 |🌷 |
| 评论  ^[空板块不生成]                                 |🌷  |🌷 |🌷 |
| 章节评论   ^[空板块不生成]                          |🌷  |🌷 |🌷 |
| 书籍评论     ^[空板块不生成]                         |🌷  |🌷 |🌷 |
| blockid                          |🌷  |🌷 |🌷 |
| 时间日期显示                     |🌷  |🌷 |🌷 |
| 笔记按章节排序                   |🌷  |🌷 |🌷 |
| 章节内按笔记类型排序  ^[即章节内，”高亮“、”评论“、”章节评论“分别生成板块]                | ✖️          | ✖️            |🌷 |
| 章节内按原文顺序排序 ^[即章节内，”高亮“、”评论“、”章节评论“板块混在一起，按照原文顺序排列]         |🌷  |🌷 | ✖️            |
| 笔记设置了特殊css格式？          |🌷  | ✖️            | ✖️            |
| 既“高亮”又“评论”的笔记展示一次？ |🌷  |🌷 | ✖️            |

我将使用“美化混排版”来讲解。

## 美化混排版

###### 1. **章节顺序**：
+ 按照章节顺序展示高亮和评论，而不是分成两个部分；
###### 2. **原文顺序**：
+ 章节标题下，按照原文顺序展示高亮和评论;
+ ![[Pasted image 20240129153610.png]]
###### 3. **高亮评论不重复**：
+ 同一段话，如果同时“高亮+评论”，只出现一次；
###### 4. **书籍详情卡**：
+ 书记详情卡图片点击一下会生成跳转链接，创立一个细读文件，方便新做关联。
	+ ![[生成双链精度笔记.gif]]
	+ 不喜欢可以自行去掉这句(<{{metaData.title}}细读>)；
	+ （）内替换成{{metaData.cover}}，就可以点击图片看到封面大图，方便下载；
	+ 如果未来作者提供了{{metaData.url}}变量，替换之后就可以直接跳转到书的网页链接；
###### 5. **callout优化**：
+ 用callout重新规划了页面的布局，同时做了callout优化，如果原文是分段的，在你的笔记里也是同样的格式。
+  如果你不喜欢我的callout，或者怕麻烦，可以直接修改成系统自带的。
+ 如下：
	+ *我的callout版式*：分段的内容还在标题栏![[Pasted image 20240129154904.png]]
	+ *普通callout版式*：分段的内容会直接到callout的内容栏![[Pasted image 20240129155207.png]]
###### 6. 页面美化：
+  笔记开始的时候列出标题、作者和简介，可以使得书本内容一目了然；
+ 书籍详情卡片视图，方便查看，也方便截图分享；
- 当鼠标停留在词条上，会有悬浮卡片的效果，同时在右下角显示创建日期，更有互动感；
		![[鼠标悬浮效果.gif]]
## 拓展用法

###### 1. 标签法：

我的版本中，因为是混合排列，所以并没有给“高亮”和“评论”加标题；而且我通过不同的callout已经实现了区分。如果后期想要分类查看，可以加标签。代码可以这样修改，评论部分也是这样。
```
>[!weread4] {{ note.data.markText | trim | replace('\n', '<br>') }} ^{{ note.data.chapterUid }}-{{ note.data.range }} 
>- {{note.data.createTime}} #高亮
>{{ '---' }}
```
###### 2. 双链法：

在阅读中，对于要进一步查阅的地方，直接评论的时候就打上双链标签，这样返回的时候笔记就会生成双链。
**Step 1**
![[Pasted image 20240129133915.png]]
**Step 2:**
![[Pasted image 20240129164516.png]]
**Step 3:**
为了进一步使用这个双链，你可以使用dataview插件的内联语句，在代码中加上这一句话：
=filter(this.file.outlinks,(x) => meta(x).display != "cover"),这样你就可以看到这个笔记的未完成事项。
![[dataviw内联代码.gif]]

注：meta(x).display != "cover"是我之前设置的，笔记封面自动双链一个《{{书名}}细读笔记》（<{{metaData.title}}细读>)）的文档。在这段代码里，我把这个文档过滤了，剩下的筛选出来的，就是自己看书生成的笔记双链。

如果你不想生成《{{书名}}细读笔记》这个文档，可以直接删除这行代码，那么dataview的内联代码就改成：=this.file.outlinks

`
## 代码
