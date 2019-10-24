# Input Validation Exercise Workbench

Design an algorithm that prompts the user to enter a positive nonzero number and validates the input.

Declare Real userInput
Display "Please enter a positive, nonzero number: "
Input userInput
If userInput <= 0 Then
   Display "Invalid Input"

Design an algorithm that prompts the user to enter a number in the range of 1 through 100 and validates the input.

Declare Real userInput
Display "Please enter a number between 1, 100: "
Input userInput
If userInput < 1 OR userInput > 100 Then
   Display "Invalid Input"

Design an algorithm that prompts the user to enter “yes” or “no” and validates the input. (Use a case-insensitive comparison.)

Declare String userInput
Display "Enter yes or no: "
Input userInput
If toLower(userInput) != "yes" OR toLower(userInput) != "no" Then
   Display "Invalid Input"

Design an algorithm that prompts the user to enter a number that is greater than 99 and validates the input.

Declare Real userInput
Display "Enter a number that is more than 99: "
Input userInput
If userInput <= 99 Then
   Display "Invalid Input"

Design an algorithm that prompts the user to enter a secret word. The secret word should be at least 8 characters long. Validate the input.

Declare String userInput
Display "Enter a secret word: "
Input userInput
While length(userInput) < 8
   Display "The secret word must be at least 8 characters long!"
   Display "Enter a secret word: "
   Input userInput

# Debugging Exercises

Why does the following pseudocode not perform as indicated in the comments?
```
// This program asks the user to enter a value
// between 1 and 10 and validates the input.
Declare Integer value

// Get a value from the user.
Display "Enter a value between 1 and 10."
Input value

// Make sure the value is between 1 and 10.
While value < 1 AND value > 10 // Logic error, AND should be OR
   Display "ERROR: The value must be between 1 and 10."
   Display "Enter a value between 1 and 10."
   Input value
End While
```
Why does the following pseudocode not perform as indicated in the comments?
```
// This program gets a dollar amount from the user
// and validates the input.
Declare Real amount

// Get the amount from the user.
Display "Enter a dollar amount"
Input amount

// Make sure the amount is not less than zero. If it is,
// get a new amount from the user.
While amount < 0  // does not reassigns input to amount in the loop, infinite loop if True
   Display "ERROR: The dollar amount cannot be less than 0."
   Display "Enter a dollar amount."
End While
```
The following pseudocode works, but it performs a case-sensitive validation of the user’s input. How could the algorithm be improved so the user does not have to pay attention to capitalization when entering a name?
```
// This program asks the user to enter a string
// and validates the input.
Declare String choice

// Get the user's response.
Display "Cast your vote for Chess Team Captain."
Display "Would you like to nominate Lisa or Tim?"
Input choice

// Validate the input.
While choice != "Lisa" AND choice != "Tim"
   Display "Please enter Lisa or Tim."
   Display "Cast your vote for Chess Team Captain."
   Display "Would you like to nominate Lisa or Tim?"
   Input response
End While
```
