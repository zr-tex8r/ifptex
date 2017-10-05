ifptex パッケージバンドル
=========================

TeX: エンジンが pTeX（やその派生）であるかを判定する

ifptex パッケージは ifxetex や ifluatex 等のパッケージの pTeX 版に
相当する。ifuptex パッケージは ifptex の別名で、後方互換性のために
用意されている。

### システム要件

  - TeX フォーマット： plain TeX、LaTeX （および他の plain 互換なもの）
  - TeX エンジン： 不問
  - DVI ウェア（DVI 出力時）： 不問

### インストール

TDS 1.1 に準拠するシステムの場合、以下のようにファイルを移動する：

  - `*.sty` → $TEXMF/tex/latex/ifptex

この後必要に応じて mktexlsr を実行する。

ifptex パッケージ ― pTeX 系エンジンの判定
------------------------------------------

### パッケージ読込

plain TeX の場合：

    \input ifptex.sty

LaTeX の場合：

    \usepackage{ifptex}

### 機能

注意：e-TeX拡張の有無は区別されない。

  * `\ifpTeX`（又は `\ifptex`）［if-トークン］  
    pTeX（upTeX、pTeX-ng を含む）を使っているか。
  * `\ifstrictpTeX`（又は `\ifstrictptex`）［if-トークン］  
    pTeX（upTeX、pTeX-ng ではなく）を使っているか。
  * `\ifupTeX`（又は `\ifuptex`） ［if-トークン］  
    upTeX（pTeX-ng を含む）を使っているか。
  * `\ifstrictupTeX`（又は `\ifstrictuptex`） ［if-トークン］  
    upTeX（pTeX-ng ではなく）を使っているか。
  * `\ifnativeupTeX` ［if-トークン］  
    upTeX を内部文字コードが Unicode の状態で使っているか。  
  * `\ifpTeXng`（又は `\ifptexng`）［if-トークン］  
    pTeX-ng を使っているか。  
    ※一応 `\ifstrictpTeXng`（`\ifstrictptexng`）もある。
  * `\RequirepTeX`  
    `\ifpTeX` 不成立の場合はエラーを出す。
  * `\RequireStirctpTeX`  
    `\ifstrictpTeX` 不成立の場合はエラーを出す。
  * `\RequireupTeX`  
    `\ifupTeX` 不成立の場合はエラーを出す。
  * `\RequireStrictupTeX`  
    `\ifstrictupTeX` 不成立の場合はエラーを出す。
  * `\RequireNativeupTeX`  
    `\ifnativeupTeX` 不成立の場合はエラーを出す。
  * `\RequirepTeXng`  
    `\ifpTeXng` 不成立の場合はエラーを出す。  
    ※一応 `\RequireStrictpTeXng` もある。


ifuptex パッケージ ― ifptex の別名
-----------------------------------

ただ単に ifptex を読み込むだけのパッケージであり、0.2 版との後方互換性の
ために用意されている。

### パッケージ読込

plain TeX の場合：

    \input ifuptex.sty

LaTeX の場合：

    \usepackage{ifuptex}


更新履歴
--------

  * Version 1.2c 〈2017/10/04〉
      - バグ修正。
  * Version 1.2b 〈2017/09/20〉
      - バグ修正。
  * Version 1.2a 〈2017/09/15〉
      - (試験的) `漢字コード=UTF-8` 機能を追加。
  * Version 1.2  〈2017/09/09〉
      - `\ifstrictupTeX`、`\RequireStrictupTeX` を追加。
  * Version 1.1  〈2017/05/04〉
      - 細かい調整。
  * Version 1.0  〈2013/04/29〉
      - 独立のバンドルに移動。
      - パッケージ名を ifptex に変更して、pTeX 判定機能を付加。
      - (試験的) upTeX の版判定機能を追加。
  * Version 0.2  〈2008/03/14〉
      - 最初の公開版。

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
