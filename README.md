# pandoc-report-env
あたいの大学用レポート環境だお（ ＾ω＾）

## pandocのインストール
ArchLinuxを使ってるのでyayとか使いますが,お好きなディストロに読み替えてもらってokです。

- AURからpandocのバイナリとcrossrefのバイナリをインストール
- バイナリだとHaskellの依存関係をｲﾝｽｺしなくて済むので気が楽
```
yay -S pandoc-bin
yay -S pandoc-crossref-bin

```

## 書く
- もりもり書いていこう
- mdの頭にこれ付けるといいよ
```
---
documentclass: ltjsarticle
title: 題名
author:
    id:   YJSNPI114514
    name:   山本　太郎
    email:  oketsumarudashi@mail.jp
lecture:
    deadline: 1970年10月10日
geometry:
  - margin=1in
papersize: a4
linestretch: 0.5
figureTitle: "図 "
tableTitle: "表 "
listingTitle: "コード"
figPrefix: "図"
eqnPrefix: "式"
tblPrefix: "表"
lstPrefix: "コード"
fontsize: 11pt
code-block-font-size: 10pt
---
```
## 実行

 ```
 pandoc HOGE.md -o HOGE.pdf --template=template.tex -F pandoc-crossref --pdf-engine=lualatex -N --highlight-style=tango
 ```

