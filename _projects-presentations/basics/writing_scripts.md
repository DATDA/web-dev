---
title: "Writing Scripts"
layout: single
author_profile: true
read_time: true
comments: true
share: true
related: true
toc: false
toc_label: "TOC LABEL"
toc_icon: file-alt
toc_sticky: false
last_modified_at: 2017-10-15
tags: [Bash, Perl, Python, Scripts]
categories: []
---

by scrypy

Scripts are great for automating, controlling, and otherwise simplifying your workflows on a computer. But they can be confusing when first starting out and trying to figure out exactly how to make them work.

## Bash

Consider the command `echo "hello world"`. This should print out the words 'hello world' right? Now, what if you want to echo the most memory intensive process on your system every 30 seconds? You could sit at the terminal and use your bash history to re-submit this command according to the stopwatch on your phone. Or you can write a script that does it for you!

The beginning of every bash script should begin with `#!/bin/bash`. The `#!` is called a [shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)) and lets your computer know that this file should be treated as a script, and then whatever comes after it is going to be the interpreter that you want the computer to use when running this script. After changing the file to be executable by using `chmod u+x <filename>` then when you run the file by typing `./<filename>` into the terminal it will use the interpreter on the shebang line to execute the commands within.

##### Basic Script

Now back to the scripting. Create a new file and enter the below text into it, make it executable, and run it.
```bash
#!/bin/bash
echo 'hello this is my first script!'
#this line is a comment
```

Congrats! You just made and ran a bash script. Granted it's really basic and doesn't do a lot so lets remedy that. Go to your terminal and enter the following command([explanation here](https://explainshell.com/explain?cmd=ps+-aux)): `ps -aux`. This should print out a list of almost all the processes running on your linux machine, along with the amount of CPU and memory that it is using(amongst other things). Now enter this command courtesy of [Guillermo Garron](https://www.garron.me/en/go2linux/how-find-which-process-eating-ram-memory-linux.html): `ps aux | awk '{print $2, $4, $11}' | sort -k2rn | head -n 20`. This nice series of [piped](https://www.geeksforgeeks.org/piping-in-unix-or-linux/) commands will print the top 20 most RAM intensive processes into your terminal.

##### Capturing Command Output

But suppose we want to take those 20 processes and do some further investigating into them. This is where some of the power of scripting comes into play. We will take the output from that command and then store the output into an array, where each line is an element of the array. The process of capturing the output from a command for further use is something known as [command substitution](http://www.gnu.org/software/bash/manual/bashref.html#Command-Substitution)[[2]](https://www.cyberciti.biz/faq/unix-linux-bsd-appleosx-bash-assign-variable-command-output/)[[3]](https://www.oreilly.com/library/view/bash-cookbook/0596526784/ch13s04.html). Copy/pasta the below script to see it in action:

```bash
#!/bin/bash
example1=`echo hello`
example2=$(echo world)
echo $example1 $example2
```

This will perform 3 different echo calls, where the first is captured into the variable example1, the second is captured in variable example2, and the third prints out the contents of each variable. This is the basic example of how to store the output of a command into a single variable, and we can treat this variable as an array of sorts. Since our output contained in the array contains newline characters, we are able to iterate through the variable like it is an array and we can extract each whitespaced element from the variable.

```bash
#!/bin/bash
memory_hogs=$(ps aux | awk '{print $2, $4, $11}' | sort -k2rn | head -n 20)
for i in $memory_hogs; do echo "array output=>$i"; done
```

<hr>

## Python

Python is a great scripting utility that combines your abilities to write programs with the power of system administration utilities. Python scripts, similar to the bash scripts above, should begin with a shebang and your choice of python interpreter(i.e. `#!/usr/bin/python3.5`).

The most common libraries when writing a script to perform system administration functions are the [os](https://docs.python.org/3/library/os.html),[sys](https://docs.python.org/3/library/sys.html), [re](https://docs.python.org/3/library/re.html), and [subprocess](https://docs.python.org/3/library/subprocess.html) libraries which give you access to operating system, system-specific parameters, regular expression capabilities, and subprocess management(respectively) which can be imported using: `import os,sys,re,subprocess`.

##### Basic Script

Here is an example of a basic script that will take two input parameters and print them both out, then print out the amount of memory being used by our script(using the `psutil` library, which can be installed by typing `pip3 install --user psutil` in your terminal):
```python
#!/usr/bin/python3.5
import sys, psutil, os

#this is a comment

if(len(sys.argv)<3):#make sure we have the right number of inputs
  print('you need more arguments')
  sys.exit()

print('{} {}'.format(sys.argv[1],sys.argv[2]))
process = psutil.Process(os.getpid())
print('This script is called {} and is using {} bytes'.format(sys.argv[0],process.memory_info().rss))  # in bytes
```
[snippet cred](https://stackoverflow.com/questions/938733/total-memory-used-by-python-process)

##### Capturing Command Output

Now, using our `ps aux` command from above, we write the following script to capture the output of that from the python side of things, and then print out the first 4 lines of the output:
```python
#!/usr/bin/python3.5
import subprocess

my_output = subprocess.run(["ps", "aux"], stdout=subprocess.PIPE)
for line in str(my_output).split('\\n')[:4]:
    print('my split line=>{}'.format(line))
    print('*********')
```

<hr>
## Perl
Perl is a beautifully ugly scripting language that is very flexible and allows you to get away with really nasty syntax and is extremely fun to write with. As with the previous languages, start these scripts with the following shebang: `#!/usr/bin/perl`.

##### Basic Script

```perl
#!/usr/bin/perl
print "hello world fro the script\n";
print "input values from the user are @ARGV\n";
print "first user provided input value is: $ARGV[0]\n";
print "second user input is: $ARGV[1]\n";
```

##### Capturing Command Output

Perl captures the output of commands in a similar way to bash:

```perl
#!/usr/bin/perl
@output = `ps aux | awk '{print $2, $4, $11}' | sort -k2rn | head -n 20`;
chomp @output;#get rid of newline characters in the strings
foreach $line (@output){
  print "output line=> $line\n***********************\n";
}
```

*NOTE:* Guillermo's one-liner would not work on my Mac due to the formatting differences of the output from `ps aux` so be aware of that.

<br/><br/><br/><br/>
fin
