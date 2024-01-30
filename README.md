# ob-微信读书插件模板大魔改``

你一直在找的微信读书模板:

按照章节排序，按照原文顺序，高亮评论混排，没有高亮的评论(笔记)也能展示，没有高亮、评论的章节不展示“高亮”“评论”的相应板块……已经完全实现。

▶▶*快速通道:直接查看[代码](#代码)*

我一直想找按照章节和原文顺序排列笔记的模板，一直苦等无果，遂贼心四起，搞起代码，几个月前整出一个[雏形](https://forum-zh.obsidian.md/t/topic/26281)，但是发现有一点问题。

作者大人自己有[新版式](https://github.com/zhaohongxuan/obsidian-weread-plugin/discussions/62#discussioncomment-3164134)，可以实现类似功能，不过只能展示已经高亮（划线）的评论，如果做评论的时候没有划线，就也无法展示；这不太方便。

所以我就做了个全新大套件，给大家用用。有问题快来告诉我🌷🌷🌷~
>之前做的那个模板没人用，所以有问题我自己过了几个月才发现呢——主要是章节标题没有按照顺序展示的问题。

我一共做了三个版本满足不同需求。

#### 1.美化混排版
<details>
<summary>点击查看大图</summary>
<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129152557.png style="margin: 0 auto; width: 50%;">
</div>
</details>

#### 2.无格式混排版
<details>
<summary>点击查看大图</summary>
	<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129172330.png style="width: 500px;">
</div>
</details>

#### 3. 无格式分组版
<details>
<summary>点击查看大图</summary>
	<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129172738.png style="width: 500px;">
	</div>
</details>



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

如果想看具体的功能说明和拓展做笔记的用法，可以看Wiki页面。


## 代码
###### 美化混排版
+ nunjucks
+ css
###### 无格式混排版
###### 无格式分组版 
