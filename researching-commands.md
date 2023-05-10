# Researching Commands
## Interesting Uses of the `grep` Command ##
`grep` is a command-line tool that lets you find a pattern or expression in a given file, the output returns lines with matches to your string.<br> 

Standard use of grep: <br>
`grep "zebra" zooPamphlet.txt` <br>
_Here we want to find the word "zebra" in a file called "zooPamphlet.txt"_ <br>

### `grep -e`
Sometimes you want to find a match for more than one expression, in this case you will need to add `-e` before every expression. 

        $ grep -e "bomb" -e "flight" chapter-2.txt
        Islam, and celebrated recent suicide `red` bomb
    
    
### `grep -o`
### `grep -n`
### `grep -m`
#### Sources that Helped Inform this Blog:

[Code Snippets for grep Commands](https://www.makeuseof.com/grep-command-practical-examples/) <br>

[grep manual](https://ss64.com/bash/grep.html)

