[![](../../Banner.jpg)](http://uwm.edu/hpc/support)

## <a name="filesfolders1"></a><a href="#contents" style="text-decoration:none; color:black;">Files and Directories</a>

In the last section we answered the questions `who`, what (`$SHELL`), and when (`date`), so now it's time to discuss the question _where_? When moving around a Linux system you will be encountered by files and directories. The Linux system considers everything to be a file with directories being files that contain files. The following section will discuss how to file system is set up and how to navigate the file system.

The first thing we probably want to know is where are we within the file system. The command `pwd` will **p**rint the **w**orking **d**irectory. For example:

	$ pwd
	/home/<LoginID>

It is important to note that the directory that is printed to the terminal starts with `/`. This refers to the root directory, or the outermost directory while everything after a `/` is a subdirectory. In this case the `LoginID` is a subdirectory of `home` and so on.

When referring to the location of a file or directory there are two ways in which you can reference the path to the file. The *absolute* path refers to a file or directory from the root directory. The *relative* path refers to a file or directory from the current directory.

### Unix File System

![](./img/file-system-01.png)

* All of the directories are descended from the master **root** directory `/`.
* Each of the top-level directories descend directly from the **root** `/`. There are many other standard directories on Unix-derived systems: `/usr`, `/bin`, `/opt`, *etc.*)

<br>

---

<br>

#### Within any one of these folders we can identify a subsidiary structure:

![](./img/file-system-02.png)

<br>


---

<br>

And then we can drill down all the way to something that perhaps looks more familiar to you, a home directory populated with files just like you may treat the **My Documents** folder on Windows.

![](./img/file-system-03.png)

To navigate this system on the command line (as opposed to in a file browser), you only need a few basic commands: `pwd` ,`ls` ,`cd`.

You already learned that `pwd` prints the working directory. To list the contents within a directory use the `ls` command. For example, typing `ls` in the "root" directory:

	$ ls
	bin	data	home	usr

Often a command will take options or flags which begin with `-`. Type `ls -l` to print a long list of the contents within a directory.

	$ ls -l
	total 2
	drwxrwxr-x  2 peetz  wheel  2 Apr  6 09:56 bin
	drwxrwxr-x  2 peetz  wheel  2 Apr  6 09:56 data
	drwxrwxr-x  5 peetz  wheel  5 Apr  6 09:57 home
	drwxrwxr-x  2 peetz  wheel  2 Apr  6 09:56 usr


Other flags such as `-a`,`-t`, or `-r	` display the same contents with some modifications (Refer to the `man` pages for a full list of all the flags). The `-a` flag will display all files including the hidden files.

	$ ls -a
	.	..	bin	data	home	usr

To physically move from one directory to another you can use the `cd` command, as in **c**hange **d**irectory. This can be used in the following way:

	$ cd home/sonic

Notice that the current directory has changed. We can direct `cd` to a directory through an absolute path. For example:

	$ cd /home/$USER/sonic/music

A few handy shortcuts when moving around the file system:

`.` refers to the current directory

`..` refers to the directory above the current directory

`~` refers to the home directory

*Tab completion* will become your best friend when using a linux system. When typing a path becomes tedious you can use tab completion to auto-complete the directory or file. This becomes especially useful for long paths and filenames.

### Do [Exercise #1](./ex1)

<br>
<table style="width:100%; border-collapse: collapse; border:0px solid black;" >
<tr style="border:0px solid black; border-top:1px solid #CCC; line-height:300%;">
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./bash_multi.html">Contents</a></td>
<td style=" border:0px solid black;"></td>
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./bash_multi_1.html">⬅ Previous</a></td>
<td style=" border:0px solid black; text-align:center; font-size:20px;"><a style="font-weight:bold;" href="./bash_multi_2.html">Files and Directories</a></td>
<td style="border:0px solid black; text-align:center; font-size:20px;"><a style="text-decoration:none;" href="./bash_multi_3.html">Next ➡</a></td>
