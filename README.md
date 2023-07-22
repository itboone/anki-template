# anki-template

## 选择题模板

### 模板信息

基础模板是anki的Cloze填空题模板，在卡片背面点击按钮'R'开启/关闭随机选项。

**Question：题目信息**

此处填写题目信息，模板会去除数字和小数点或顿号组合的序号，例如`1.`或`2、`之后根据题目数量重新编号。由于以Anki填空题模板为原型改编，所以题目中必须包含一个填空标签`{{C1:: }}`四个小点后面必须填写一个字符，比如空格、小括号等等，否则移动版会显示这是空白卡片。

**Options：选项列表**

此处填写选项信息。每一行即代表一个选项，每个选项以换行符分割，描述中不能夹杂换行符，如果想在选项中达到换行效果请使用自定义换行符：`[br]`。每个选项开头可带有一个字母和小数点或顿号组成的序号，例如`A.`或`A、`也可以不设选项序号，模板会剔除序号并重新编号，暂只支持`[A-Z]`字母编号，更改源码以实现不同编号需求。

**Answer：预设答案**

此处填写题目预设答案，注意与选项相对应。暂只支持字母作为答案标识，字母不区分大小写，可以设置多个答案，字母前后中间可以夹带其它字符，模板会自动过滤。

**Remark：题目解析**

此处填写题目解析，点击显示答案按钮后会在题目下方显示。

### 传值问题

做选择题模板会涉及到正反卡片传值的问题，对于桌面版窗口对象window不会因为卡片切换而销毁，所以使用window对象共享正反卡片数据即可，但是在移动版anki每切换一个窗口window对象就会销毁，所以这里使用SimonLammer写的Persistence缓存，来实现Anki正反卡片传值。

### 相关依赖

[SimonLammer/anki-persistence](https://github.com/SimonLammer/anki-persistence)

### 版本更新

* 2020.10.12 Anki选择题模板初始版本

* 2021.04.25 修复桌面版切换题目刷新bug

* 2023.07.22 增加开启/关闭随机选项按钮

### 测试版本

桌面版：[Anki 2.1.43](https://github.com/ankitects/anki/releases/tag/2.1.43)

移动版：[AnkiDroid 2.14.6](https://github.com/ankidroid/Anki-Android/releases/tag/v2.14.6)
