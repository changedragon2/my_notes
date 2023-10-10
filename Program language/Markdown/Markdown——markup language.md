# 说明
[Readme](obsidian://open?vault=markdown&file=language%2FReadme)
# 基本 
1. Italics and Bold (斜体和粗体)
    使用下划线 ( _ , underscore) 将单词括起来 <code>_some word_</code>
    	_我是 斜体_
	使用两个星号 ( ** , asterisks) 将单词括起来 <code>**some word**</code>
    	**我是 粗体**
	在同一行可以同时使用粗体和斜体，以及使用它们穿过多个单词 <code>**_some words_**</code>，星号和下划线顺序不重要，但需要嵌套对应
    	_**我既是斜体，也是粗体**_
2. Headers (标题)
    使用井号（#，hash）放在标题前面，几个#代表几级标题，共六级
    	<code># header one</code>
    	<code>## header two</code>
    	<code>### header three</code>
    	<code>#### header four</code>
    	<code>##### header five</code>
    	<code>###### header six</code>
    #### _我是四级标题，而且是斜体_
3. Links (链接)
    inline link (内联链接)
    方括号后紧跟着圆括号，方括号内是链接文本，圆括号内是网址
        <code>[link text](URL)</code>
        [**Blod link text**](URL)
        标题中的链接
    ##### 我是一个带有[链接](URL)的五级标题
    reference link (引用链接)
        <code>[link text][url text]</code>
        <code>[url text]: URL</code>
        [链接1][first-url]
        [链接2][second-url]
[first-url]: www.github.com
[second-url]: www.gnu.org  ^6e9087
4. Image (图像)
    与链接类似，但方括号前有个感叹号（！，exclamation）
    <code>![img text][url to img]</code>
5. Blockquotes (块引用)
    在块引用前使用"大于"插入号（>，greater than caret）
    > "这是一段块引用"
    多段落块引用，在每行前放置插入字符（包括空行）
    块引用可以包含其他 Markdown 元素如斜体，图像或链接
5. Lists (列表)
    无序列表——使用一个星号（*，asterisk）
    * Milk
    * Eggs
    * Salmon
    有序列表——使用数字
    1. 泰拉瑞亚
    2. 星露谷物语
    3.  宝可梦
    列表可以包含斜体、粗体或链接
    镶嵌列表（每一级比上一级多缩进一个空格）
    * Game
     * Terraria
     * Stardew Valley
     * Pokemon
    * Music
     * Silence wang
6. Paragraphs (段落)
    段落内换行——在行末输入两个空格
    段落换行——加入空行
# 额外
###### strikethrough——删除线
~~此文本带有删除线~~
 ```
 ~~This text has a strike through~~
 ```

###### highlight——强调，突出显示
==此文本是突出显示的==
```
==This is highlighted==
```

###### horizontal rule——水平线（紧跟在文本下使用会变成一级标题）

---
```
---
```

###### unordered list——无序列表
- This
- is an
- list
```
- This
- is an
- list
```

###### checklist——清单
- [ ] This
- [ ] is a
- [ ] checklist
     - [ ] Indented check list or sub-task
 ```
     - [ ]This
     - [ ]is a
     - [ ]checklist
         - [ ] Indented check list or sub-task
 ```

###### code blocks——代码块
```lang-name
    ```lang-name
    some code here
    ```
```

###### tables——表格

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```
| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |
```

###### footnotes——脚注
Text[^1] with note[^2]

[^1]: The first word
[^2]: The last word
```
Text[^1] with note[^2]

[^1]: footnote1
[^2]: footnote2
```

###### linking and back linking——链接和反向链接 ^terraria
1. 链接到 obsidian 内某页
[[Markdown——markup language]] 
```
[[Page link]]
```
2. 链接到特定的块
[[Markdown——markup language#^terraria]]
```
[[Page Link^block to link]]
```
3. 链接到特定标题
[[Markdown——markup language#linking and back linking——链接和反向链接 terraria]]
```
[[Page link#The heading]]
```
4. alias——别名
[[Markdown——markup language|Markdown]]
```
[[Page link|alias]]
```
5. 外部链接
[github](https://github.com)
```
[github](https://github.com)
```

###### 镶嵌
1. 镶嵌页面
```
![[Page Name]]
![[Page Name^block to link]]
![[Page Name#heading to link]]
```
2. 镶嵌图片
```
![[picture.jpg]]
```
3. 镶嵌类型
```
1. Markdown files: md
2. Image files: png, jpg, jpeg, gif, bmp, svg
3. Audio files: mp3, web, wav, ogg, 3gp, flac
4. Video files: mp4, webm, ogv
5. PDF files: pdf
```
###### query and search——查询和搜索
```query
Game
```
```
    ```query
    Game
    ```
```
![img](file:///home/change/Pictures/backgrounds/gosch.png)