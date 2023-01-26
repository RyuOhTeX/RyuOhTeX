# RyuOhTeX LaTeX package
## Quick Start
Please download `RyuOhTeX Template.zip` to your computer and open LaTeX compiler to compile, or browse to [Overleaf website](https://overleaf.com) and import `RyuOhTeX Template.zip` to the project, and you're good to go!
registrations may be required if you do not have an Overleaf account.
## Include

```tex
\usepackage{RyuOhTeX}
```

## Usage

### Placing a Shogi Piece

```tex
\koma<column><row><piece command>
```

### Taken Pieces (Mochigoma)

```tex
\mochigoma[<number of this piece>]<piece>
```

Please be noted that:

* different pieces should be declared separately.
* An upright piece command represents that this piece is captured by sente (black side).

### Shogi Piece Commands

All Shogi Piece commands are named after a "CSA" way, which is a notation method proposed by [Computer Shogi Association](http://www2.computer-shogi.org/).

The general idea for naming piece is listed below:

* All pieces is named in CSA notation method.
* For ally (upright, black side) pieces, enter the command ALL CAPITALIZED. (e.g. `\FU, \OU ` )
* For opponent (reverted, white side) pieces, only the second character of the command is in lowercase. (e.g. `\Ka, \Ry ` )

For more details for piece command, please refer to the PDF file.

### Full Board

```tex
\shogiban{<shogi position>}
```

### Section of a Board

```tex
\tsumeshogi{begin column}{end column}{begin row}{end row}{<shogi position>}
```

### Displaying Kifus (Game Records)

For a single kifu with including rows and columns: (e.g.  ☗７六步)

```tex
\siro<column><row><pieces><move suffixes(optional)>
```

For a kifu only contains kanjis: (e.g. ☖同銀)

```tex
\Siro<pieces><suffixes>
```

For black pieces, change the `\siro` and `\Siro` to `\Kuro `and `\Kuro`.

### Graphicalize Pieces

```tex
\shogiban{\gazouka<shogi pieces>}
```

### Reverted Game Boards

```tex
\gyakuban{<shogi pieces>}
```

Please be noted that the coordinate system has been reverted in this environment.

