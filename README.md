# Simple Bash Utils
## A training project. Development of cat and grep utilities in the C programming language. Equivalents of the utilities of the same name in Bash

## cat Usage

`cat [OPTION] [FILE]...`

### cat Options

| No. | Options | Description |
| ------ | ------ | ------ |
| 1 | -b (GNU: --number-nonblank) | numbers only non-empty lines |
| 2 | -e implies -v (GNU only: -E the same, but without implying -v) | but also display end-of-line characters as $  |
| 3 | -n (GNU: --number) | number all output lines |
| 4 | -s (GNU: --squeeze-blank) | squeeze multiple adjacent blank lines |
| 5 | -t implies -v (GNU: -T the same, but without implying -v) | but also display tabs as ^I  |

Building
```
cd ./src/cat
make build
```

Running
```
./s21_cat [OPTION] [FILE]...
```

Run tests
```
make tests
```

Cheak memory leaks
```
make leaks
```

To view the valgrind report, see the file `./test/e2` file

## grep Usage

`grep [options] template [file_name]`

### grep Options

| No. | Options | Description |
| ------ | ------ | ------ |
| 1 | -e | pattern |
| 2 | -i | Ignore uppercase vs. lowercase.  |
| 3 | -v | Invert match. |
| 4 | -c | Output count of matching lines only. |
| 5 | -l | Output matching files only.  |
| 6 | -n | Precede each matching line with a line number. |
| 7 | -h | Output matching lines without preceding them by file names. |
| 8 | -s | Suppress error messages about nonexistent or unreadable files. |
| 9 | -f file | Take regexes from a file. |
| 10 | -o | Output the matched parts of a matching line. |

Building 
```
cd ./src/grep
make build
```
Running 
```
./s21_grep [options] template [file_name]
```
Run tests 
```
make tests
```
Cheak memory leaks
```
make leaks
```
To view the valgrind report, see the file `./test/e2` file

## Note
Tests of both utilities compare the behavior of the utility with the original one in Linux Bash, using the specified flags and their combinations
