# pandoc-report-env
ワテの大学用レポート環境だお（ ＾ω＾）

## pandocのインストール
ArchLinuxを使ってるのでyayとか使いますが,お好きなディストロに読み替えてもらってokです。

- pandocとpandoc-crossrefをインストール
- TeXもインストールしておく（最低限の日本語環境がOKだと思う）
- バイナリだとHaskellの依存関係をｲﾝｽｺしなくて済むので、可能ならばそっちのほうが良いかも。

```
# Debuan GNU/Linux | Ubuntu
sudo apt install pandoc cabal-install
sudo cabal install --global pandoc-crossref

# Fedora | Alma Linux etc...
sudo dnf install pandoc

# ArchLinux | Manjaro Linux etc...
yay -S pandoc-bin
yay -S pandoc-crossref-bin

```

## 書く
- もりもり書いていこう
- 表紙は以下のようにして書く
```
---
documentclass: ltjsarticle
title: 題名
author:
    id:   A00020001     # 学籍番号
    name:   名前　無胃
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

