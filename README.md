# _Text Analyzer_

#### By _**Grace Kostanich & Maxwell Alvord**_

#### _A word-count text analyzer!_

## Technologies Used

* _HTML_
* _CSS_
* _JS_

## Description

_This is a webpage written in HTML using Bootstrap CSS for styling & JavaScript for functionality._

## Setup/Installation Requirements

* _Fork project to your own GitHub repository_ 
* _Clone that repository to your desktop_
* _Open index.html or view any files you'd like!_

## Known Bugs

* _No known issues_

## License

_none_

Copyright (c) _6/7/2022_ _Grace Kostanich & Maxwell Alvord_

-------------------------------------------------------------

Describe: wordCounter()

Test: "It should return 1 if a passage has just one word."
Code:
const text = "hello";
wordCounter(text);
Expected Output: 1

Test: "It should return 2 if a passage has two words."
Code:
const text = "hello there";
wordCounter(text);
Expected Output: 2

Test: "It should return 0 for an empty string."
Code: wordCounter("");
Expected Output: 0

Test: "It should return 0 for a string that is only spaces."
Code: wordCounter("            ");
Expected Output: 0

Test: "It should not count numbers as words."
Code: wordCounter("hi there 77 19");
Expected Output: 2

------------------------------------------------------

Describe: numberOfOccurrencesInText()

Test: "It should return 0 occurrences of a word for an empty string."
Code:
const text = "";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return 1 occurrence of a word when the word and the text are the same."
Code:
const text = "red";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 1

Test: "It should return 0 occurrences of a word when the word and the text are different."
Code:
const text = "red";
const word = "blue";
numberOfOccurrencesInText(word, text);
Expected Output: 0

Test: "It should return the number of occurrences of a word."
Code:
const text = "red blue red red red green";
const word = "red";
numberOfOccurrencesInText(word, text);
Expected Output: 4

Test: "It should return a word match regardless of case."
Code:
const text = "red RED Red green Green GREEN";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

Test: "It should return a word match regardless of punctuation."
Code:
const text = "Red! Red. I like red, green, and yellow.";
const word = "Red";
numberOfOccurrencesInText(word, text);
Expected Output: 3

---------------------------------------------------

Describe: omitOffensiveWords()

Test: "It should return undefined when the text is an empty string."
Code:
const text = ""
const word = "zoinks";
omitOffensiveWords(words, text);
Expected output: undefined

Test: "It should record if an offensive word is in the text"
Code:
const text = "zoinks";
const words = "offensiveWords";
omitOffensiveWords(words, text);
expected output: 1

Test: "It should return the amount of offensive words in the text when we have more than one offensive word"
Code:
const text = "hi how are you zoinks zoinks ZOINKS are you a muppeteer";
const word = offensiveWords;
omitOffensiveWords(words, text);
expected output: 4

Test: "It should remove offensive words from our text."
Code:
const text: "hi how loopdaloop you Zoinks zoinks ZOINKS are you a muppeteer";
const word: offensiveWords
omitOffensiveWords(words, text);
expected output: "hi how you are you a"