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