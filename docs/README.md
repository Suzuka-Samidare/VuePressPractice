# 描画まとめ

## 目次
VuePressでは、h2見出し以下が目次対象として反映される
[[toc]]

## 見出し
# h1
## h2
### h3
#### h4
##### h5
###### h6

## 箇条書き
- 我那覇響
  - 名前
    - 名字
      - がなは
    - 名前
      - ひびき
  - 身長
    - 152cm
  - 血液型
    - A型

## 画像表示
### 大きさ指定なし
```markdown
![GANAHA](/ganaha.PNG)
```
または
```html
<img src="/ganaha.PNG">
```
![GANAHA](/ganaha.PNG)

### 横幅指定
```html
<img src="/ganaha.PNG" width="200px">
```
<img src="/ganaha.PNG" width="200px">

### 並べる
```html
<img src="/ganaha.PNG" width="200px"><img src="/ganaha.PNG" width="200px"><img src="/ganaha.PNG" width="200px">
```
<img src="/ganaha.PNG" width="200px">
<img src="/ganaha.PNG" width="200px">
<img src="/ganaha.PNG" width="200px">

### きれいに並べる
```html
<div style="text-align: center;">
  <div style="display: inline-block;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
  </div>
</div>
```
<div style="text-align: center;">
  <div style="display: inline-block;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
    <img src="/ganaha.PNG" width="30%" style="padding: 0px 10px;">
  </div>
</div>

## 番号付きリスト
1. 765
2. 283
3. 346

## 引用
> ヤヴァイ

## 二重引用
> nyaa
>> myaa

## 区切り

block1

---

block2

---

## 書体
ここは、*斜体*にしてる

ここは、**強調**にしてる

~~あーそういうことね。完全に理解した~~

## 絵文字
:tada: :100:

## リンク
[スターリットシーズン](https://starlit-season.idolmaster.jp/)

直書きは自動的にリンク生成されない
https://starlit-season.idolmaster.jp/＼

## コード
### 単一行
`はいさーい！！`

### 複数行
- 言語の指定で色分け
- 左側に行番号表示可能
- 行番号を指定して強調表示可能

```js{18}
<script>
import { getIdolProfile } from '../api/sampleData'

export default {
  data () {
    return {
      idolList: [],
      viewData: [],
      loading: false
    }
  },
  methods: {
    test () {
      this.idolList = []
      this.loading = true
      getIdolProfile()
        .then(res => {
          this.idolList = res.data.results.bindings
        })
        .catch(err => {
          alert(err)
        })
        .finally(() => {
          this.loading = false
        })
    }
  }
}
</script>
```

## テーブル
|header1|header2|header3|
|:--|--:|:--:|
|align left|align right|align center|
|a|b|c|

## カスタムコンテナ
::: tip
これはチップです。
:::

::: warning
これは警告です。
:::

::: danger 注意するべき点
これは危険な警告です。
:::

## SPAリンク
[アイドル一覧](/idol/)

