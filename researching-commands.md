# Researching Commands
## Interesting Uses of the `grep` Command ##
`grep` is a command-line tool that lets you find a pattern or expression in a given file, the output returns lines with matches to your string.<br> 

Just as a point of comparison, here is a standard use of grep: <br>
`grep "zebra" zooPamphlet.txt` <br>
_find string "zebra" in a file called "zooPamphlet.txt"_ <br>


We will use the following-line tools for files and directories from `./technical`. <br>
### `grep -e`
Sometimes you want to find a match for more than one expression, in this case you will need to add `-e` before every expression. The command-line input: 

        $ grep -e "bomb" -e "flight" chapter-2.txt
    
Generates the output:
        
        Islam, and celebrated recent suicide bombings of 
        
Similarly, the command-line input:

        $ grep -e "killed" -e "flight" chapter-2.txt
        
Generates the output:

        [Copy here]
        
### `grep -o`
Maybe you want to only output the matched expression without the rest of the line. In this case, you will need to add `-o` after `grep` before expression arguments. The command-line input:

        $ grep -o "killed" chapter-1.txt
        
Generates the output:

        killed
        killed
        killed
        killed
        killed
        killed
        killed
        killed

Similarly, the command-line input:

        $grep -o -e "killed" -e "bomb" chapter-2.txt

Generates the output:



### `grep -n`
Or, perhaps, you want to not only find matches but line numbers for those matches as well. In this case, you will need to add `-n` after `grep` but before expression arguments. The command-line input: 

        $ grep -n "killed" chapter-1.txt

Generates the output:



Similarly, the command-line input: 

        $grep -n -e "killed" -e "bomb" chapter-1.txt

Generates the output:
### `grep -m`
Another interesting take would be to only generate the first _n_ (where _n_ is a number) matches of the expression. The command-line output:

        $grep -m 5 "bomb" chapter-2.txt

Generates the output: 



Similarly, the command-line input:



Generates the output:
#### Sources that Helped Inform this Blog:

[Code Snippets for grep Commands](https://www.makeuseof.com/grep-command-practical-examples/) <br>

[grep manual](https://ss64.com/bash/grep.html)

