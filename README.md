# ob-微信读书插件模板大魔改

⚜你一直在找的**微信读书模板**:

+ 按照`章节排序`，按照`原文顺序`，`高亮评论混排`，
+ 没有高亮的评论(笔记)也能展示
+ 没有高亮、评论的章节不展示“高亮”“评论”的相应板块……

![演示图](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E9%A6%96%E9%A1%B5%E5%B1%95%E7%A4%BA%E5%9B%BE)




> [!NOTE]
>+ 我一直想找按照章节和原文顺序排列笔记的模板，苦等无果，贼心四起，搞起代码，几个月前整出一个[雏形](https://forum-zh.obsidian.md/t/topic/26281)，但是发现有一点问题。
>+ 作者大人自己有[新版式](https://github.com/zhaohongxuan/obsidian-weread-plugin/discussions/62#discussioncomment-3164134)，可以实现类似功能，不过只能展示已经高亮（划线）的评论，如果做评论的时候没有划线，就也无法展示；这不太方便。
>+ 所以我就做了个全新大套件，给大家用用。有问题快来告诉我🌷🌷🌷~
>>+ 之前做的那个模板没人用，所以有问题我自己过了几个月才发现呢——主要是章节标题没有按照顺序展示的问题。
>>
>>  

## 我一共做了三个版本满足不同需求。

1. `美化混排版`
<details>
<summary>点击查看大图</summary>
<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129152557.png style="margin: 0 auto; width: 50%;">
</div>
</details>

2. `无格式混排版`
<details>
<summary>点击查看大图</summary>
	<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129172330.png style="width: 500px;">
</div>
</details>

3. `无格式分组版`
<details>
<summary>点击查看大图</summary>
	<div align=center>
<img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129172738.png style="width: 500px;">
	</div>
</details>



|                                  | **美化混排版** | **无格式混排版** | **无格式分组版** |
| -------------------------------- | -------------- | ---------------- | ---------------- |
| 高亮[^1]                             |🌷             |🌷 |🌷 |
| 评论[^2].                                |🌷  |🌷 |🌷 |
| 章节评论[^3].                        |🌷  |🌷 |🌷 |
| 书籍评论[^4].                       |🌷  |🌷 |🌷 |
| blockid                          |🌷  |🌷 |🌷 |
| 时间日期显示                     |🌷  |🌷 |🌷 |
| 笔记按章节排序                   |🌷  |🌷 |🌷 |
| 章节内按笔记类型排序[^5].                | ✖️          | ✖️            |🌷 |
| 章节内按原文顺序排序[^6].         |🌷  |🌷 | ✖️            |
| 笔记设置了特殊css格式？          |🌷  | ✖️            | ✖️            |
| 既“高亮”又“评论”的笔记展示一次？ |🌷  |🌷 | ✖️            |

以下以`美化混排版`为例，详细讲解**功能**和**拓展用法**。也可以🌟💨*快速通道:直接查看[代码](#代码)


[^1]: 空板块不生成。
[^2]: 空板块不生成。
[^3]: 空板块不生成。
[^4]: 空板块不生成。
[^5]: 即章节内，”高亮“、”评论“、”章节评论“分别生成板块
[^6]: 即章节内，”高亮“、”评论“、”章节评论“板块混在一起，按照原文顺序排列


## 代码
1. `美化混排版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E7%BE%8E%E5%8C%96%E6%B7%B7%E6%8E%92%E7%89%88nunjucks)
+ [css](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E7%BE%8E%E5%8C%96%E6%B7%B7%E6%8E%92%E7%89%88css)
2. `无格式混排版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E6%97%A0%E6%A0%BC%E5%BC%8F%E6%B7%B7%E6%8E%92%E7%89%88nunjucks)
3. `无格式分组版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E6%97%A0%E6%A0%BC%E5%BC%8F%E5%88%86%E7%BB%84%E7%89%88nunjucks)
