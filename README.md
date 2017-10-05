ifptex Package Bundle
=====================

TeX: To check the engine is pTeX (or its derivatives)

The ifptex package is a counterpart of ifxetex, ifluatex, etc. for
the pTeX engine. The ifuptex package is an alises to ifptex provided
for backward compatibility.

### System Requirements

  - TeX format: plain TeX, LaTeX (and any plain-compatible ones).
  - TeX engine: Anything.
  - DVI driver (in DVI mode): Anything.

### Installation

In a system compliant to TDS 1.1, move the files as follows:

  - `*.sty` → $TEXMF/tex/latex/ifptex

And rehash your TEXMF trees if necessary.

### License

This package is distributed under the MIT License.

ifptex Package ― Test for pTeX engine
--------------------------------------

### Package Loading

In plain TeX:

    \input ifptex.sty

In LaTeX:

    \usepackage{ifptex}

### Usage

NB: Here “e-TeX-ness” is not considered.

  * `\ifpTeX` (or `\ifptex`)  [if-token]  
    Whether the engine is pTeX (including upTeX or pTeX-ng).
  * `\ifstrictpTeX` (or `\ifstrictptex`) [if-token]  
    Whether the engine is pTeX but *not* upTeX or pTeX-ng.
  * `\ifupTeX` (or `\ifuptex`) [if-token]  
    Whether the engine is upTeX (including pTeX-ng).
  * `\ifstrictupTeX` (or `\ifstrictuptex`) [if-token]  
    Whether the engine is upTeX but *not* pTeX-ng.
  * `\ifnativeupTeX` [if-token]  
    Whether the engine is upTeX and its internal encoding is Unicode.
  * `\ifpTeXng` (or `\ifptexng`) [if-token]  
    Whether the engine is pTeX-ng.
  * `\RequirepTeX`  
    Issues an error if `\ifpTeX` fails.
  * `\RequireStrictpTeX`  
    Issues an error if `\ifstrictpTeX` fails.
  * `\RequireupTeX`  
    Issues an error if `\ifupTeX` fails.
  * `\RequireStrictupTeX`  
    Issues an error if `\ifstrictupTeX` fails.
  * `\RequireNativeupTeX`  
    Issues an error if `\ifnativeupTeX` fails.
  * `\RequirepTeXng`  
    Issues an error if `\ifpTeXng` fails.


ifuptex Package ― Alias of ifptex
----------------------------------

The ifuptex package does nothing but loading ifptex internally. It is
provided for backward compatibility.

### Package Loading

In plain TeX:

    \input ifuptex.sty

In LaTeX:

    \usepackage{ifuptex}

### Usage

Just the same as the ifptex package.


Revision History
----------------

  * Version 1.2c 〈2017/10/04〉
  * Version 1.2b 〈2017/09/20〉
  * Version 1.2a 〈2017/09/15〉
  * Version 1.2  〈2017/09/09〉
      - Add `\ifstrictupTeX` and `RequireStrictupTeX`.
  * Version 1.1  〈2017/05/04〉
      - Minor fix.
  * Version 1.0  〈2013/04/29〉
      - Move to a separate bundle.
      - Change the package name to ifptex, and added the test
        for pTeX (besides upTeX).
  * Version 0.2  〈2008/03/14〉
      - First public version.

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
