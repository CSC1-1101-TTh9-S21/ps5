# Problem Set 5

### Due Friday, March 12, 2021, at 11:59pm EST

For this problem set, you will submit to Canvas **a single .zip file**. Detailed instructions for what the .zip file should contain are at the end of this problem set. Note that if you do not submit the files as specified here, there will be a major deduction in your grade for this assignment. Following directions to the letter is a crucial skill for computer programming.

**Note: Your programs should all have the following format: import statements (if necessary); then function definitions (if there are any); then a `main()` function that gets the ball rolling and calls the functions you defined (if any); and finally outide all other functions, the call to `main()`.**

*Reminder:* I now expect you to write comments in your code! One point will be deducted if you do not provide comments explaining your code. Here's what I would like commented this time:

* Before every function, describe what it does and what its arguments are (if any).
* Before every variable, explain what value it is holding.
* Do not write comments at the end of a line unless they are really short.
* If you have a long comment, insert some line breaks so it doesn't trail off end of the screen.
* Leave a new line before each comment so they are easy to read.

And, as always, in every program, the first four lines (comments) should be:

* The name of the file.
* Your name.
* The date.
* A statement saying "This code is my own work. I did not share my code or look at the code of another student."

---

## Part 1: Madlibs
In this program, you will write your own interface for doing [Madlibs](https://en.wikipedia.org/wiki/Mad_Libs). Look at the text file called `madlib.txt`. You will see normal text interspersed with parts of speech in all caps, like this:

```
When I was VERB_IN_ING to PLACE , I found a NOUN on the sidewalk .
```

When you play Madlibs with friends with paper and pencil, only one person can see the text. That person asks the other players for words fitting the part of speech (e.g., noun, verb, place). Since the other players don't know what the text is about, they select whatever words come to mind that fit the part of speech, and in theory, hilarity ensures.

In this version of the game, the computer knows the text and asks the user for words. The computer then writes out the complete text to a file. 

Here are some requirements for this prorgram:

1. A function called `readMadLib(infile)`. This function takes as an argument a string that is the name a file. It opens the file, reads the whole file into a string, splits the string on space using `split()`, and returns the **list** that `split()` creates.

2. A function called `writeMadLib(mylist, outfile)`. This function taes as an argument a list, `mylist` and writes it out to a file, `outfile`.

3. A `main()` function. The main function does the following:

* Get a file name from the command line and pass it to `readMadLib()`. 
* Take the list returned by `readMadLib()`, and proceed through the list item by item. Each time you come across an item that is all caps, ask the user for a word in that category. Replace that item in the list with the word the user provides.
* call `writeMadLib(mylist, outfile)` with the modified list and an output file name.

Here is a sample run of the program using `madlib2.txt` as the input file.

<img src="pic1.png" width=500>

And here is what the output file looks like:

```
When I was swimming to Trader Joe's , I found a lampshade on the sidewalk . I picked it up and gave it to my fireplace who said " Meh !"
```

## Part 2: Guess my number
In the last problem set, you wrote a program in which the program randomly selected a letter of the alphabet and the user tried to guess it. This time, the tables will be turned: the computer will have to guess what the user is thinking. In addition, we'll switch from letters to integers between 1 and 100, inclusive, to make it a little more challenging.

The user will pick a number, and the computer will try to guess it. The user will not actually tell the computer anything other than "yes" or "no", so the computer will have to guess randomly. The one thing that guarantees the computer will eventually guess the number is that it is not allowed to guess the same number twice.



The `main()` code I have provided will use a function I wrote to randomly select a secret letter between *A* and *Z*. Your job is to write code, within the `main()` function, that will allow the user **10 chances** to try to guess the letter. After each guess, the program will tell the user one of four things: 

1. The secret letter comes before the user's guess in the alphabet, and they should try again.

2. The secret letter comes after the user's guess in the alphabet, and they should try again.

3. The user entered an invalid option (i.e., something that is not a **capital letter in the standard American English A through Z alphabet**), and they should try again.

4. The user entered the correct letter. The secret letter will be revealed, the user will be congratulated, and the program will end.

If the user uses all 10 guesses without guessing the correct letter, print out a message revealing the secret letter and wishing them better luck next time.

**Note**
 * You will use a `while` loop to control the flow of interaction. 
 * You should use `<` and `>` to help with alphabetical order. 
 * **You may not use `break` or `return`. The `while` loop condition will be the only way to break out of the loop.** 
 * *You will need to think carefully about how to make sure you print out the correct message when the while loop ends!*
 
Here are some example runs of the program:

<img src="pic2.png" width=700>


---

## What to turn in
If you haven't already, create a `ps4` folder. In your `p4` folder you should have three python scripts: `part1.py`, `part2.py`, and `part3.py`. Remove any other things you might have accidentally put in the folder, then zip the folder up using whatever means you normally use to zip things up (e.g., on a Mac, you can right click and select `Compress`).

Upload the `.zip` file you created to Canvas. 

Note that if you do not submit the files as specified here, there will be a major deduction in your grade for this assignment. Following directions to the letter is a crucial skill for computer programming.

**Don't forget your comments!**

### This problem set is due Friday, February 19, 2021, at 11:59pm EST
