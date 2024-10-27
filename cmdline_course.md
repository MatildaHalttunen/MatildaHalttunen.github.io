---
layout: default
---

## Command Line Tools for Linguists

<img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEikGeMQVbPLFoYNr8brw5JZSLmlQgYRHmm-Tr89x4pgVeMMFpx-5hqUDQPxldmlk72AZCfT49smhq5cZDZNUn-jK1CJTzISMoxby2USLD2Z_6WoaYcuofe-EZDUqql9bG9d3RGqTjVjzIg/s1600/download.jpg" alt="Photo" hspace="20" width="30%" align="right"/> 
This was an online course to introduce the students to command line and its different uses, and how to benefit from it in their work. The course was specifically aimed towards linguistics students. 


### Week 1: Intoruduction to Command Line Environments

During this first week we learned to open and use the command line environment on our chosen operating system, as well as some basic commands.

Commands learned during the first week included the following:
 * whoami
 * pwd
 * ls
 * cd
 * mkdir
 * cp
 * mv
 * cat
 * less
 * man

##### Example command

 ```
whoami
gustaf
```

This command is to determine who is the current logged in user.


### Week 2: Navigating a UNIX System

During the second week we were introduced to UNIX systems as well as remote servers and safely conecting to them using ssh. We were also introdduced to process management and controling the processes from the command line, as well as using the chmod-command to manage the read, write and execute permissions of files.

##### Example command

```
chmod 654 example.txt
```

This command would adjust the read, write and execute permissions of the example file in such a way that the owner of the file would have read and write permissions, the group would have read and execute permissions, and others would have read permission.


### Week 3: Basic Corpus Processing

This week we were introduced to basic text processing tools, and learned about different character encodings. We also learned how to manage formatted text files in the command line environment.

##### Example command

```
dos2unix example.txt
```

Windows and Unix files have different line-end encodings. This command takes a Windows-encoded file and translates it to Unix encoding.


### Week 4: Advanced Corpus Processing

During the fourth week we learned to use piping to create more complex text processing commands without creating a surplus of files. We also learned about sed and some basics on how to use it when editing large text files.

##### Example command

```
sed '/^$/d' example.txt
```

The above sed command deletes all empty lines from the example.txt file.


### Week 5: Scripting and Configuration Files

This week we learned to understand and construct scripts to help us run more complex text editing. We were also introduced to configuring files and how to use them to alter system behaviour through environmental variables.

##### Example script

```python
#! /bin/bash

# if an adjective ends with a consonant, print a comparative form.

if [[ "$1" =~ [aeioyu]$ ]];
then
   echo "$1"
else
   echo "$1""er"
fi
```

This script takes one argument, in this case an English adjective ending with a consonant, and creates a comparative form for it.


### Week 6: Installing and Running Programs

Week six saw us learning how to install and update programs using package managers such as brew. We were also introduced to make and how to create and use makefiles.

##### Example make rule

```python
%.no_md.txt: %.txt
	python3 src/remove_gutenberg_metadata.py $< $@

results/%.freq.txt: data/%.no_md.txt 
	src/freqlist.sh $< $@
```

The first example make rule has target %.no_md.txt and dependency %.txt. It uses python code to remove the metadata from the dependency files.  
The second example make rule has target %.freq.txt and dependency %.no:md.txt. It uses the freqlist.sh script to create word frequency lists from the dependency files. 

##### Example results of running the make rules

A Christmas Carol | Dracula | Life of Bee
--- | --- | ---
the | the | the
and | and | of
a | I | and
of | to | to


### Week 7: Version Control

During week seven we were introduced to the importance of version control, and were shown how to use git. We also created our own GitHub accounts to keep track of our projects.

##### Example command

```
git commit -m "This is an example commitment"
```

The above git command commits the changes made in the local repository to the remote repository with an added comment, which helps track the changes committed.


### Final Assignment

We wrapped up the course by using GitHub and Jekyll to build our own websites. We were introduced to markdown and its different uses.

##### Example from a markdown file

```
## Find me on

[GitHub](https://github.com/MatildaHalttunen)
```

This markdown text will create a header size 2 and a link to my Git Hub page with the link text "GitHub".