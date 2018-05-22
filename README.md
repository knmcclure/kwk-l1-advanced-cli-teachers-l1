## Advanced Command Line and Shell Scripting

![simpsons grocery store](https://metrouk2.files.wordpress.com/2015/06/simpsons-2.gif)

You've just been hired by your local grocery store to stock all the shelves with a delivery that has come in from the warehouse. Congratulations on your new job.

### Get the files
There are a couple of ways you can get these files. Choose the method that works for you. You can click `Open` at the top of this page. You could also go to the GitHub link at the top of the lab and, if you are familiar with Github already, clone the repo locally. Otherwise, click on the "Clone or Download" button then the "Download Zip" button on the right side of the screen. Once you've downloaded the file, double click it to unzip the file, and then drag the unzipped file (called 'kwk-l1-advanced-cli') to your development directory.

## Part 1: Write a shell script
You've learned about the different commands in your terminal (`ls`, `mv`, `rm`, `mkdir`, `touch`, etc), but now we're going to learn how to string these commands together by using **bash scripting**. A _bash script is essentially a file with a set of instructions inside of it that when called from the command line will run the commands in the order in which they are written in the file_. For example, in your development directory create a file called `test_script.sh`. Open this file in the text editor and add the follwing to the contents of the file:

```bash
ls;
mkdir this_is_a_directory_made_in_a_script;
mkdir another_directory;
touch this_is_a_directory_made_in_a_script/first_file.txt;
touch this_is_a_directory_made_in_a_script/second_file.txt;
mv this_is_a_directory_made_in_a_script/second_file.txt another_directory

```

Save and close the file and then run it in your terminal by typing `sh test_script.sh`. This will run all the commands in this bash script. From the `kwk-l1-advanced-cli` directory, run `learn` as usual to check your progress!

### Challenge 1
Using the mini-lesson above, write a bash script that will put all of the files in the delivery directory in their right locations. As part of the challenge:
- You cannot `cd` into any directories, you must stay in the root directory of the project.
- All commands should be written in a shell script called `stock_supermarket.sh`.

## Part 2: Search for code inside files

The `grep` command is awesome. It allows you to search through all the text inside files and returns the line that contains the text you're looking for. For example, create a new file in your development directory called `a_lot_of_text.txt`, and then copy and paste all the text from [this link](http://www.fullbooks.com/The-Adventures-of-Huckleberry-Finn-Complete1.html). Now, let's say we want to find all instances of the word 'dog'. We'd use the command:

```bash
grep dog a_lot_of_text.txt
```

This will show you all the lines that contain the word 'dog'.

If you want to search the text of many files in many directories, you can use the recursive flag `-r` to go through all files in directories within the start directory:

```
grep -r dog big_directory_with_sub_directories
```

### Challenge 2

Using the `grep` command, find out the following information:

* What food is otherwise known as _gorp_?
* Which food has the word _grapes_ in its text file?
* Which food may or may not be _gluten free_, based on its file text.
* Winston Churchill is hiding in a food's text file. What food?
* What food is used to ward off vampires?
* Name the food that has a joke about canteloupe hidden inside it.
* What food has a youtube link inside of it?
* What food has the word _sprinkles_ in it?

<p data-visibility='hidden'>KWK-L1 Advanced Command Line and Shell Scripting</p>
