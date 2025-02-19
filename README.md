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
7. rmdir: Remove an emptyfolder

# specific things for 1-2
1.Pipes|: Pipes allow you to send the output of one command as the input to another command so that we can chain multiple commands together.
          eg: If you want to find out all the occurances of the word "error" in a file and count how many times it appears:
          cat file.txt | grep "error" | wc-l
