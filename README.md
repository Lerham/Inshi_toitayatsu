# Inshi_toitayatsu
B4のとき院試で解いた問題の答案たちを、AI使って文字起こしさせたリポジトリです

## 構成

`tex/main.tex` が答案集全体の入口です。大学、年度、試験・問題の順に分類し、各答案の `answer-body.tex` を読み込みます。

## ビルド

```powershell
Set-Location tex
uplatex main.tex
uplatex main.tex
dvipdfmx main.dvi
```

完成PDFは `output/pdf/大学院数学院試_答案集.pdf` として公開します。

## 院試対策ノート

過去問答案集とは別に、`Inshi_Taisaku_Note/exam.tex` を入口とする院試対策ノートがあります。

```powershell
Set-Location Inshi_Taisaku_Note
latexmk exam.tex
```

完成PDFは `output/pdf/院試対策ノート.pdf` として公開します。`[GANSHO_REPORT]` は公開対象外のため、Gitの追跡から除外しています。


