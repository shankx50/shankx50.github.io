---
layout: page
title: Unix
date:   2015-09-14
permalink: /unix/
---
<p>Last update: {{ page.date | date: "%b %-d, %Y" }}</p>
There's no serious web development without using UNIX commands and the command line. Daunting at the beginning, the command line quickly becomes every programmer's best friend.

---
<br/>

### Navigation

-  <q>cd -</q> gets you back to the previous directory.

### File creation

- touch

### File editing

- nano

### File reading

- cat (concatenation of more small files)
- less (larger files)
- head (displays beginning of file)
- tail -f (displays the end of a file) -f: follows the file for updates

### Create directory

- mkdir, use option -p if parent directory already exists

### Move and renaming files/directories

- mv filename/directory relative or absolute path
- also use mv for renaming files since rename command is unreliable
- -n no overwriting
- -f force overwriting (attention default mode)
- -i interactive mode (gives you options)
- -v verbose

### Copying files

- cp source destination_path (same options as mv)
- cp -R for whole directories (recursive copy)

### Delete files/directories

- rm file; -R (recursive option)
- rmdir directory (only for empty directories)

### Hard links

Makes a reference to a file in the file system (just like any listed file name if you think about it)

- ln filetolink hardlink
- Do not break if file is deleted/moved

### Symbolic links

- ln -s filetolink symlinkname
- symbolic links reference the path, not the file itself (like the hard link)

### Searching

- find path expression ex. find ~/Documents -name "something.jpg"
- can use wildcard characters (\*,?,[])
- check out man find since this is a very powerful command
