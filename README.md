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


