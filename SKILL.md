# 三语翻译（中式英语过渡法）

## Purpose
英文长难句阅读拆解工具。把英文嵌套结构拆成平铺短句，用一套不讲语法的"中式英语"做人脑理解的中间过渡层，一眼看懂英文句子含义。**只为阅读理解，不用于对外交流。**

触发：用户要求按"中式英语过渡法"翻译/拆解英文，或扔英文长句要求三段式输出时。

## 核心规则

### 1. 选词规则
从原文提取有实际含义的单词，**无意义虚词（the/a/is/are/of 等）可以直接省略**，不用罗列原文所有单词。

### 2. 语序规则
保留的单词按**中文说话语序**重排：先说修饰描述，再抛出主体名词，**主谓宾主干必须相邻，不被长修饰隔开**。

### 3. 从句拆分（最重要）
名词后带从句修饰时：
- **重复书写该核心名词**，拆成多段短句；
- 每段短句内部主谓宾紧邻；
- 消除嵌套，不用在大脑里缓存名词、找断点。

底层类比：英文 = 面向对象（先实例对象，挂一堆属性，最后调动作）；中式英语 = 平铺过程式代码（多段独立主谓宾短句）。

### 4. 输出格式（强制三段式）
```
英文原文：
中式英语：
标准中文：
```

### 5. 禁止事项
- 不要生成符合英语语法的句子。
- 不要保留长嵌套结构；后置定语从句优先拆分、重复名词。
- 不要把主谓宾拆开。

## Workflow
1. 读原句，定位主句主干（谁-做-什么），标出所有从句修饰边界。
2. 提取实义单词，扔掉虚词。
3. 遇到"名词+从句"：重复该名词，拆成两段（先讲从句内容，再讲主句动作）。
4. 按中文语序排每段：时间/修饰在前，主体名词随后，谓语宾语紧贴。
5. 按三段式输出，检查每段主谓宾是否相邻。

## 示例
> 英文原文：The man who you bought yesterday cues another slave.
> 中式英语：you yesterday bought that man, that man cues another slave
> 标准中文：你昨天买下的那个男人，暗示另一个奴隶。

> 英文原文：The cat that I rescued last night sits on the roof.
> 中式英语：I last night rescue that cat, that cat sits on roof
> 标准中文：我昨晚救下的那只猫，坐在屋顶上。

> 英文原文：The candidate who the team interviewed last week will join the project next month.
> 中式英语：team last week interviewed that candidate, that candidate next month joins the project
> 标准中文：团队上周面试的那位候选人，下个月加入项目。

中文原文输入时同样适用：先给出对应的英文，再按同样规则做中式英语拆解。

> 标准中文：那是几个身材魁梧的汉子，全身包裹在暗沉的铁甲里，头盔下的眼睛锐利如鹰，手中的长枪枪尖泛着幽冷的寒光。
> 英文：There were several burly men, their whole bodies wrapped in dark, dull iron armor, eyes under their helmets sharp as eagles', the spear tips in their hands gleaming with a cold, eerie light.
> 中式英语：there stand several burly men, men whole body wrapped in dark dull iron armor, helmet under eyes sharp like eagle, men hands hold long spears, spear tips gleam cold eerie light

## 踩坑记录
- 定语从句的关系代词（who/that/which）是虚词，直接扔掉，不要试图在中式英语里保留。
- 时态不用纠结：中式英语不讲语法，过去时态用时间状语（yesterday/last night）表达即可，动词用原形。
- 一句话里多个从句嵌套时，从最内层开始拆，一层一层向外铺平。
- 中式英语里允许出现中文标点和 that 指示代词，一切以"一眼看懂"为准。
