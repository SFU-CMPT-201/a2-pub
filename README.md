# Assignment 2: Bash Scripting

A bash script is something that you will encounter quite frequently when you use Linux. You can
think of it as a task automation tool---it allows you to create a single command that executes
multiple commands. It's not just that you can execute a series of commands sequentially. You can do
much more complicated things, using variables, if-else conditionals, etc., similar to what you can
do with a general-purpose programming language. In this assignment, you will learn the basics of
bash scripting.

We will again use a tutorial from [Ryan's Tutorials](https://ryanstutorials.net). The URL of the
bash script tutorial is [this](https://ryanstutorials.net/bash-scripting-tutorial/). Your task is to
finish the tutorial, but there are extra instructions you need to follow.

## Extra Instructions

Similar to the command-line interface tutorial, there are activities described at the end of each
section and those are the basis of your grade. However, we have made slight modifications to these
activities for easier grading. As a result, you need to complete the activities that we describe
below, not the ones from the tutorial.

Of course, you need to complete the activities using `nvim` on our VM. As mentioned before, we have
configured our `nvim` so that it occasionally takes a snapshot of the file you are editing and saves
the snapshot to a directory named `.nvim`. For this and all future assignments, you need to push
this directory as part of your submission. We will check this directory, analyze the snapshots to
make sure that you are using `nvim`, and use the analysis results as part of our grading. So make
sure you always use `nvim` for this and all future assignments.

### Using Bash

It is important to note that the tutorial assumes that you are using bash. However, you're using zsh
on our VM, which is a different shell. You can enter `which $SHELL` to find out which shell you're
using. Zsh behaves slightly differently from bash (albeit not much), so when you test out commands
before you include them in your bash script, it is important to do it using bash, not zsh. You can
simply enter `bash` and it will give you a bash shell. That way, you can test out various commands
using bash. After you're done, enter `exit` to return to the original zsh shell. Note that we have
configured zsh on our VM to enable many features, e.g., custom prompt, autocompletion, git support,
etc. When you use bash, you won't have access to those features.

### Neovim Linter for Bash

As you write bash scripts using our Neovim, you will notice that it shows various suggestions. This
is because we have installed a *linter* called [ShellCheck](https://www.shellcheck.net/). A linter
is a program that analyzes code and reports errors, bugs, and suggestions. It is a very common
programming tool and we highly encourage you to use it for all programming tasks, regardless of
the language and the editor you use. Using a linter, you can learn a lot about writing clean and
reliable code and following best practices. In fact, we have installed Neovim linters for C/C++ as
well, as you will see in later assignments.

### Activities for `2. Variables`

* Create a script named `2.variables.1.sh` which will accept command line arguments and echo out how
  many arguments there are and what the second argument is. The format of the output should be the
  number of arguments followed by a single space followed by the second argument. This *must* be
  your format. Otherwise, the grader will fail.
* Create a script named `2.variables.2.sh` which will print a random word. There is a file
  containing a list of words (usually /usr/share/dict/words or /usr/dict/words). Print a random word
  from that file. Look at the tutorial's activity description for a hint.
* Expand the previous activity so that if a number is supplied as the first command line argument
  then it will select from only words with that many characters. Look at the tutorial's activity
  description for a hint.
* Create a script named `2.variables.3.sh` which will take a filename as its first argument and
  create a dated copy of the file. eg. if our file was named file1.txt it would create a copy named
  2023-08-02_file1.txt. (To achieve this you will probably want to play with command substitution
  and the command `date`)

### Activities for `3. Input`

* Create a script named `3.input.1.sh` which will ask the user for a last name, a first name, and an
  address, and then combine these into a single message which is echo'd to the screen. The message
  format should be `<first name> <last name>, <address>`. Note that there is a comma between the
  name and the address.
* Add to the previous script to add in two command command line arguments and two system variables,
  `$TERM` and `$PWD`. The message format should be `$TERM, $PWD, <first name> <last name>,
  <address>`. The script name should be `3.input.2.sh`.
* Create a script named `3.input.3.sh` which will take data from STDIN and print the 3rd line only.

### Activities for `4. Arithmetic`

* Create a script named `4.arithmetic.1.sh` which will take two command line arguments and then
  multiply them together using each of the methods detailed above.
* Write a Bash script named `4.arithmetic.2.sh` which will print tomorrows date. (Hint: use the
  command `date`)
* Remember when we looked at variables we discovered $RANDOM will return a random number. This
  number is between 0 and 32767 which is not always the most useful. Let's write a script named
  `4.arithmetic.3.sh` which will use this variable and some arithmetic (hint: play with modulus) to
  return a random number between 0 and 100.
* Now let's play with the previous script. Modify it so that you can specify as a command line
  argument the upper limit of the random number. Can you make it so that a lower limit can be
  specified also? E.g. if I ran ./random.sh 10 45 it would only return random numbers between 10 and
  45. Name this script `4.arithmetic.4.sh`.

### Activities for `5. If Statements`

* Create a script named `5.if.1.sh` which will take 2 numbers as command line arguments. It will
  print to the screen the larger of the two numbers.
* Create a script named `5.if.2.sh` which will accept a file as a command line argument and check if
  the file is executable or writable. You should print a message with true/false for each. For
  example, if the file is both executable and writable, the message should be `true, true`. If the
  file is executable but not writable, the message should be `true, false`.

### Activities for `6. Loops`

* Create a script named `6.loops.1.sh` which will print the numbers 1 - 10 (each on a separate line)
  and whether they are even or odd. The format should be `number, even/odd` e.g., `1, odd`.
* Write a script named `6.loops.2.sh` which will take a single command line argument (a directory)
  and will print each entry in that directory, each on a separate line. If the entry is a file it
  will print its size (just the size, not the file name). If the entry is a directory it will print
  how many items are in that directory (just how many items there are, not the directory name).

### Submission

Make sure you use git to push all the scripts you wrote and files/directories you created, including
`.nvim/`, for grading.

# Next Steps

You need to accept the invite for the next assignment (A3).

* Get the URL for A3. Go to the URL on your browser.
* Accept the invite for Assignment 3 (A3).
* If you are not in `units/02-tools` directory, go to that directory.
* Clone the assignment repo.
