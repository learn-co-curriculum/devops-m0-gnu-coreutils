# GNU Coreutils

## Learning goals

- Learn basics and history of the *GNU Coreutils*
- Gain an understanding of the most frequently used tools in the collection
- Learn what piping is and how to use it

## Introduction

The **GNU Coreutils** are a collection of *CLI (command-line interface) tools* that are very frequently used on *Linux* systems. These tools are part of the **GNU Project**, which is a collaborative effort to create a free and open-source suite of tools based on the *Linux* kernel.

These tools include everything from working with files and directories, to performing system tasks like copying/moving files, changing user permissions, searching, etc.

All the tools in the GNU suite are released under the *GNU General Public License (GPL)*, which allows users to freely use, modify, and distribute the software, as long as their derivations also remain open-source.

## Tools in the collection

Here's a non-exhaustive list of some of the most commonly used commands belonging to the GNU suite, and by extension, *Linux*:

- `ls`: Lists the contents of a directory.

```bash
$ ls
Desktop Documents Downloads Music Pictures Videos
```

- `mkdir`: Creates a new directory.

```bash
$ mkdir new_directory
```

- `mv`: Moves (or renames) files and directories. If you specify the filename in the destination, it will rename the file to that.

```bash
$ mv old_file.txt new_directory
$ mv old_file.txt new_file.txt
```

- `cp`: Copies files and directories.

```bash
$ cp old_file.txt new_directory
```

- `rm`: Deletes a file. Can be used with the `-r` option to recursively remove a directory and its contents.

```bash
$ rm old_file.txt
$ rm -r old_directory
```

- `find`: Searches for files and directories based on user criteria. You can use the `-name` option to specify a filename. The following example tries to find a file named `file.txt` in the root directory (`/`).

```bash
$ find / -name "file.txt"
```

- `grep`: Searches for patterns within text files. In the following example, `grep` is used to search for the word `word` in the file `file.txt`. Remember that if you are not in the same folder, you have to specify the location.

```bash
$ grep "word" file.txt
```

- `pwd`: Prints the current working directory. In other words, the path to the folder your shell is currently in.

```bash
$ pwd
```

Keep in mind that all these commands can be augmented with arguments, like we described in the previous chapter. For example, `rm` can be augmented with `-r` to delete a directory. To find out all of a command's capabilities, read the manual with `man`. For instance, `man rm`.

## Piping

In the Linux shell, you can redirect the output of one command into the input of another command. This is known as **piping**, due to the `|` (pipe) symbol.

As an example, let's say you want to list all the files in a directory, and then search for a specific file. You could use the `ls` command to list the files, and then the `grep` command to search for the specific file. With piping, you can do this in a single command:

```bash
$ ls | grep filename
```

You can pipe as many times as you need to in a single command, so get as creative as you need to!

## Unix philosophy

Piping is closely related to what is known as the **UNIX Philosophy**, which are a set of guiding principles for designing and developing programs. You can find this philosophy in practice all over the *GNU/Linux* ecosystem.

The *UNIX* philosophy is actually very straightforward, and is based on a few key ideas, the most essential being:

- Make each program do one thing well; if you need to do a new job, create a new program rather than complicating an existing one.
- Expect the output of every program to become the input to another, to allow for piping and reuse.

While not required, following the *UNIX* Philosophy can allow you to create programs that are simple, modular, and easy to maintain/understand, while also giving you a deeper understanding of how *UNIX-like* systems work.

## Portability

In addition to these useful tools, the GNU Coreutils are also designed to be *highly portable*. When a program is **portable**, it simply means that they can be ran on a variety of different hardware platforms and operating systems. 

## Conclusion

The GNU Coreutils form an integral part of the *Linux* ecosystem, providing a standard set of tools that are essential for working with *Linux/UNIX* systems. These tools are widely used by system administrators, developers, and essentially all users that rely on the command-line for their daily work.
