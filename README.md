# SP19-LING-L245

Francis M. Tyers 

## Commands from 4th February

```
http://cl.indiana.edu/~ftyers/courses/2019/L-245/

sudo apt install git <=-- type this 

"sudo" means do this as 'admin'	
"apt install git" installs the version control system

... password is "apertium" (there will be no output) -- it doesn't tell you what you're typing


git clone https://github.com/REPLACE_WITH_GITHUB_USERNAME/SP19-LING-L245.git

This makes a local copy of your repository.

You need to put your username instead of REPLACE_WITH_GITHUB_USERNAME.

Type 'ls' and press return, you should see a folder called 'SP19-LING-L245'.

Then type: cd SP19-LING-L245

And then 'ls' again.

You should see files like 'wiki.txt' and 'wiki.hist'

wget https://dumps.wikimedia.org/kbdwiki/20190201/kbdwiki-20190201-pages-articles.xml.bz2

python3 WikiExtractor/WikiExtractor.py   --infn   kbdwiki-20190201-pages-articles.xml.bz2

or

python3 ~/WikiExtractor.py --infn kbdwiki-20190201-pages-articles.xml.bz2

wc -l wiki.txt # how many lines are there in the file. line = paragraph.

ls -lh wiki.txt # how big the file is. if it's over 10M we don't want it in github

git status # this checks to see if any local files have been changed (compared to your repository)

git commit -a -m "update wiki.txt" # commit your changes to the wiki.txt / corpus file

git config --global user.email "YOUR EMAIL ADDRESS HERE"

git config --global user.name "YOUR NAME HERE"

git commit -a -m "update wiki.txt" # because the previous one failed

git push
---------------------------------
sed 's/[^a-zA-Z]\+/\n/g' 

sed = command
's/aaa/bbb/g'
   s = substitute
   g = global
   aaa = pattern to search for
   bbb = pattern to replace with

^ = not
a-z = lowercase latin letters
A-Z = uppercase latin letters 

+ = one or more

[^a-zA-Z]\+ = any sequence of symbols/characters that is not in the set of a-zA-Z
---------------------
git status
git add wiki.words ; git commit -a -m "add file" ; git push


```

## Commands from the 6th February

```
Set up VirtualBox again (sorry!) 
--

The disk image is found in:

C:\Program Files\Oracle\VirtualBox

(It's the .vdi file)

Remember: Ubuntu (32bit)

Memory 4Gb minimum (4096Mb)

Name of the machine doesn't matter.

----------
Commands:

ls = list files 

cd = change directory (folder)

    cd SP19-LING-245 (just type SP and press 'TAB')

pwd = present working directory (where are you?)

sed = stream editor

----------

sed 's/[^A-Za-z]\+/\n/g' < wiki.txt > wiki.words
```
