
# Program 5-1
```
 1  // Variable declarations
 2  Declare Real sales, commission
 3  Declare String keepGoing = "y"
 4
 5  // Constant for the commission rate
 6  Constant Real COMMISSION_RATE = 0.10
 7
 8  While keepGoing == "y"
 9      // Get the amount of sales.
10      Display "Enter the amount of sales."
11      Input sales
12
13      // Calculate the commission.
14      Set commission = sales * COMMISSION_RATE
15
16      // Display the commission
17      Display "The commission is $", commission
18
19      Display "Do you want to calculate another"
20      Display "commission? (Enter y for yes.)"
21      Input keepGoing
22  End While
```
```
Program Output (with Input Shown in Bold)
Enter the amount of sales.
10000.00 [Enter] 
The commission is $1000
Do you want to calculate another
commission? (Enter y for yes.)
y [Enter] 
Enter the amount of sales.
5000.00 [Enter] 
The commission is $500
Do you want to calculate another
commission? (Enter y for yes.)
y [Enter] 
Enter the amount of sales.
12000.00  [Enter] 
The commission is $1200
Do you want to calculate another
commission? (Enter y for yes.)
n [Enter]
```
# Program 5-2
```
 1  // Declare a variable to hold the password.
 2  Declare String password
 3
 4  // Repeatedly ask the user to enter a password
 5  // until the correct one is entered.
 6  Do
 7     // Prompt the user to enter the password.
 8     Display "Enter the password."
 9     Input password
10
11     // Display an error message if the wrong
12     // password was entered.
13     If password != "prospero" Then
14        Display "Sorry, try again."
15     End If
16  Until password == "prospero"
17
18  // Indicate that the password is confirmed.
19  Display "Password confirmed."
```
```
Program Output (with Input Shown in Bold)
Enter the password.
ariel [Enter] 
Sorry, try again.
Enter the password.
caliban [Enter] 
Sorry, try again.
Enter the password.
prospero [Enter] 
Password confirmed.
```
# Program 5-3
```
1  Declare Integer counter
2  Constant Integer MAX_VALUE = 5
3
4  For counter = 1 To MAX_VALUE
5     Display "Hello world"
6  End For
```
```
Program Output
Hello world
Hello world
Hello world
Hello world
Hello world
```
# Program 5-10
```
 1  // Declare a counter variable
 2  Declare Integer counter
 3
 4  // Constant for the maximum value
 5  Constant Integer MAX_VALUE = 11
 6
 7  // Display the odd numbers from 1 through 11.
 8  For counter = 1 To MAX_VALUE Step 2
 9     Display counter
10  End For
```
```
Program Output
1
3
5
7
9
11
```

