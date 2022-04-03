ifptex Package Bundle
=====================

TeX: To check the engine is pTeX (or its derivatives)

The ifptex package is a counterpart of ifxetex, ifluatex, etc. for
the pTeX engine. The ifuptex package is an alises to ifptex provided
for backward compatibility.

### System Requirements

  * TeX format: plain TeX, LaTeX, and INI mode.
  * TeX engine: Anything.
  * DVI driver (in DVI mode): Anything.
  * Dependent packages:
      - iftex

### Installation

In a system compliant to TDS 1.1, move the files as follows:

  - `*.sty` → $TEXMF/tex/generic/ifptex

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

  * `\ifptex` (or `\ifpTeX`)  [if-token]  
    Whether the engine is pTeX (including upTeX or pTeX-ng).
  * `\ifstrictptex` (or `\ifstrictpTeX`) [if-token]  
    Whether the engine is pTeX but *not* upTeX or pTeX-ng.
  * `\ifuptex` (or `\ifupTeX`) [if-token]  
    Whether the engine is upTeX (including pTeX-ng).
  * `\ifstrictuptex` (or `\ifstrictupTeX`) [if-token]  
    Whether the engine is upTeX but *not* pTeX-ng.
  * `\ifnativeuptex` (or `\ifnativeupTeX`) [if-token]  
    Whether the engine is upTeX and its internal encoding is Unicode.
  * `\ifptexng` (or `\ifpTeXng`) [if-token]  
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
  * `\upTeXguessedversion` [mathchardef-token]  
    The guessed value of upTeX version; given as a 100-folded integer.  
    NB. On version 1.23 or later, the value is correct.  
    NB. On a non-upTeX engine, the value is zero.
  * `\RequireupTeXAtLeast{<required>}`  
    Issues an error if `\upTeXguessedversion` is smaller than the given
    required value.
  * `\RequireNativeupTeXAtLeast{<required>}`  
    Issues an error either if `\upTeXguessedversion` is smaller than
    the given required value or if `\ifnativeupTeX` fails.


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

  * Version 2.2  〈2022/04/03〉 
      - Officialy support `\upTeXguessedversion`.
      - Add `\Require(Native)upTeXAtLeast`.
  * Version 2.1  〈2021/07/01〉 
      - Adjust for the future version of pTeX.
      - Drop an undocumented feature.
  * Version 2.0  〈2019/11/01〉
      - Adjust to work better with the new iftex package maintanined
        by the LaTeX3 Project.
          - Now iftex is loaded inside ifptex.
          - Provide always all-lowercase `\if...tex` commands.
      - Support for loading in INI mode.
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
