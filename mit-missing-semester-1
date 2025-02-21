# Feb-notes
# key knowledge points about mit-missing semester

# 1.Shell and command line basis
  1-1. Shell basis: ls\cd\mv\cp\rm.etc
  
  1-2. Pipes and direction: |\>\<.etc
  
  1-3. Text processing: grep\awk\sed\sort.etc
  
  1-4. scripting: simple shell scripts to automate tasks
     
# specific things for 1-1
1.pwd: Prints (the current) working directory

2.cd: Change (the current) directory cd/path/to/your/folder
      cd .. # go up one level
      cd ~ # go to your home directory
      
3.ls: List files and directories

      ls -l # detailed listing
      
      ls -a # include hidden files
      
4. touch: Create a new and empty file
   
5. mkdir: Create a new directory
  
6. rm: Remove a file
   
7. rmdir: Remove an empty folder

# specific things for 1-2
1.Pipes|: Pipes allow you to send the output of one command as the input to another command so that we can chain multiple commands together.

1.eg: 
          
          If you want to find out all the occurances of the word "error" in a file and count how many times it appears:
          
          cat file.txt | grep "error" | wc -l
          
          # greb is a tool for searching text. It looks for lines that match a specified pattern in a file or input. wc is a tool used to count the number of lines\words. -l option counts the number of lines. 

          # the -o option in grep outputs only the matching part of the line, with each match on a new line.

          # Remeber greb is a count tool only for xxx.txt, if we need to count something like xxx.docx, we need to change the type of it. 即转化成纯文本 这里用pandoc的例子

          pandoc -s /Users/hehejialei/Desktop/人类研究/我.docx -t plain -o output.txt
          
          grep -o "你" output.txt | wc -l

          # pandoc支持文档转换，-s表示standalone（生成一个完整的文档），-t plain指定输出格式为纯文本， -o output.txt将转换后的内容
          
          输出到output.txt文件中。

2.eg: 
          
          the content of file.txt is:
          
          This is an error sample.
          
          Another error here, and yet another error.

          without -o:
          
          grep "error" file.txt
          
          Output:

          This is an error example.

          Another error here, and yet another error. (the whole sentence)

          with -o:

          grep -o "error" file.txt

          Output:

          error

          error

          error

          combined with wc -l:

          grep -o "error" file.txt | wc -l

          output:

          3

2.Redirection: > >> <

          1. >：Redirects output to a file, overwriting it if it exists.

          $ echo "Hello, World!" > hello.txt  # Writes "Hello, World!" to hello.txt

          2. >>：Appends output to a file without overwriting

          $ echo "Appended text" >> hello.txt  # Appends to hello.txt

          3. <： Takes input from a file.

          $ sort < unsorted_file.txt  # Sorts the contents of unsorted_file.txt

# specific things for 1-3

1. grep (mentioned on the previous lines)

2. awk

          # a important tip: Field（字段）$1\$2...field1\2....;$0 represents the whole sentence

1.eg.

          John Doe 30 Developer
          
          Jane Smith 25 Designer (content of file.txt)

          bash: awk '{ print $1, $4 }' file.txt

          output: John Developer
          
                  Jane Designer

          # 可以指定不同的东西作为字段分隔符，如awk -F','就是将逗号作为字段分隔符。

2.eg. （修改输出字段分隔符）

          John Doe 30 Developer
          
          Jane Smith 25 Designer (content of file.txt)

          bash: awk 'BEGIN { OFS=" - " } { print $1, $4 }' file.txt

          output: John - Developer
          
                  Jane - Designer

          
  
          
          

          
