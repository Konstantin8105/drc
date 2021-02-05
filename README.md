# drc
document revision control

## User commands

### initialize dvc for document `0051`
```
drc init 0051
```

create folder:
```
-+0051-0
 |-content.txt
```

### initialize next revision of document
```
drc newrevision 0051
```
create folder `0051-1`

### printing

```
drc print -output=0051.rev0.txt -rev=0 0051
```
create text file `0051.rev0.txt`


```
drc print -output=0051.rev0-1.txt -rev=0 -rev=1 0051
```
create text file `0051.rev0-1.txt` with combination revision 0 and 1 with revision indication

## TODO

*   Multilanguages
*   Inject blocks
*   Internal text format. Maybe markdown
*   Add hash function of each print page
*   how to add image to output document

```
|---------------------|-----|
|HEADER               | REV |
|---------------------+-----|
|                     |     |
|                     |     |
|PAGE                 |     |
|                     |     |
|                     |     |
|---------------------+-----|
|FOOTER               |     |
|---------------------+-----|

```
