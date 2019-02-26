lsdl
====

A small shellscript to download multiple files on a list at once.
## Dependency
wget ( and maybe zsh )

## Usage

make a file with urls separated with newline:

```
test.dls:

http://www.example.com/image01.jpg
http://www.example.com/image02.jpg
http://www.example.com/image03.jpg
http://www.example.com/image04.jpg
```
on the same directory type **`lsdl`**!
Then, it will do three things:
 1. make a directory named "test/"
 2. download all the url in "test/"
 3. move the test.dls underneath test/ and rename it to "receipt"
 
If you have different lists in the same folder, it downloads it all!

## Create mode

If you put the `-c` option, it switches to create mode to create list files.

If you connect to a pipe. it reads from it too.
