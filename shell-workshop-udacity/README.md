# Shell Commands

### Basic Shell I/O 
1.  `echo` - Prints input to shell
Example - 
```
echo hello shell!
```

```
hello shell!
```

Note: 

a) '$' symbol in front of a variable implies it is a shell variable. And this gives us the columns x lines (size) of terminal
```
echo $COLUMNS x $LINES
```
```
60 x 24
```

2.  ``ls`` - List items in the current directory (folder)

   ``cd`` - changes current directory to a particular directory

Note: 

a) List items in a particular directory (if it is a sub-directory within your current directory, just the name is enough)
```
ls Downloads
```
b) List items in a particular directory (full path of the required directory)
```
ls Downloads/folder1/folder2
```
c) Go back to your home directory - 
```
cd ~
```
d) Get details (time last modified,size, name, read-write permissions etc.) about all the files 
```
ls -l Documents/
```
```
total 0
-rw-r--r-- 1 root root 0 Jan 16  2019 1911 Webster Dictionary.epub
-rw-r--r-- 1 root root 0 Jan 17  2019 Alice.pdf
-rw-r--r-- 1 root root 0 Jan 17  2019 All About Love.txt
-rw-r--r-- 1 root root 0 Jan 17  2019 Ballons Gone.png
-rw-r--r-- 1 root root 0 Jan 16  2019 emma.pdf
-rw-r--r-- 1 root root 0 Jan 16  2019 example.txt
-rw-r--r-- 1 root root 0 Jan 16  2019 index.html
-rw-r--r-- 1 root root 0 Jan 17  2019 SillyFile.txt
-rw-r--r-- 1 root root 0 Jan 16  2019 test.json
```

e) Get all files with .txt extension in a directory
```
ls -l Documents/*.txt
```
```
-rw-r--r-- 1 root root 0 Jan 17  2019 Documents/All About Love.txt
-rw-r--r-- 1 root root 0 Jan 16  2019 Documents/example.txt
-rw-r--r-- 1 root root 0 Jan 17  2019 Documents/SillyFile.txt
```
f) Get all files starting with 'Alice' in a directory
```
ls -l Documents/Alice*
```
```
-rw-r--r-- 1 root root 0 Jan 17  2019 Documents/Alice.pdf
```

f) Change directory and then list current directory. Using `;` run two commands in a single line
```
cd /Downloads ; ls
```
```
file1.txt file2.txt
```
g) We could also go back one directory directly using `cd ..`


3.  ``pwd`` - Prints the current working directory


4.  ``mkdir`` - Makes a directory on the given path
```
mkdir Documents/Books
```

5.  ``mv`` - Moves files from one directory to another
``` 
mv Document/*pdf Documents/Books/
```
Now, the directory looks like this -
```
ls Documents/Books/
```
```
Alice.pdf  emma.pdf
```

### Getting data & working with it

1.  ``curl`` - Used to transfer data
```
curl -o google.html -L 'https://www.google.com/'
```
Saves the data to google.html. Without 'o' it returns an output similar to View Source option (in a browser) and prints it **on the terminal**. 
We ususally put website address in single quotes because they have special characters in them which might confuse the shell.

2. `cat` - View file contents

   `less` - View file content section by section (from the start) 
Views a fixed portion of a file. Offers navigation through arrow keys and `/` command for search. Press `q` to quit. 
  
3. `rm` - remove file
  
  `rm -i` - remove file (with safety prompt before deleting)
  
  `rmdir` - remove directory

**NOTE** - Files/directories are never sent to any 'recycle bin' only directly deleted.

4. `grep` - 'global regular expression print' processes text iteratively by lines and prints lines matching an i/p pattern.
  
   `wc` - 'word count', reads standard input or a list of files and generates one or more of the following statistics: newline count, word count, and byte count
  
   `|` - 'pipe command', used for o/p of one command to other

**Usage**: 

Search for 'apple' in dictionary.txt and view the o/p contents
```
grep apple dictionary.txt | less
```

Pull text from a url, search for a keyword and print number of lines
```
curl -L https://tinyurl.com/zeyq9vc | grep fish | wc -l
```
(More on this here - https://man7.org/linux/man-pages/man1/grep.1.html)


5. Shell & Environment variables

Shell variables are internal to the shell. Example- `$LINES` and `$COLUMNS`. Environment variables are shared with program run from within the shell. Example - `$PATH` 

Usage:

Define a shell variable
```
new_variable='test string @!#$@' 
```

NOTE: No spaces between the equal to and variable value 

print command for shell variable
```
echo $new_variable
```

which outputs
```
test string @!#$@
```

Environment variable `$PATH` can be listed as follows-
`echo $PATH`


Add a path varibale to the existing path/directory (works only for single shell session; restart not possible)
```
PATH=$PATH:new/dir/here
```

### Customizing the shell


## Further references
1. https://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html
2. https://www.youtube.com/c/MissingSemester/playlists
