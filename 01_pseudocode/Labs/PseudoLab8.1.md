
##  Payroll Program with Input Validation


Design a payroll program that prompts the user to enter an employee’s hourly pay rate and the number of hours worked. Validate the user’s input so that only pay rates in the range of $7.50 through $18.25 and hours in the range of 0 through 40 are accepted. The program should display the employee’s gross pay.


Module grossPayCalc
	Declare Real payRate, grossPay
	Declare Integer payHours

	Do
		Display "Enter employee's hourly pay rate: $"
		Display "Valid hourly pay rates are between $7.50 and $18.25."
		Input payRate
	While payRate < 7.50 OR payRate > 18.25
	Do
		Display "Enter employee's hours worked: "
		Display "Company Policy: No one works overtime!!!"
		Display "Valid hours are between 0 and 40."
		Input payHours
	While payHours < 0 OR payHours > 40
	Set grossPay = payHours * payRate
	Display :Employee's calculated gross pay is $", grossPay
End Module


## Theater Seating Revenue with Input Validation

A dramatic theater has three seating sections, and it charges the following prices for tickets in each section: section A seats cost $20 each, section B seats cost $15 each, and section C seats cost $10 each. The theater has 300 seats in section A, 500 seats in section B, and 200 seats in section C. Design a program that asks for the number of tickets sold in each section and then displays the amount of income generated from ticket sales. The program should validate the numbers that are entered for each section.


Module main
	Declare real revenue, sectionAProfits, sectionBProfits, sectionCProfits
	Constant Integer MAX_SEATS_A = 300
	Constant Integer MAX_SEATS_B = 500
	Constant Integer MAX_SEATS_C = 200

	Set sectionAProfits = getTicketsSales(20, MAX_SEATS_A)
	Set sectionBProfits = getTicketsSales(15, MAX_SEATS_B)
	Set sectionCProfits = getTicketsSales(10, MAX_SEATS_C)
	Set revenue = sectionAProfits + sectionBProfits + sectionCProfits

	Display "$", revenue
End Module

Function Real getTicketsSales(Real price, Integer maxSeats)
	Declare Integer ticketsSold
	Declare String sectionID

	Select maxSeats
		Case 300:
			Set sectionID = "A"
		Case 500:
			Set sectionID = "B"
		Case 200:
			Set sectionID = "C"
	End Select

	Display "Enter number of seats sold for ", sectionID, ": "
	Input ticketsSold

	While ticketsSold < 0 OR tiscketsSold > maxSeats
		Display "Ticket sales for section ", sectionID," cannot be negative or exceed the number of seats in the section (", maxSeats, ")"
		Display "Enter number of seats sold for ", sectionID, ": "
		Input ticketsSold
	End While

	Return price * ticketsSold
End Function

## Fat Gram Calculator

Design a program that asks for the number of fat grams and calories in a food item. Validate the input as follows:

Make sure the number of fat grams and calories is not less than 0.

According to nutritional formulas, the number of calories cannot exceed "fat grams X 9 "

Make sure that the number of calories entered is not greater than "fat grams X 9"

Once correct data has been entered, the program should calculate and display the percentage of calories that come from fat. Use the following formula:

![image](https://user-images.githubusercontent.com/47218880/67504468-0ba93a80-f64f-11e9-85d0-f080ac66a64a.png)

Some nutritionists classify a food as “low fat” if less than 30 percent of its calories come from fat. If the results of this formula are less than 0.3, the program should display a message indicating the food is low in fat.


Module fatGramCalc
	Declare Integer fatGrams, calories
	Declare Real percentCalsFromFat

	Do
		Display "Please enter the total calories: "
		Input calories
	While calories < 0

	Display "Please enter the amount of grams of fat: "
	Input fatGrams
	
	While fatGrams < 0 OR fatGrams * 9 > calories
		Display "Invalid entry! Amount of grams of fat cannot be negative"
		Display "Calculated calories from fat cannot exceed total calories (grams of fat * 9)"
		Display "Please enter the amount of grams of fat: "
		Input fatGrams
	End While

	Set percentCalsFromFat = ((fatGrams * 9) / calories) * 100
	Display "%", percentCalsFromFat, " calories from fat."
	If percentCalsFromFat < 30 Then
		Display "Low-Fat"
	End If
End Module


## Speeding Violation Calculator

Design a program that calculates and displays the number of miles per hour over the speed limit that a speeding driver was doing. The program should ask for the speed limit and the driver’s speed. Validate the input as follows:

The speed limit should be at least 20, but not greater than 70.

The driver’s speed should be at least the value entered for the speed limit ­(otherwise the driver was not speeding).
Once correct data has been entered, the program should calculate and display the number of miles per hour over the speed limit that the driver was doing.

# Rock, Paper, Scissors Modification (MANDATORY)

In a previous Programming Exercise option you were asked to design a program that plays the Rock, Paper, Scissors game. In the program, the user enters one of the three strings—"rock", "paper", or "scissors"—at the keyboard. Add input validation (with a case-insensitive comparison) to make sure the user enters one of those strings only.
(If you didnt design one, here is a version of that game program to work with) 

// Copied from PseudoLab7.1, then modified

Module main
	Declare String compChoice, userChoice, result
 	Do
		set compChoice = rpsComp(random(1, 3))
		set userChoice = rpsUser()
		set result = rps(userChoice, compChoice)
		Select result
			Case "Win":
				Display "You Win!"
			Case "Lose":
				Display "You Lose!"
			Case "Draw":
				Continue
			Case "Failure":
				Display "How did you get here?"
			Default:
				Display "You should never see this!!!"
		End Select
	While result == "Draw"
End Function

Function String rpsComp(Integer num)
  Select num
    Case 1:
      Return "rock"
    Case 2:
      Return "paper"
    Case 3:
      Return "scissors"
    Default:
      Return "Something went wrong"
  End Select
End Function


Function String rpsUser()
	Declare String userInput
	Do
		Display "Select either 1: rock, 2: paper, 3: scissors: "
		Input userInput
	While userInput != "1" OR userInput != "2" OR userInput != "3" OR toLower(userInput) != "rock" OR toLower(userInput) != "paper" OR toLower(userInput) != "scissors"

	If userInput == "1" OR toLower(userInput) == "rock"
    	Return "rock"
  	Else If userInput == "2" OR toLower(userInput) == "paper"
    	Return "paper"
  	Else If userInput == "3" OR toLower(userInput) == "scissors"
    	Return "scissors"
  	End If
End Function


Function String rps(String user, String comp)
  Display "You played ", user
  Display "Computer played ", comp
  If user == comp Then
    Display "Draw! Play Again until a winner is chosen"
    Return "Draw"
  Else If user == "rock" AND comp == "paper"
    Display "Paper wraps Rock."
    Return "Lose"
  Else If user == "paper" AND comp == "rock"
    Display "Paper wraps Rock."
    Return "Win"
  Else If user == "rock" AND comp == "scissors"
    Display "Rock smashes Scissors."
    Return "Win"
  Else If user == "scissors" AND comp == "rock"
    Display "Rock smashes Scissors."
    Return "Lose"
  Else If user == "scissors" AND comp == "paper"
    Display "Scissors cuts Paper."
    Return "Win"
  Else If user == "paper" AND comp == "scissors"
    Display "Scissors cuts Paper."
    Return "Lose"
  Else
    Return "Failure"
  End If
End Function

### Program "Rock,Paper,Scissors"

```
// main module
Module main()
// Local variables
Declare Integer computer, player

// Get computer number
Set computer = Rand(1, 3)

// Get player number
Call getNumber(player)

// Show winner
Call showWinner(computer, player)

End Module

// The getNumber module gets an integer
Module getNumber(Integer Ref inputAnswer)
		Display “Enter 1 for rock, 2 for paper, 3 for scissors:  “
		Input inputAnswer
End Module

// The showWinner module shows if number is a prime
Module showWinner(Integer computer, player)
Declare Integer which

Display “Computer chose “, whichChoice(computer)
If computer == player Then
	Display “Player made same choice.  Play again.”
Else
Set which = whoWon(computer, player)
If which == 1 Then
		Display “Computer wins.”
Else
If which == 2 Then
			Display “Player wins.”
		Else
			Display “No winner.”
		End If
End If
End If

End Module

// The whichChoice function displays choice 
Function String whichChoice (Integer number)

If number == 1 Then
	Return “rock”
Else
If number == 2 Then
		Return “paper”
	Else
		Return “scissors
	End If

End Function

// The whoWon function selects winner 
Function Integer whoWon(computer, player)
// 1 = rock, 2 = paper, 3 = scissors
// rock smashes scissors
// scissors cuts paper
// paper wraps rock

	// both choose same no winner
If computer == player then
		Return 0
	End If

	// test computer chose rock
	If computer == 1 then
		If player == 2 then
			Return 2  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 1  // rock smashes scissors
		End If
End If

	// test computer chose paper
	If computer == 2 then
		If player == 1 then
			Return 1  // paper wraps rock
		End If
Else
		If player == 3 then
			Return 2  // scissors cuts paper
		End If
End If

	// test computer chose scissors
	If computer == 3 then
		If player == 1 then
			Return 2  // rock smashes scissors 
		End If
Else
		If player == 2 then
			Return 1  // scissors cuts paper
		End If
End If

	Return 0

End Function
```
