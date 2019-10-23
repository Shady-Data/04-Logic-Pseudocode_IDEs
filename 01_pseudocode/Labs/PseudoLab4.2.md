# CHOOSE THREE PROMPTS (unless mandatory ones are assigned)

# Roman Numerals

Design a program that prompts the user to enter a number within the range of 1 through 10. The program should display the Roman numeral version of that number. If the number is outside the range of 1 through 10, the program should display an error message.

Start // romanNumeral
    Declare Integer numEntry

    Display "Enter a number between 1 and 10, inclusive: "
    Input numEntry

    Select numEntry
        Case 1:
            Display "I"
        Case 2:
            Display "II"
        Case 3:
            Display "III"
        Case 4:
            Display "IV"
        Case 5:
            Display "V"
        Case 6:
            Display "VI"
        Case 7:
            Display "VII"
        Case 8:
            Display "VIII"
        Case 9:
            Display "IX"
        Case 10:
            Display "X"
        Default:
            Display "Error: outside of expected input range."
    End Select

Stop


# Areas of Rectangles

The area of a rectangle is the rectangle’s length times its width. Design a program that asks for the length and width of two rectangles. The program should tell the user which rectangle has the greater area, or whether the areas are the same.

Start // rectangleAreaCompare
    Declare Real length1, width1, length2, width2, area1, area2

    Display "Please enter the length of the first rectangle: "
    Input length1
    Display "Please enter the width of the first rectangle: "
    Input width1
    Display "Please enter the length of the second rectangle: "
    Input length2
    Display "Please enter the length of the second rectangle: "
    Input width2

    Set area1 = length1 * width1
    Set area2 = length2 * width2

    If area1 > area2 Then
        Display "The First Rectangle has the greater area."
    Else If area2 > area1 Then
        Display "The second Rectangle has the greater area."
    Else
        Display "Both Rectangles have the same area."
Stop

# Mass and Weight

Scientists measure an object’s mass in kilograms and its weight in Newtons. If you know the amount of mass of an object, you can calculate its weight, in Newtons, with the following formula:

![image](https://user-images.githubusercontent.com/47218880/67404289-c6b2d480-f578-11e9-80c0-9bfa15de3df7.png)

Design a program that asks the user to enter an object’s mass, and then calculates its weight. If the object weighs more than 1,000 Newtons, display a message indicating that it is too heavy. If the object weighs less than 10 Newtons, display a message indicating that it is too light.

# Magic Dates

The date June 10, 1960, is special because when it is written in the following format, the month times the day equals the year:

![image](https://user-images.githubusercontent.com/47218880/67404336-d92d0e00-f578-11e9-9801-6742f67d71fe.png)

Design a program that asks the user to enter a month (in numeric form), a day, and a two-digit year. The program should then determine whether the month times the day equals the year. If so, it should display a message saying the date is magic. Otherwise, it should display a message saying the date is not magic.

# Color Mixer

The colors red, blue, and yellow are known as the primary colors because they cannot be made by mixing other colors. When you mix two primary colors, you get a secondary color, as shown here:
```
When you mix red and blue, you get purple.

When you mix red and yellow, you get orange.

When you mix blue and yellow, you get green.
```
Design a program that prompts the user to enter the names of two primary colors to mix. If the user enters anything other than “red,” “blue,” or “yellow,” the program should display an error message. Otherwise, the program should display the name of the secondary color that results.

Start // colorMixer
    Declare String priColor1, priColor2

    Display "Please enter the first color to mix 'red, yellow, or blue': "
    Input priColor1
    Display "Please enter the second color to mix 'red, yellow, or blue': "
    Input priColor2

    Select priColor1
        Case red:
            Select priColor2
                Case red:
                    Display "Mixed color is still red."
                Case blue:
                    Display "Mixed color is purple."
                Case yellow:
                    Display "Mixed color is orange."
                Default:
                    Display "Error: not a primary color"
            End Select
        Case blue:
            Select priColor2
                Case red:
                    Display "Mixed color is purple."
                Case blue:
                    Display "Mixed color is still blue."
                Case yellow:
                    Display "Mixed color is green."
                Default:
                    Display "Error: not a primary color"
            End Select
        Case yellow:
            Select priColor2
                Case red:
                    Display "Mixed color is orange."
                Case blue:
                    Display "Mixed color is green."
                Case yellow:
                    Display "Mixed color is still yellow."
                Default:
                    Display "Error: not a primary color"
            End Select
        Default:
            Display "Error: not a primary color"
    End Select

Stop
# Book Club Points

Serendipity Booksellers has a book club that awards points to its customers based on the number of books purchased each month. The points are awarded as follows:
```
If a customer purchases 0 books, he or she earns 0 points.

If a customer purchases 1 book, he or she earns 5 points.

If a customer purchases 2 books, he or she earns 15 points.

If a customer purchases 3 books, he or she earns 30 points.

If a customer purchases 4 or more books, he or she earns 60 points.
```

Design a program that asks the user to enter the number of books that he or she has purchased this month and displays the number of points awarded.

Module main()
    Declare int booksPurchased

    getBooksPurchased(booksPurchased)
    If booksPurchased < 0 Then  // Check if a negative number was entered
        Set booksPurchased = 0  // Set negative number to avoid default case
    End If
    Select booksPurchased
        Case 0:
            Display "0 Points earned for this month."
        Case 1:
            Display "5 Points earned for this month."
        Case 2:
            Display "15 Points earned for this month."
        Case 3:
            Display "30 Points earned for this month."
        Default:
            Display "60 Points earned for this month."
    End Select
Stop

Module getBooksPurchased(int ref booksPurchased)
    Display "Please enter the number of books you purchased this month: "
    Input booksPurchased
return


# Software Sales

A software company sells a package that retails for $99. Quantity discounts are given according to the following table:

![image](https://user-images.githubusercontent.com/47218880/67404439-04aff880-f579-11e9-8496-6a778d4ce7d1.png)

Design a program that asks the user to enter the number of packages purchased. The program should then display the amount of the discount (if any) and the total amount of the purchase after the discount.

# Change for a Dollar Game

Design a change-counting game that gets the user to enter the number of coins required to make exactly one dollar. The program should ask the user to enter the number of pennies, nickels, dimes, and quarters. If the total value of the coins entered is equal to one dollar, the program should congratulate the user for winning the game. Otherwise, the program should display a message indicating whether the amount entered was more than or less than one dollar.

# Shipping Charges

The Fast Freight Shipping Company charges the following rates:
![image](https://user-images.githubusercontent.com/47218880/67404533-26a97b00-f579-11e9-8944-5cfaa2dc2729.png)
Design a program that asks the user to enter the weight of a package and then displays the shipping charges.

# Time Calculator

Design a program that asks the user to enter a number of seconds, and works as follows:

* There are 60 seconds in a minute. If the number of seconds entered by the user is greater than or equal to 60, the program should display the number of minutes in that many seconds.

* There are 3,600 seconds in an hour. If the number of seconds entered by the user is greater than or equal to 3,600, the program should display the number of hours in that many seconds.

* There are 86,400 seconds in a day. If the number of seconds entered by the user is greater than or equal to 86,400, the program should display the number of days in that many seconds.

Module main
    Declare Integer secondsEntry, secondsCalc, minutesCalc, hoursCalc, daysCalc

    call getSeconds()
    set secondsCalc = secondsEntry // copy user input into another variable to work with, preserves original input
    While secondsCalc > 60 // loop until the secondsCalc is less then 1 minute
        If secondsCalc > 86400 Then // check if any days are able to be pulled out of seconds
            set daysCalc = call calcDays(secondsCalc)
        Else If secondsCalc > 3600 Then // check if any hours are able to be pulled out of seconds
            set hoursCalc = call calcHours(secondsCalc)
        Else If secondsCalc > 60 Then // check if any minutes are able to be pulled out of seconds
            set minutesCalc = call calcMinutes(secondCalc)
        Else:
            Display "Something went wrong, You shouldn't be seeing this message! \n\nWhile loop failed to terminate"
            break
        End If
    Display secondsEntry, "is equivalent to ", daysCalc, " days ", hoursCalc, " hours ", minutesCalc, " minutes and ", secondsCalc, " seconds."
End Module



# Leap Year Detector

Design a program that asks the user to enter a year, and then displays a message indicating whether that year is a leap year or not. Use the following logic to develop your algorithm:

* If the year is evenly divisible by 100 and is also evenly divisible by 400, then it is a leap year. For example, 2000 is a leap year but 2010 is not.

* If the year is not evenly divisible by 100, but it is evenly divisible by 4, it is a leap year. For example, 2008 is a leap year but 2009 is not.

Module main
    Declare Integer yearVar
    Declare Boolean leapYear

    Display "Enter a year to determine if it's a leap year: "
    Input yearVar

    Set leapYear = call calcLeapYear(yearVar) //
    If leapYear Then  // executes if leapYear is True
        Display yearVar, "is a leap year."
    Else // executes if leapYear if False
        Display yearVar, "is not a leap year."
    End If
End Module

Module calcLeapYear(Integer yearVar)
    If yearVar % 100 == 0 AND yearVar % 400 == 0 Then // Check if yearVar is divisible by 100 and 400, no remainders
        return True
    Else If yearVar % 4 == 0 Then // Check if yearVar is evenly divisible by 4 if not divisible by 100
        return True
    Else
        return False
    End If
End Module