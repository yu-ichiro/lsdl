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

## Options

### Create mode (-c)

If you put the `-c` option, it switches to create mode to create list files.

If you connect to a pipe. it reads from it too.

### Wget Options (-w)

You can add custom wget options to every download

```
lsdl -w ...
```

### Sleep Option (-s)

You can add a rate limit in seconds to sleep between each download

```
lsdl -s 1 # sleeps 1 second after each download
```

## Cookies

If you need cookie to access the resource, you can simply add a .cookie file to the same level as the .dls file, and lsdl will automatically include it.
