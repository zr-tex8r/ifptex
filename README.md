ifptex Package Bundle
=====================

TeX: To check the engine is pTeX (or its derivatives)

The ifptex package is a counterpart of ifxetex, ifluatex, etc. for
the pTeX engine. The ifuptex package is an alises to ifptex provided
for backward compatibility.

### System Requirements

  - TeX format: plain TeX, LaTeX (and any plain-compatible ones)
  - TeX engine: any engine

### Installation

In a system compliant to TDS 1.1, move the files as follows:

  - `*.sty` → $TEXMF/tex/latex/ifptex

And rehash your TEXMF trees if necessary.

ifptex Package ― Test for pTeX engine
--------------------------------------

### Package Loading

In plain TeX:

    \input ifptex.sty

In LaTeX:

    \usepackage{ifptex}

### Usage

  * `\ifpTeX`  [if-token]  
    Whether the engine is pTeX (or its derivative, including upTeX).
  * `\ifupTeX` [if-token]  
    Whether the engine is upTeX (or its derivative).
  * `\ifNativeupTeX` [if-token]  
    Whether the engine is upTeX and its internal encoding is Unicode.
  * `\ifNewupTeX` [if-token]  
    Whether the engine is a new upTeX supporting `\disablecjktoken`.
  * `\RequirepTeX`  
    Issues an error if `\ifpTeX` fails.
  * `\RequireupTeX`  
    Issues an error if `\ifupTeX` fails.
  * `\RequireNativeupTeX`  
    Issues an error if `\ifNativeupTeX` fails.
  * `\RequireNewupTeX`  
    Issues an error if `\ifNewupTeX` fails.

Revision History
----------------

  * version 1.0  [2013/04/29]
      - Moved to a separate bundle.
      - Changede the package name to ifptex, and added the test
        for pTeX (besides upTeX).
  * version 0.2  [2008/03/14]
      - First public version.

----------------------------------------

ifptex パッケージバンドル
=========================

TeX: エンジンが pTeX（かその派生）であるかを判定する

ifptex パッケージは ifxetex や ifluatex 等のパッケージの pTeX 版に
相当する。ifuptex パッケージは ifptex の別名で、後方互換性のために
用意されている。

### システム要件

  - TeX フォーマット： plain TeX、LaTeX （や他の plain 互換なもの）
  - TeX エンジン： 不問

### インストール

TDS 1.1 に準拠するシステムの場合、以下のようにファイルを移動する：

  - `*.sty` → $TEXMF/tex/latex/ifptex

この後必要に応じて mktexlsr を実行する。

ifptex パッケージ ― pTeX エンジンの判定
----------------------------------------

### パッケージ読込

plain TeX の場合：

    \input ifptex.sty

LaTeX の場合：

    \usepackage{ifptex}

### 機能

  * `\ifpTeX`  [if-トークン]  
    pTeX (upTeXを含む)を使っているか。
  * `\ifupTeX` [if-トークン]  
    upTeX を使っているか。
  * `\ifNativeupTeX` [if-トークン]  
    upTeX を内部文字コードが Unicode の状態で使っているか。  
    [旧名称: `\ifnativeupTeX`]
  * `\ifNewupTeX` [if-トークン]  
    `\disablecjktoken` をサポートした upTeX を使っているか。
  * `\RequirepTeX`  
    `\ifpTeX` 不成立の場合はエラーを出す。
  * `\RequireupTeX`  
    `\ifupTeX` 不成立の場合はエラーを出す。
  * `\RequireNativeupTeX`  
    `\ifNativeupTeX` 不成立の場合はエラーを出す。
  * `\RequireNewupTeX`  
    `\ifNewupTeX` 不成立の場合はエラーを出す。

更新履歴
--------

  * version 1.0  [2013/04/29]
      - 独立のバンドルに移動。
      - パッケージ名を ifptex に変更して、pTeX 判定機能を付加。
      - (試験的) upTeX の版判定機能を追加。
  * version 0.2  [2008/03/14]
      - 最初の公開版。

----------------------------------------
Takayuki YATO (aka. "ZR")  
http://zrbabbler.sp.land.to/
