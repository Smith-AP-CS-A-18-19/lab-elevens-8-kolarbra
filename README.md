# Elevens 8

Follow the instructions provided for Activity 8 in the student lab guide. This is more of an exploratory lab, so you will not need to copy any of your previous code into the repo. Answer the questions from the Student Guide in this document and ensure that you save and push the repo. You have one week to complete this lab.

1. Discuss the similarities and differences between *Elevens*, *Thirteens*, and *Tens*.

    * They all deal cards, task the player with matching cards under certain conditions, and end when all cards have been matched or no moves remain, but they have different conditions for matching cards and different board sizes

2. As discussed previously, all of the instance variables are declared in the `Board` class. But it is the `ElevensBoard` class that “knows” the board size, and the ranks, suits, and point values of the cards in the deck. How do the `Board` instance variables get initialized with the `ElevensBoard` values? What is the exact mechanism?

    * Inheritance: The ElevensBoard class initializes its own variables for board size, ranks, suits, and values; then its constructor calls on that of the superclass and creates an ElevensBoard object with all the same properties as a Board object

3. Now examine the files `Board.java` and `ElevensBoard.java`, found in this repository. Identify the `abstract` methods in `Board.java`. See how these methods are implemented in `ElevensBoard`. Do they cover all the differences between *Elevens*, *Thirteens*, and *Tens* as discussed in question 1? Why or why not?

    * isLegal() and anotherPlayIsPossible() are both abstract because different games have different conditions for legal matches, but they all need to check whether these conditions are met. They do cover the differences because different games will have different implementations as is appropriate for their board sizes and match conditions.
