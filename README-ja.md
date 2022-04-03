ifptex パッケージバンドル
=========================

TeX: エンジンが pTeX（やその派生）であるかを判定する

ifptex パッケージは ifxetex や ifluatex 等のパッケージの pTeX 版に
相当する。ifuptex パッケージは ifptex の別名で、後方互換性のために
用意されている。

### システム要件

  * TeX フォーマット： plain TeX、LaTeX、INI モード
  * TeX エンジン： 不問
  * DVI ウェア（DVI 出力時）： 不問
  * 依存パッケージ：
      - iftex

### インストール

TDS 1.1 に準拠するシステムの場合、以下のようにファイルを移動する：

  - `*.sty` → $TEXMF/tex/generic/ifptex

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

  * `\ifptex`（又は `\ifpTeX`）［if-トークン］  
    pTeX（upTeX、pTeX-ng を含む）を使っているか。
  * `\ifstrictptex`（又は `\ifstrictpTeX`）［if-トークン］  
    pTeX（upTeX、pTeX-ng ではなく）を使っているか。
  * `\ifuptex`（又は `\ifupTeX`） ［if-トークン］  
    upTeX（pTeX-ng を含む）を使っているか。
  * `\ifstrictuptex`（又は `\ifstrictupTeX`） ［if-トークン］  
    upTeX（pTeX-ng ではなく）を使っているか。
  * `\ifnativeuptex`（又は `\ifnativeupTeX`） ［if-トークン］  
    upTeX を内部文字コードが Unicode の状態で使っているか。  
  * `\ifptexng`（又は `\ifpTeXng`）［if-トークン］  
    pTeX-ng を使っているか。  
    ※一応 `\ifstrictptexng`（`\ifstrictpTeXng`）もある。
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
  * `\upTeXguessedversion` ［mathchardef-トークン］  
    upTeX のバージョンの推測値（を百倍した整数値）。  
    ※1.23版以降では常に正確なバージョン値が得られる。  
    ※upTeX 以外のエンジンでは 0 になる。
  * `\RequireupTeXAtLeast{<要求値>}`  
    `\upTeXguessedversion` の値が要求値より小さい場合はエラーを出す。
  * `\RequireNativeupTeXAtLeast{<要求値>}`  
    `\upTeXguessedversion` の値が要求値より小さいまたは `\ifnativeupTeX`
    が不成立の場合はエラーを出す。


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

  * Version 2.2  〈2022/04/03〉 
      - `\upTeXguessedversion` を正式にサポート。
      - `\Require(Native)upTeXAtLeast` を追加。
  * Version 2.1  〈2021/07/01〉 
      - 将来の版の pTeX に対応させる。
      - とある非公開機能を削除。
  * Version 2.0  〈2019/11/01〉
      - LaTeX チームによる新しい iftex パッケージと動作を整合させる。
          - 特に、iftex を中で読み込むようにする。
          - `\if...tex` について常に小文字のみの名前を用意する。
      - INI モードでの読込に対応。
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
