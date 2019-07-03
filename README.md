# Strings Lab 1

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

Write code that prints out all the numbers from 1 to 10 as a single string.
(Hint: the `String()` function can convert an Int to a String)

var N = 10
var numString = ""
var i = 1

for _ in i...N {
numString += "\(i)" + " "
i += 1
}

print("\(numString)")

***
## Question 2

Write code that prints out all the even numbers from 5 to 51 as a single string.

var N = 51
var numString = ""
var i = 5

for _ in i...N {
if i % 2 == 0 {
numString += "\(i)" + " "
}
i += 1
}

print("\(numString)")


***
## Question 3

Write code that prints out every number ending in 4 between 1 and 60 as a single string.


var N = 60
var numString = ""
var i = 1

for _ in i...N {
if i % 10 == 0 {
numString += "\(i - 6)" + " "
}
i += 1
}

print("\(numString)")


***
## Question 4

Print each character in the string `"Hello world!"`

let helloWorld = "Hello world!"
var string = ""

for char in helloWorld {
string += "\(char)"
}

print(string)

***
## Question 5

Print out the last character in the string below.  You cannot use the Character literal "!" (i.e you must access `myStringSeven`'s characters).

`let myStringSeven = "Hello world!"`

let myStringSeven = "Hello world!"

var string = ""

for char in myStringSeven {
if char == "!" {
string += "\(char)"
}
}
print(string)

***
## Question 6

Write code that switches on a string, given the following conditions:
- If the string's length is even, print out every character.
- If the string's length is odd, print out every other character.


let string = "Hello world!!"

var i = 0

if string.count % 2 == 0 {
for char in string {
print(char)
}
} else {
for char2 in string {
if i % 2 == 0 {
print (char2)
}
i += 1
}
}

***
## Question 7

Initialize a String with a character. Show that it is a Character, and not another String, that you're using to initialize it.

????
***
## Question 8

Build five pairs of **canonically equivalent** strings, the first of each being a pre-composed character and the second being one that uses combinable unicode scalars. Show that they are equivalent.

let string1 = "Voulez-vous un caf\u{E9}?"
let string2 = "Voulez-vous un caf\u{65}\u{301}?"

print(string1 == string2)

let string3 = "Dale a la pi\u{00F1}ata!"
let string4 = "Dale a la pi\u{6E}\u{303}ata!"

print(string3 == string4)

let string5 = "Te\u{E1}"
let string6 = "Te\u{61}\u{301}"

print(string5 == string6)

let string7 = "Who\u{227}"
let string8 = "Who\u{61}\u{307}"

print(string7 == string8)

let string9 = "reverse \u{203}"
let string10 = "reverse \u{61}\u{311}"

print(string9 == string10)


***
## Question 9

**Using only Unicode**, print out `"HELLO WORLD!"`

print("\u{48}\u{45}\u{4C}\u{4C}\u{4F}\u{20}\u{57}\u{4F}\u{52}\u{4C}\u{44}\u{21}")


***
## Question 10

**Using only Unicode**, print out your name.

print("\u{4B}\u{65}\u{76}\u{69}\u{6E}\u{20}\u{4E}\u{61}\u{74}\u{65}\u{72}\u{61}")

***
## Question 11

**Using only Unicode**, print out `"HELLO WORLD!"` in another language.

print("\u{48}\u{4F}\u{4C}\u{41}\u{20}\u{4D}\u{55}\u{4E}\u{44}\u{4F}\u{21}")
***
## Question 12

Print the below flower box using the following information.

- The unicode number for ⚘ is U-2698
- The top and bottom of the box are represented by dashes and the rows are |
- Use the terminator argument in your print statements to print on the same line.
- Hint: It may be useful to try printing out a box of just one character to start then work your way from there.

```swift
Flower Box:
- - - - - - - - - - -
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
| ⚘ | ⚘ | ⚘ | ⚘ | ⚘ |
- - - - - - - - - - -
```

***
## Question 13

Write a program that sets up a chess board using Unicode.

```swift
Chess Board:
♖ ♘ ♗ ♕ ♔ ♗ ♘ ♖
♙ ♙ ♙ ♙ ♙ ♙ ♙ ♙




♟ ♟ ♟ ♟ ♟ ♟ ♟ ♟
♜ ♞ ♝ ♛ ♚ ♝ ♞ ♜



let whitePawn = "\u{2659}"
var whitePawns = ""
let whiteRook = "\u{2656}"
let whiteBishop = "\u{2657}"
let whiteKnight = "\u{2658}"
let whiteQueen = "\u{2655}"
let whiteKing = "\u{2654}"

let blackPawn = "\u{265F}"
var blackPawns = ""
let blackRook = "\u{265C}"
let blackBishop = "\u{265D}"
let blackKnight = "\u{265E}"
let blackQueen = "\u{265B}"
let blackKing = "\u{265A}"

print(whiteRook, whiteKnight, whiteBishop, whiteQueen, whiteKing, whiteBishop, whiteKnight, whiteRook)

for _ in 1...8 {
whitePawns += whitePawn + " "
}

print(whitePawns)

for _ in 1...4 {
print("")
}

for _ in 1...8 {
blackPawns += blackPawn + " "
}

print(blackPawns)

print(blackRook, blackKnight, blackBishop, blackQueen, blackKing, blackBishop, blackKnight, blackRook)

```

***
## Question 14

You are given a string stored in the variable `aString`. Create new string named `replacedString` that contains the characters of the original string with all the occurrences of the character `"e"` replaced by `"\*"`.

```swift
var aString = "Replace the letter e with \*"
// Your code here
 ```

Example:

Input:
`var aString = "Replace the letter e with *"`

Expected values:
`replacedString = "R*plac* th* l*tt*r * with *"`

var aString = "Replace the letter e with *"

var replacedString = ""

for char in aString {
if char == "e" {
print("*", terminator:"")
} else {
print(char, terminator: "")
}
}

***
## Question 15

You are given a string stored in variable `aString`. Create a new string called `reverse` that contains the original string in reverse order. Print the reversed string.

```swift
var aString = "this string has 29 characters"
var reverse = ""


//Your code here

var aString = "this string has 29 characters"

for char in aString.reversed() {
print(char, terminator: "")
}

```

Example:
Input:
`var aString = "Hello"`

Output:
`"olleH"`

***
## Question 16

You are given a string stored in variable `aString`. Print `true` if `aString` is a palindrome, and `false` otherwise. A **palindrome** is a string which reads the same backward or forward.

```swift
let aString = "anutforajaroftuna"

// Your code here


let aString = "anutforajaroftuna"
var reverse = ""

for char in aString.reversed() {
reverse += "\(char)"
}

print(aString == reverse)


```

Example 1:
Input:
`var aString = "anutforajaroftuna"`

Output:
`true`

Example 2:
Input:
`var aString = "Hello"`

Output:
`false`

***
## Question 17

You are given a string stored in variable `problem`. Write code so that you print each word of the string on a new line.

```swift
var problem = "split this string into words and print them on separate lines"

// Your code
```

Example:
Input:
`var problem ="split this string into words and print them on separate lines"`

Output:
```swift
split
this
string
into
words
and
print
them
on
separate
lines



var problem = "split this string into words and print them on separate lines"
var solution: [String] = problem.components(separatedBy: " ")

for word in solution {
print(word)
}



```

***
## Question 18

You are given a string stored in variable `problem`. Write code that prints the longest word in the string.

```swift
var problem = "find the longest word in the problem description"

var problem = "find the longest word in the problem description"
var array: [String] = problem.components(separatedBy: " ")
var longestWord = String()

for word in array {
if (word.count > longestWord.count) {
longestWord = word
}
}

print(longestWord)

```

Example:
Input:
`var problem = "find the longest word in the problem description"`

Output:
`description`

Hint: Keep track of the longest word you encounter and also keep track of its length.

***
## Question 19

Given a string in English, create a tuple containing the number of vowels and consonants.

```swift
let vowels = "aeiou"
let consonants = "bcdfghjklmnpqrstvwxyz"
let input = "Count how many vowels I have!"

var numberOfVowels = 0
var numberOfConsonants = 0

for char in input.lowercased() {
if vowels.contains(char) {
numberOfVowels += 1
} else if consonants.contains(char) {
numberOfConsonants += 1
}
}
var answer = (numberOfVowels,numberOfConsonants)

print("\(answer.0) vowels and \(answer.1) consonants")

```

***
## Question 20

Given a string of words separated by a `" "`. Write code that prints out the length of the last word.

If there is no last word print out `"No last word"`.

Example:
Input: `"How are you doing this Monday?"`

Output: `7`

***
