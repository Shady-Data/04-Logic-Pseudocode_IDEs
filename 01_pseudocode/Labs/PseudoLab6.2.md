# Array Programming Projects Choose 4 of the prompts.

## Total Sales

Design a program that asks the user to enter a store’s sales for each day of the week. The amounts should be stored in an array. Use a loop to calculate the total sales for the week and display the result.

## Lottery Number Generator

Design a program that generates a 7-digit lottery number. The program should have an Integer array with 7 elements. Write a loop that steps through the array, randomly generating a number in the range of 0 through 9 for each element. Then write another loop that displays the contents of the array.

## Rainfall Statistics

Design a program that lets the user enter the total rainfall for each of 12 months into an array. The program should calculate and display the total rainfall for the year, the average monthly rainfall, and the months with the highest and lowest amounts.

## Number Analysis Program

Design a program that asks the user to enter a series of 20 numbers. The program should store the numbers in an array and then display the following data:
```
The lowest number in the array

The highest number in the array

The total of the numbers in the array

The average of the numbers in the array
```

## Charge Account Validation

Design a program that asks the user to enter a charge account number. The program should determine whether the number is valid by comparing it to the following list of valid charge account numbers:
```
5658845  4520125  7895122  8777541  8451277  1302850
8080152  4562555  5552012  5050552  7825877  1250255
1005231  6545231  3852085  7576651  7881200  4581002
```
These numbers should be stored in an array. Use the sequential search algorithm to locate the number entered by the user. If the number is in the array, the program should display a message indicating the number is valid. If the number is not in the array, the program should display a message indicating the number is invalid.

## Days of Each Month

Design a program that displays the number of days in each month. The program’s output should be similar to this:
```
January has 31 days.
February has 28 days.
March has 31 days.
April has 30 days.
May has 31 days.
June has 30 days.
July has 31 days.
August has 31 days.
September has 30 days.
October has 31 days.
November has 30 days.
December has 31 days.
```
The program should have two parallel arrays: a 12-element String array that is initialized with the names of the months, and a 12-element Integer array that is initialized with the number of days in each month. To produce the output specified, use a loop to step through the arrays getting the name of a month and the number of days in that month.

## Phone Number Lookup

Design a program that has two parallel arrays: a String array named people that is initialized with the names of seven of your friends, and a String array named phoneNumbers that is initialized with your friends’ phone numbers. The program should allow the user to enter a person’s name (or part of a person’s name). It should then search for that person in the people array. If the person is found, it should get that person’s phone number from the phoneNumbers array and display it. If the person is not found in the people array, the program should display a message indicating so.

##  Payroll

Design a program that uses the following parallel arrays:

empId: An array of seven Integers to hold employee identification numbers. The array should be initialized with the following numbers:
```
56588 45201 78951 87775 84512 13028 75804
```
hours: An array of seven Integers to hold the number of hours worked by each employee.

payRate: An array of seven Reals to hold each employee’s hourly pay rate.

wages: An array of seven Reals to hold each employee’s gross wages.

The program should relate the data in each array through the subscripts. For example, the number in element 0 of the hours array should be the number of hours worked by the employee whose identification number is stored in element 0 of the empId array. That same employee’s pay rate should be stored in element 0 of the payRate array.

The program should display each employee number and ask the user to enter that employee’s hours and pay rate. It should then calculate the gross wages for that employee (hours times pay rate), which should be stored in the wages array. After the data has been entered for all the employees, the program should display each employee’s identification number and gross wages.

##  Driver’s License Exam

The local driver’s license office has asked you to design a program that grades the written portion of the driver’s license exam. The exam has 20 multiple choice questions. Here are the correct answers:
```
B

D

A

A

C

A

B

A

C

D

B

C

D

A

D

C

C

B

D

A
```
Your program should store these correct answers in an array. (Store each question’s correct answer in an element of a String array.) The program should ask the user to enter the student’s answers for each of the 20 questions, which should be stored in another array. After the student’s answers have been entered, the program should display a message indicating whether the student passed or failed the exam. (A student must correctly answer 15 of the 20 questions to pass the exam.) It should then display the total number of correctly answered questions, the total number of incorrectly answered questions, and a list showing the question numbers of the incorrectly answered questions.

## Saddle Points

Design a program that has a two-dimensional integer array with 7 rows and 7 columns. The program should store a random number in each element. Then, the program should search the array for saddle points. A saddle point is an element whose value is less than or equal to all the other values in the same row, and greater than or equal to all the other values in the same column. The program should display all of the saddle point values found in the array (if any).

## Tic-Tac-Toe Game

Design a program that allows two players to play a game of tic-tac-toe. Use a two-dimensional String array with three rows and three columns as the game board. Each element of the array should be initialized with an asterisk (*). The program should run a loop that does the following:
```
Displays the contents of the board array.

Allows player 1 to select a location on the board for an X. The program should ask the user to enter the row and column number.

Allows player 2 to select a location on the board for an O. The program should ask the user to enter the row and column number.

Determines whether a player has won or if a tie has occurred. If a player has won, the program should declare that player the winner and end. If a tie has occurred, the program should say so and end.

Player 1 wins when there are three Xs in a row on the game board. Player 2 wins when there are three Os in a row on the game board. The winning Xs or Os can appear in a row, in a column, or diagonally across the board. A tie occurs when all of the locations on the board are full, but there is no winner.
```
## Lo Shu Magic Square

The Lo Shu Magic Square is a grid with 3 rows and 3 columns shown in Figure below. The Lo Shu Magic Square has the following properties:
![image](https://user-images.githubusercontent.com/47218880/67577307-d1e73b00-f705-11e9-91ba-8acf75ad7a5d.png)

The grid contains the numbers 1 through 9 exactly.

The sum of each row, each column, and each diagonal all add up to the same number. This is shown in Figure below.
![image](https://user-images.githubusercontent.com/47218880/67577377-f9d69e80-f705-11e9-9907-1a522d98cc16.png)

In a program, you can simulate a magic square using a two-dimensional array. Design a program that initializes a two-dimensional array with values entered by the user. The program should determine whether the array is a Lo Shu Magic Square.
