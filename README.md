1 + 2 + 34 – 5 + 67 – 8 + 9 = 100
======
Write a program that outputs all possibilities to put + or - or nothing between the numbers 1, 2, ..., 9 (in this order) such that the result is always 100. For example: 1 + 2 + 34 – 5 + 67 – 8 + 9 = 100.

11 Posibbilities:
* 1 + 2 + 3 - 4 + 5 + 6 + 78 + 9
* 1 + 2 + 34 - 5 + 67 - 8 + 9
* 1 + 23 - 4 + 5 + 6 + 78 - 9
* 1 + 23 - 4 + 56 + 7 + 8 + 9
* 12 + 3 + 4 + 5 - 6 - 7 + 89
* 12 + 3 - 4 + 5 + 67 + 8 + 9
* 12 - 3 - 4 + 5 - 6 + 7 + 89
* 123 + 4 - 5 + 67 - 89
* 123 + 45 - 67 + 8 - 9
* 123 - 4 - 5 - 6 - 7 + 8 - 9
* 123 - 45 - 67 + 89

---
Matrix Rotate
======
Write a function to rotate an NxN matrix by 90 degrees. You should rotate it in place, meaning you can't use another matrix to perform the rotation, but instead you have to use the same given structure.

1 2 3   7 4 1
4 5 6   8 5 2
7 8 9   9 6 3


1   2  3  4
5   6  7  8
9  10 11 12
13 14 15 16
 
13  9  5  1
14 10  6  2
15 11  7  3
16 12  8  4

---
Reverse Words
======

Given a list of space separated words, reverse the order of the words. Each line of text contains L letters and W words. A line will only consist of letters and space characters. There will be exactly one space character between each pair of consecutive words.

this is a test		=> test a is this
foobar				=> foobar
all your base		=> base your all

Input: 
*5
*this is a test
*foobar
*all your base
*class
*pony along

---
Roman Numbers
======

The Romans wrote numbers using letters: I, V, X, L, C, D, M.

Write a function to convert from normal numbers to Roman Numerals.
There is no need to be able to convert numbers larger than about 3000. (The Romans themselves didn't tend to go any higher)

Examples
* 1990 = MCMXC
* 2008 = MMVIII
* 1999 = MCMXCIX

---
Bowling Game
======

The game consists of 10 frames. In each frame the player has two opportunities to knock down 10 pins. The score for the frame is the total number of pins knocked down, plus bonuses for strikes and spares.

A spare is when the player knocks down all 10 pins in two tries. The bonus for that frame is the number of pins knocked down by the next roll. So in frame 3 above, the score is 10 (the total number knocked down) plus a bonus of 5 (the number of pins knocked down on the next roll.)

A strike is when the player knocks down all 10 pins on his first try. The bonus for that frame is the value of the next two balls rolled.
In the tenth frame a player who rolls a spare or strike is allowed to roll the extra balls to complete the frame. However no more than three balls can be rolled in tenth frame.

REQUIREMENTS

Write a class named “Game” that has two methods
– roll(pins : int) is called each time the player rolls a ball. The argument is the number of pins knocked down.
– score() : int is called only at the very end of the game. It returns the total score for that game.

---
String Calculator
======

- Create a simple String calculator with a method int Add(string numbers)
	+ The method can take 0, 1 or 2 numbers, and will return their sum (for an empty string it will return 0) for example “” or “1” or “1,2”

- Start with the simplest test case of an empty string and move to 1 and two numbers
- Allow the Add method to handle an unknown amount of numbers
- Allow the Add method to handle new lines between numbers (instead of commas).
	+ the following input is ok:  “1\n2,3”  (will equal 6)
	+ the following input is NOT ok:  “1,\n” (not need to prove it - just clarifying)
- Support different delimiters
	+ to change a delimiter, the beginning of the string will contain a separate line that looks like this:   “//[delimiter]\n[numbers…]” for example “//;\n1;2” should return three where the default delimiter is ‘;’ .
- Calling Add with a negative number will throw an exception “negatives not allowed” - and the negative that was passed.
	+ if there are multiple negatives, show all of them in the exception message

**STOP HERE** if you are a beginner. Continue if you can finish the steps so far in less than 30 minutes.
- Numbers bigger than 1000 should be ignored, so adding 2 + 1001  = 2
- Delimiters can be of any length with the following format:  “//[delimiter]\n” for example: “//[&#42;&#42;&#42;]\n1&#42;&#42;&#42;2&#42;&#42;&#42;3” should return 6
- Allow multiple delimiters like this:  “//[delim1][delim2]\n” for example “//[&#42;][%]\n1&#42;2%3” should return 6.
	+ make sure you can also handle multiple delimiters with length longer than one char
