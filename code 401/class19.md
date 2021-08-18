# Automation

the technique of making an apparatus, a process, or a system operate automatically.

the creation and application of technology to monitor and control the production and delivery of products and services.


Automation professionals are responsible for solving complex problems in many vital aspects of industry and its processes. 

The work of automation professionals is critically important to the preservation of the health, safety, and welfare of the public and to the sustainability and enhancement of our quality of life.

## [Python Regular Expressions Tutorial](https://www.datacamp.com/community/tutorials/python-regular-expression-tutorial)

Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. 

If you've ever used search engines, search and replace tools of word processors and text editors 

some very useful functions provided by the re library, such as: `compile()`, `search()`, `findall()`, `sub()` for search and replace, `split()`
```
import re
```
The `match()` function returns a match object if the text matches the pattern. Otherwise, it returns None

`search()` : you scan through the given string/sequence, looking for the first location where the regular expression produces a match.

`group()` : returns the string matched by the re.
**`.` - A period. Matches any single character except the newline character.
```
re.search(r'Co.k.e', 'Cookie').group()
OUTPUT--> 'Cookie'
```

**`^` - A caret. Matches the start of the string.

```
re.search(r'^Eat', "Eat cake!").group()
OUTPUT--> 'Eat'
```

**`$` - Matches the end of string.
```
re.search(r'cake$', "Cake! Let's eat cake").group()
OUTPUT--> 'cake'

```
**`[abc]` - Matches a or b or c.

**`[a-zA-Z0-9]` - Matches any letter from (a to z) or (A to Z) or (0 to 9).
**`\` recognized escape character
+ If the character following the backslash is a recognized escape character, then the special meaning of the term is taken (Scenario 1)

+ Else if the character following the `\` is not a recognized escape character, then the `\` is treated like any other character and passed through (Scenario 2).

+ `\` can be used in front of all the metacharacters to remove their special meaning (Scenario 3).

**`\w` - Lowercase 'w'. Matches any single letter, digit, or underscore.
**`\W` - Uppercase 'W'. Matches any character not part of `\w`(lowercase w).

**`\s` - Lowercase 's'. Matches a single whitespace character like: space, newline, tab, return.

**`\S` - Uppercase 'S'. Matches any character not part of `\s` (lowercase s).

**`\d` - Lowercase d. Matches decimal digit 0-9.

**`\D` - Uppercase d. Matches any character that is not a decimal digit.

**The `+` symbol used after the `\d` for repetition.

**`\t` - Lowercase t. Matches tab.

**`\n` - Lowercase n. Matches newline.

**`\r` - Lowercase r. Matches return.

**`\A` - Uppercase a. Matches only at the start of the string. Works across multiple lines as well.

**`\Z` - Uppercase z. Matches only at the end of the string.

**`* `- Checks if the preceding character appears zero or more times starting from that position.

**`?` - Checks if the preceding character appears exactly zero or one time starting from that position.
**`{x} `- Repeat exactly x number of times.
**`{x,}` - Repeat at least x times or more.
**`{x, y}` - Repeat at least x times but no more than y times.

**The `+` and `*` qualifiers are said to be `greedy`
**`match.group()` without any argument is still the whole matched text as usual.
**The syntax for creating named group is: `(?P<name>...).` Replace the name part with the name you want to give to your group.
**The `...` represent the rest of the matching syntax.

[https://docs.python.org/3/library/re.html#re-syntax](https://docs.python.org/3/library/re.html#re-syntax)
[https://cheatography.com/mutanclan/cheat-sheets/python-regular-expression-regex/](https://cheatography.com/mutanclan/cheat-sheets/python-regular-expression-regex/)




## [shutil- High-level File Operations](https://pymotw.com/3/shutil/)

The shutil module includes high-level file operations such as copying and archiving.
### Copying Files
`copyfile()` copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.
```
import glob
import shutil

print('BEFORE:', glob.glob('shutil_copyfile.*'))

shutil.copyfile('shutil_copyfile.py', 'shutil_copyfile.py.copy')

print('AFTER:', glob.glob('shutil_copyfile.*'))
```

**The implementation of copyfile() uses the lower-level function copyfileobj(). While the arguments to copyfile() are filenames, the arguments to copyfileobj() are open file handles. The optional third argument is a buffer length to use for reading in blocks.

**The copy() function interprets the output name like the Unix command line tool cp. If the named destination refers to a directory instead of a file, a new file is created in the directory using the base name of the source.
**copy2() works like copy(), but includes the access and modification times in the metadata copied to the new file.

### Copying File Metadata

By default when a new file is created under Unix, it receives permissions based on the umask of the current user. To copy the permissions from one file to another, use copymode().

**copymode() to duplicate the permissions of the script to the example file.
**To copy other metadata about the file use copystat().

**Only the permissions and dates associated with the file are duplicated with copystat().

### Working With Directory Trees

shutil includes three functions for working with directory trees. To copy a directory from one place to another, use copytree(). 
It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.

**The symlinks argument controls whether symbolic links are copied as links or as files. 
**The default is to copy the contents to new files. If the option is true, new symlinks are created within the destination tree.

**copytree() accepts two callable arguments to control its behavior. 
**The ignore argument is called with the name of each directory or subdirectory being copied along with a list of the contents of the directory. It should return a list of items that should be copied. 
**The copy_function argument is called to actually copy the file.

### Finding Files

**The which() function scans a search path looking for a named file. 
The typical use case is to find an executable program on the shell’s search path defined in the environment variable PATH.

**which() takes arguments to filter based on the permissions the file has, and the search path to examine. The path argument defaults to os.environ('PATH'), but can be any string containing directory names separated by os.pathsep. 
**The mode argument should be a bitmask matching the permissions of the file.


## Archives

Python’s standard library includes many modules for managing archive files such as tarfile and zipfile. 

**Use make_archive() to create a new archive file. Its inputs are designed to best support archiving an entire directory and all of its contents, recursively. 

**Extract the archive with unpack_archive().

## File System Space
It can be useful to examine the local file system to see how much space is available before performing a long running operation that may exhaust that space.
disk_usage() returns a tuple with the total space, the amount currently being used, and the amount remaining free.




## Watchdog
Python API library and shell utilities to monitor file system events.
You can use pip to install watchdog quickly and easily:

`$ pip install watchdog`


