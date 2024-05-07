1. whoami
- USERNAME


2. text editor in terminal
- nano draft.txt


3. accept the name 
- ctrl + O


4. exit the editor
- ctrl + X


5. wc "" is word count


6. wc *.pdb
- will check everything within the directory's wordcount


7. wc -l *.pdb
- will only show number of lines per file in the directory
- l is lines

8. -m is for characters and -w is for words
- m is character and w id word
- can replace the -l


9. wc -l *.pdb > lengths.txt
- will create a file (or silently overwrite if one exisits) which is greater than


10. cat lengths.txt 
- cat is concatenate, join together, and prints the contents of the files one after another


11. sort "" or sort -n ""


12. using -n 1 "" will provide the first line of the file


13. echo hello > testfile01.txt ~ type twice ~ notice the output 
14. echo hello >> testfile02.txt ~ type twice ~ notice the output 


15. sort -n lengths.txt | head -n 1
- | is a pipe. tells the shell that we want to use the output of the comand on the left as the input to the command on the right


---------------------------

# Shell Scrips

1. create a file by doing nano middle.sh
2. in the file, put in it, head -n 15 octane.pdb | tail -n 5
3. exit the file
4. execute the script ~ bash middle.sh
5. edit middle.sh with head -n 15 "$1" | tail -n 3
6. $1 means the first filename or other argument, on the cli
7. exit and run bash middle.sh octane.pdb
8. Edit middle.sh to include comments for the next person # select lines from middle of file # usage: bash middle.sh filename end_line num_lines
- $@ means 'all of the command-line arguments to the shell script'
9. nano sorted.sh
10. wc - l "$@" | sort -n
11. bash sorted.sh *.pdb ../creates/*.dat