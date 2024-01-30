# ob-微信读书插件模板大魔改

⚜你一直在找的**微信读书模板**:

+ 按照`章节排序`，按照`原文顺序`，`高亮评论混排`，
+ 没有高亮的评论(笔记)也能展示
+ 没有高亮、评论的章节不展示“高亮”“评论”的相应板块……
+ 
⚜**全文导览**
+ [三个版本](#我一共做了三个版本满足不同需求)|[功能演示](#美化混排版为例)|[拓展用法](#拓展用法)| [代码](#代码)
 

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

## 美化混排版为例
1. 章节顺序：
按照章节顺序展示高亮和评论，而不是分成两个部分；
2. 原文顺序：
   章节标题下，按照原文顺序展示高亮和评论;
   
   <details>
   <summary>点击查看大图</summary>
	<div align=center>
   <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129153610.png style="width: 500px;">
        </div>
   </details>

4. 高亮评论不重复：
   同一段话，如果同时“高亮+评论”，只出现一次；
5. 书籍详情卡：
   书记详情卡图片点击一下会生成跳转链接，创立一个细读文件，方便新做关联。
   <details>
     <summary>点击查看大图</summary>
	<div align=center>
     <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/%E7%94%9F%E6%88%90%E5%8F%8C%E9%93%BE%E7%B2%BE%E5%BA%A6%E7%AC%94%E8%AE%B0.gif style="width: 
       500px;">
        </div>
   </details>
   
7. callout优化：
   用callout重新规划了页面的布局，同时做了callout优化，如果原文是分段的，在你的笔记里也是同样的格式。
   如果你不喜欢我的callout，或者怕麻烦，可以直接修改成系统自带的。
   如下：
   + 我的callout版式：分段的内容还在标题栏
     
      <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129154904.png style="width: 
              500px;">
    
   
   + 普通callout版式：分段的内容会直接到callout的内容栏
     
     <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129155207.png style="width: 
       500px;">
  
   
8. 页面美化：
   + 笔记开始的时候列出标题、作者和简介，可以使得书本内容一目了然；
   + 书籍详情卡片视图，方便查看，也方便截图分享；
   + 当鼠标停留在词条上，会有悬浮卡片的效果，同时在右下角显示创建日期，更有互动感；
   + <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/%E9%BC%A0%E6%A0%87%E6%82%AC%E6%B5%AE%E6%95%88%E6%9E%9C.gif style="width: 
       500px;">

## 拓展用法
1. 标签法：
   我的版本中，因为是混合排列，所以并没有给“高亮”和“评论”加标题；而且我通过不同的callout已经实现了区分。如果后期想要分类查看，可以加标签。代码可以这样修改，评论部分也是这样。
   ```
   >[!weread4] {{ note.data.markText | trim | replace('\n', '<br>') }} ^{{ note.data.chapterUid }}-{{ note.data.range }} 
   >- {{note.data.createTime}} #高亮
   >{{ '---' }}
   ```
   
2. 双链法：
   在阅读中，对于要进一步查阅的地方，直接评论的时候就打上双链标签，这样返回的时候笔记就会生成双链。
   + **Step 1**
     
       <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129133915.png style="width: 
       500px;">
       
   + **Step 2:**
  
       <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/Pasted%20image%2020240129164516.png style="width: 
       500px;">

   + **Step 3:**
     为了进一步使用这个双链，你可以使用dataview插件的内联语句，在代码中加上这一句话，就可以看到这个笔记的关联事项。
     ```
     `=filter(this.file.outlinks,(x) => meta(x).display != "cover")`
     ```
       <img src=https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/pic/dataviw%E5%86%85%E8%81%94%E4%BB%A3%E7%A0%81.gif style="width: 
       500px;">

       注：meta(x).display != "cover"是我之前设置的，笔记封面自动双链一个《{{书名}}细读笔记》（<{{metaData.title}}细读>)）的文档。在这段代码里，我把这个文档过滤了，剩下的筛选出来的，就是自己看书生成 
 的笔记双链。

       如果你不想生成《{{书名}}细读笔记》这个文档，可以直接删除这行代码，那么dataview的内联代码就改成：
       ```
       `=this.file.outlinks`
       ```

## 代码
1. `美化混排版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E7%BE%8E%E5%8C%96%E6%B7%B7%E6%8E%92%E7%89%88nunjucks)
+ [css](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E7%BE%8E%E5%8C%96%E6%B7%B7%E6%8E%92%E7%89%88css)
+ 字体
+ + [猫啃网糖圆体](https://www.maoken.com/tangyuan)
  + [秋空黑体](https://www.maoken.com/freefonts/13086.html)
  + [霞鹜新晰黑](https://www.maoken.com/freefonts/8999.html)
2. `无格式混排版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E6%97%A0%E6%A0%BC%E5%BC%8F%E6%B7%B7%E6%8E%92%E7%89%88nunjucks)
3. `无格式分组版`
+ [nunjucks](https://github.com/Sleepleeps/Template-for-obsidian-weread-plugin/blob/main/%E6%97%A0%E6%A0%BC%E5%BC%8F%E5%88%86%E7%BB%84%E7%89%88nunjucks)
