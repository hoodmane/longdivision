longdivision v1.2.0
========================
Author: Hood Chatham
Email: hood@mit.edu
Date: 2020-05-09
Description: 
License: All files have the Latex Project Public License.
Files:
    longdivision.sty
    longdivision_manual.tex
    longdivision_manual.pdf
    README.md


Does the long division algorithm and typesets the results. The dividend must 
be a positive decimal number and the divisor must be a positive integer. 
Correctly handles repeating decimals, putting a bar over the repeated part of 
the decimal. Handles dividends up to 20 digits long gracefully (though the 
typeset result will take up about a page) and dividends between 20 and 60 
digits long slightly less gracefully. 

Defines macros \longdivision and \intlongdivision. Each takes two arguments, 
a dividend and divisor. \longdivision keeps dividing until the remainder is 
zero, or it encounters a repeated remainder. \longdivision stops when the 
dividend stops (though the dividend doesn't have to be an integer). 

\intlongdivision behaves similarly to the \longdiv command defined in 
longdiv.tex, though I think \intlongdivision looks better, and it can handle 
much larger dividends and divisors (the dividend is only constrained by the 
size of the page, and the divisor can be up to 8 digits long). 

See the package manual for more information. To compile the manual, you need 
the file pgfmanual-en-macros.tex from the tikz manual. I am not allowed to
include this file on the CTAN repositiory due to rules against file duplication,
but you can find it on github: 
https://github.com/hoodmane/longdivision/blob/master/pgfmanual-en-macros.tex

Email me at hood@mit.edu to submit bug reports, request new features, etc. 
The current development copy is hosted at https://github.com/hoodmane/longdivision. 


Changelog:
==========

## [1.2.0] (2020-05-09)
### Added:
- An option to control the decimal separator
- Options to specify "digit separator" and "digit group length"
- A "separators in work" option to put spaces rather than punctuation in the work
- Change the division sign in "german style" long division

### Fixed:
- Math mode usage used to be inconsistent. Now if not used in math mode, 
  typesetting is consistently not in math mode, if used in math mode it is 
  consistently in math mode.
- Major improvements to typesetting engine should allow changes in the future to be less painful.
- A few deprecated expl3 commands have been replaced (thanks to a pull request from Phelype Oleinik).


## [1.1.0] (2018-10-08)
### Added:
- Multiple typesetting styles
- Multiple styles for indicating a repeating decimal
- Typesetting partial long division (as suggested by Cameron McLeman).

### Fixed:
- If the "\longdivision" command is in math mode, the numbers are typeset in math mode too (reported by Yu-Tsiang Tai).
- The "\longdivision" command now can handle macros as arguments (as suggested by Mike Jenck).


## [1.0.0] (2017-02-05)

