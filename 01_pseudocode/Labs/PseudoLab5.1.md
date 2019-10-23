#Exercise Workbench
* Design a While loop that lets the user enter a number. The number should be multiplied by 10, and the result stored in a variable named product. The loop should iterate as long as product contains a value less than 100.

Module main
   Declare real number, product

   set product = 0 // initializing with a value for while loop
   While product < 100
      Display "Enter a number: "
      Input number
      If number < 0 Then // check if number is negative
         number = number * -1 // multiply negative number by -1 to make number positive
      Else If number == 0 Then
         Display "Entering infinite loop!!!" // While loop will not terminate since 0 * 10 == 0
      End IF
      product = number * 10
   End while
End Module

* Design a Do-While loop that asks the user to enter two numbers. The numbers should be added and the sum displayed. The loop should ask the user whether he or she wishes to perform the operation again. If so, the loop should repeat; otherwise it should terminate.

Module main
   Declare real num1, num2, sum
   Declare String runAgain

   Do
      Display "Enter a number: "
      input num1
      Display "Enter another number: "
      input num2
      Set sum = num1 + num2
      Display "The sum is ", sum
      Display "Do you want to run the program again? yes or no?"
      input runAgain
   while runAgain != n or runAgain != no
   End While
End Module


* Design a For loop that displays the following set of numbers:

0, 10, 20, 30, 40, 50, . . . , 1000

Module main
   Declare Integer displayNum

   For displayNum 0 to 1000 Step 10
      Display displayNum
   End For
End Module

* Design a loop that asks the user to enter a number. The loop should iterate 10 times and keep a running total of the numbers entered.

Module main
   Declare Integer counter
   Declare Real number, total

   total = 0
   Set counter = 1
   While counter <= 10
      Display "Enter a number: "
      input number
      total += number
      set counter = counter + 1 // increment counter by 1
   End while
End Module

* Design a For loop that calculates the total of the following series of numbers:
![image](https://user-images.githubusercontent.com/47218880/67423054-31740800-f599-11e9-9565-031c1f729e1c.png)

Module main
   Declare Integer denominator, numerator
   Declare Real total, value

   set total = 0
   For number in 1 to 30
      Set numerator = number
      set denominator = 31 - number // if denominator is set to 30 a Zero division error could occur
      set value = numerator / denominator
      set total = total + value
   End For
End Module

* Design a nested loop that displays 10 rows of # characters. There should be 15 # characters in each row.

For row 1 to 10 step 1
   For charInRow 1 to 15 step 1
      Display charInRow
   End For
End For

* Convert the While loop in the following code to a Do-While loop:
```
Declare Integer x = 1
While x > 0
   Display "Enter a number."
   Input x
End While
```
* Convert the Do-While loop in the following code to a While loop:
```
Declare String sure
Do
  Display "Are you sure you want to quit?"
  Input sure
While sure != "Y" AND sure != "y"
```
* Convert the following While loop to a For loop:
```
Declare Integer count = 0
While count < 50
   Display "The count is ", count
   Set count = count + 1
End While
```
* Convert the following For loop to a While loop:
```
Declare Integer count
For count = 1 To 50
   Display count
End For
```
