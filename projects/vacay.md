---
layout: project
type: project
image: img/cotton/hangman.png
title: "Hangman Game"
date: 2022
published: true
labels:
  - Scratch
summary: "A Hangman Game on Scratch"
---

<img src="https://github.com/user-attachments/assets/478d10c6-eee7-431b-82a5-ef245797a758" width="300" />

**Hangman Game in Scratch: AP Computer Science Final Project**

For my AP Computer Science final project, I developed a Hangman game in Scratch that integrates key programming principles such as loops, conditionals, randomization, and user input handling. The primary objective of the project was to implement the essential game mechanics while demonstrating an understanding of fundamental programming concepts and structuring an engaging, interactive user experience.

**Game Overview**
The game challenges the player to guess a randomly selected 5-letter word. To add variety, I manually created a list of 31 words, each approximately five letters long. The game randomly selects a word from this list and presents it as a series of blank spaces, representing each letter in the word. The player is prompted to guess a letter, and if the guess is correct, the corresponding letter is revealed in the word's blank spaces. If the guess is incorrect, a body part is added to the "hangman" figure. The game features six body parts (head, body, arms, legs) that visually indicate how many incorrect guesses the player has made.

The game ends when the player either correctly guesses the word or the hangman figure is fully drawn, at which point the word is revealed, and the game concludes.

<ins>Implementation Details</ins>
The core of the game's functionality relies on several key programming constructs:

<ins>Random Word Selection:</ins> I created a list of words and used a random number generator to select one word from this list. The random selection is implemented using Scratch's pick random block. The word is then split into individual letters, and each is initially represented by a blank space.

<ins>User Input Handling:</ins> User input is handled via the ask block, prompting the player to guess a letter. The player's guess is stored in a variable, which is then used to check against the letters of the randomly chosen word.

<ins>Checking the Guess:</ins> A custom procedure, checkGuess, iterates through the letters of the word to check if the guessed letter exists. If the letter is found, it is revealed in the word display; otherwise, an incorrect guess is logged, and a body part is added to the hangman figure.

<ins>Game Flow Control:</ins> The game's flow is controlled through a combination of loops and conditionals. The game continues as long as the number of incorrect guesses is less than the allowed maximum (six), and it terminates when either the word is fully guessed or the hangman is fully drawn.

**Interactive Features**
To enhance the user experience, I implemented several interactive features:

<ins> Button Interaction:</ins>Start The "Start" button grows when the player hovers their cursor over it, providing visual feedback. This was achieved by modifying the button's size dynamically based on the player's interaction.

<ins>Dynamic Feedback:</ins> Throughout the game, the player receives immediate visual feedback. Correct guesses are revealed in the word display, while incorrect guesses trigger the display of body parts on the hangman. The game also provides immediate updates to the word display after each guess.

**Reflections**
This project allowed me to apply key programming concepts such as loops (for iterating over the word to check guesses), conditionals (to determine whether a guess is correct or incorrect), and randomization (to select a random word). In addition to implementing core game logic, I also focused on enhancing the user interface through custom artwork and dynamic interactions.

Overall, this Hangman game effectively combines both technical problem-solving and creative design. It showcases my ability to design and implement a program that is both functional and engaging. The project also helped me refine my skills in managing user input, handling data structures (such as lists), and implementing custom procedures, which are crucial in software development.

You can check out my project on Scratch [here](https://scratch.mit.edu/projects/665480823).


