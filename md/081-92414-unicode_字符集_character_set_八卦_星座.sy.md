---
show: step
version: 1.0
enable_checker: true
---

# unicode

## 回忆上次内容

- 中国的简体和繁体汉字
	- 字符数量都超级大
	- 彼此还认对方为乱码
- 如果有一种编码所有的字符都能编进去就好了
  - 中日韩(CJK)
  - 欧洲拼音
  - 梵文
  - 阿拉伯文
  - 卢恩字符
  - 等等等都包括进去

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221120-1668910380061)

- 能有么？🤔

### 回顾历史

- 计算机中只有 `0` 和 `1`
  - 并且是存储在字节里的
  - 原来只能表示和处理数字
  - 字符无法处理
- 后来某些二进制数固定下来代表某个字符
  - 形成了字符集 
  - 从博多码(5bits)到 BCDIC(6bits)
  - 再到 EBCDIC码(8bits) 最后统一于 `ascii`

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614479268989)

- 但是各国家和地区都有自己的字符
  - 这一领域没有统一的标准
  - 所以每个国家和地区指定自己的标准
  - 想要同时显示法语字符和希伯来字符是不可能的
  - 同样字节状态在不同编码格式里代表不同的字符
  - 都认为对方是乱码
  - 彼此不兼容
  - 编码方式有上百种之多

### 分久必合

- 无法解决的问题背后其实可能是机会
- Xerox(施乐公司) 在 1980 年代开始尝试一种编码能融合多语言
  - Xerox 字符集包括
	- 拉丁
	- 阿拉伯
	- 希伯来
	- 希腊
	- 西里尔
	- 中日韩字符

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221022-1666445734877)

- 这个字符集 1988 年进化为 unicode
	- uni的意思是一

### uni

- uni 来自于
    - unique
    - unified
    - universal
    - unicorn
    - university
    - uniform
    - unit
    - union

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220515-1652607479811)

- uni-开头的单词都有这个特点

### universe

- universe
	- 绕着一个东西转的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221125-1669372520523)

- 后来日语universe翻译成宇宙
- 宇宙一词古中文就有
	- 上下四方曰宇
	- 古往今来曰宙


### 得一

- 这个词头计算机领域也有很多很牛的单词
    - unity、unit、unix
- 这名字得一了啊
    - 少则得,多则惑,是以圣人抱一为天下式
    - 天得一以清，地得一以宁，神得一以灵，谷得一以盈，万物得一以生，侯王得一而以为正
- 这个版本叫做 unicode88，是 16 位的 unicode
  - 1989 年 Unicode 这个工作组来了一些从大厂来的人，微软和 sun 都来了
  - 1991/1/3 日，Unicode 委员会在加州成立
  - 1991 年 8 月，unicode 第一卷发布
  - 1992 年 6 月，第 2 卷发布，这里面包含了汉语字符
  - Adobe, Apple, Facebook, Google, IBM, Microsoft, Netflix 和 SAP SE 加入 unicode 委员会

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614481940908)

- 字符的全球标准化开始了

### 基础字符

- ascii还是牢牢占据着0-127这最关键的位置
- 紧挨着 ascii 的字符的就是 Latin-1
  - 他是由 iso-8859-1 西欧、北欧字符集进化而来

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614486021235)

- 这其实也暗示出unicode的编码排序规则
- 以书写系统为单位来分类和收录

### 各种拼音文字

- 比如卢恩字符

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230101-1672566676009)

- 我们去捋一捋拉丁字符进化过程吧

### 拉丁字符进化史

|  发音 | 词义 | 埃及圣书体 | 楔形写法 | 希腊字符 | 拉丁字符 |
|---|---|---|---|---|---|
|  alpha | 牛 | 𓃾 | 𐤀 | Αα | Aa | 
| beta | 房子 | 𓉐 | 𐤁 | Ββ | Bb |
| gīml | 扔棍子 | 𓌙 | 𐤂 |  	Γγ   |	Cc,Gg |
| dālet | 门或者鱼 | 𓉿  | 𐤃‎ | Δδ  | Dd |

- 去看看他们的序号

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230102-1672669238226)

- 希腊字符比较好找
	- 序号较小
- 不过希腊字符之前只有大写字母
	- 小写字母怎么来的呢？

### 小写字母

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230102-1672669748090)

- 固定的画风又被印刷术再次固定

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230102-1672669781153)

- 能找到埃及文字的序号吗？

### 埃及文字

- unicode 确实给埃及文字排了序号
	- 但是序号很大
	- 而且目前终端没有字型支持

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20230102-1672669173026)

- 字形实现难度很高
	- 实际需求也不确定


- 同为拼音文字的种种书写系统
	- 可能用长得一样的字符
	- 会是一个序号吗？

### 书写系统

- 英文拉丁字母、西里尔文字母
	- 都来自希腊文字母
- 不同的书写系统
	- 可能会长相一样的字母
	- 但对应着不同的序号

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665541895851)

- 虽然字形一模一样
	- 但是属于三个书写系统
		- 希腊文字母
		- 英文字母
		- 西里尔字母

### 持续进化

- 每个版本都会有些变化
  - 整个编码区域分成若干个 blocks
  - 新版本对于这些 blocks 里面的字符有所增加

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614482179744)

- 除了字符之外还有很多符号
	- 比如十二个星座

### 十二星座

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220706-1657077784482)

- 集装箱标准化一旦开始
	- 就会反过来约束火车轮船飞机
- 你要想加入这个交流的行列
	- 必须要先从遵守现有的规则开始
- 新编码unicode的时代来了
	- 他会把一切字符吸收进去

### 阴阳太极

- 易有太极
	- ️☯

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20210228-1614482724842)

- 是生两仪
	- ⚊ 陽 (U+268A) ⚋ 陰 (U+268B)
- 两仪生四象
	- ⚌(太陽,U+268C)、⚍(少陰,U+268D)、⚎(少陽,U+268E)、⚏(太陰,U+268F)

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913117031)

### 八卦

- 四象生八卦
	- ☰ ☱ ☲ ☳ ☴ ☵ ☶ ☷

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651912743635)

- 如果把
	- ⚊ 陽 (U+268A)当做1
	- ⚋ 陰 (U+268B)当做0
- 顺序是逆序(递减)
- 从外而内
	- 天
	- 泽
	- 水
	- 雷
	- 风
	- 火
	- 山
	- 地

- 八卦有了
	- 可以重卦么？

### 重卦

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913261981)

- 八八六十四卦

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220211-1644564209397)

- 看起来都可以玩算卦了
- 还能做什么呢？

### 乱来

- 来随便试一个

```python
print("\u9999")
```

- 看看这是什么字？

### 中日韩字符

- 中文编码原来是 gbk

- unicode 现在unicode把中日韩(CJK)当成一组
	- 排序是CJK
	- 位置是unicode.org下方的code chart中找到

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220710-1657448172896)

- 当然关于排序各有各的排法
	- 中国是中日韩
	- 日本是日中韩
	- 韩国是韩中日
- unicode组织的CJK显然综合了东亚文化圈的排名
	- 我仿佛听到卡吉玛

### 所在位置

- 象形文字数量确实是拼音文字没有办法比的

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220710-1657448246051)

- 他们听到我们有两万个字母的时候都傻了

### 融合而来

- unicode中的文字将
	- 中国汉字
	- 朝鲜汉字
	- 日本汉字
	- 综合起来

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221012-1665543002765)

- 得到一个汉字
- 那如果有很多异体字怎么办？

### 回字的几种写法

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221112-1668213852027)

- 这些都是异体字
- 或者叫做通假字
- 在计算机里是如何的呢？

### 茴香豆

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221112-1668213947444)

- 在0x4e00到0x9fff这个范围内
- 基本一个汉字就只有一种写法

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20221112-1668213889472)

- 所有的汉字里面第一个是什么呢？

## 总结

- 字符集
	- 从博多码
	- 到 `ascii` 
	- 再到 `8859`
	- 各自割据
- 如何把世界上各种字符统进行编码
  - `unicode`顺势而生不断进化
  - 不过字符总量超过了`65536`
  - 每个汉字都有位置

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651913535341)

- 所有汉字里面第一个汉字是什么呢？
- 我们下次再说！👋

![图片描述](https://doc.shiyanlou.com/courses/uid1190679-20220507-1651928336667)

