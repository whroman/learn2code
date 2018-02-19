# exploring the file system
(new execs in this lesson: cd, touch, man, rm)
(length: 25-30 mins)

## what is a file system?
- a collection of files and directories
- directories can only hold files or other directories
- `Finder` is probably how you're most familiar to getting around a file system
	- show example with finder
- in the terminal, we have to use commands in order to navigate the file system, which we will now learn to do

## navigating the file system
- we're going to use a new executable, `cd`
- it stands for "change directory"

- (EXEC) `ls .`
	- see the dirs and files of your current dir
- (EXEC) `cd Documents`
	- english translation: <change directory to> <Documents> 
- (EXEC) `ls .`
	- see the dirs and files of `Documents`
	- compare to Finder
- (EXEC) `cd ../`
	- english translation: <change directory to> <parent directory>
	- family relations are used to describe file systems:
		- parent, child, sibling
		- show example of each relationship in Finder 
	- now we're back where we started
- (EXEC) `ls .`
	- now we see that these are the same files and dirs that we had when we began

### creating and deleting files
- (EXEC) `touch hello.txt`
	- english translation: <create a file> <called hello.txt> 
- (Q) how can we check to see whether this file exists?
	- (EXEC) `ls .`
	- view in finder
	- show file through both methods
- (EXEC) `rm hello.txt`
	- english translation: <ReMove> <hello.txt>
- (Q) how can we make sure this file was deleted?
	- same as above

## command history
- you can press "up arrow" to cycle back through your history of executed commads
- use "down arrow" to cycle forward

## errors are your friend
- cycle through your history and get to (EXEC) `rm hello.txt`
- execute it
- result is error: (EXEC) `rm: foo.txt: No such file or directory`
- we were telling the terminal to delete a file that doesnt exist, so the terminal let us know that this file doesnt exist

### creating directories
- we're going to create a new directory, so lets make sure that it doesnt exist yet in our file system:
	- (EXEC) `ls .`
	- (EXEC) `mkdir hello`
		- english translation: <create a directory> <called "hello">

### command history
- use terminal history ("up arrow") to get to `ls .` and execute it
	- make sure that the `hello` dir is there

### attempt to delete a directory
- (EXEC) `rm hello`
	- english translation: <remove> <"hello">
	- `rm: hello/: is a directory`
	- what do we do...?

### `man <exec>`
- english translation: <show me the MANual for> <any executable>
- lets use `man` to find out if we can use `rm` to delete dirs
- (EXEC) `man rm`
	- we're in a file-read mode!
	- interface:
		- "space bar"   || 	"scroll down"
		- "b" 			|| 	"scroll up"
		- "q"   		||  "exit read mode"
	- find entry for `-d`
	- press `q`

### (EXEC) `rm -d hello`
					   					 exec     option          argument
- english translation: <remove> <the directory> <"hello">
- options are always specified with a `-`
- we should have succeeded this time in deleting `hello`
- check using `ls .`

### FUN FACT
- dont do this!
- `sudo rm -rf .`


### command options
if `commands` are like sentences to computers,
and `executables` are like verbs to computers,
and `arguments` are like nouns to computers,
then what are `options`?

options are like adverbs. they modify our exectuables/verbs/actions.


