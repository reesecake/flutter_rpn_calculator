# flutter_rpn_calculator

RPN calculator with Flutter

## Overview
As the title states, this project is an RPN grading calculator made using Flutter. The calculator itself is a basic model of the Free42 re-implementation of the HP-42S scientific calculator. The purpose of the calculator is for grading and features curving methods to substitute for spreadsheets.


### UI/UX
For the look and feel of the calculator, a basic layout was modeled after the simple RPN calculator example. From there, additional buttons were added for practical grading uses, such as curving. Shades of blue were chosen to distinguish the buttons of the calculator and CN1’s RoundButton border was used to resemble the simple, rounded appearance of many modern calculators such as Apple’s iOS calculator.
The display has much larger text for the stack than the model RPN calculator. Each item is ordered vertically and allows for digits to reach across the width of the screen. When using curving functions, the display changes to show the lists and related data.

Most of the calculator’s buttons perform normal functions (ie. numbers, operations). Using listeners, the calculator is able to perform its functions upon button presses. The X register is represented by a string to allow for the user to add decimal points and so, some methods require Double parsing to manipulate the values.
	In unaryOpOrConst(), the string is checked for emptiness and then a switch statement determines what unary operation needs to be performed.

### Operations Guide
When the calculator is first opened, the user will see the general layout of a simple calculator, shown above, with numeric buttons along with operator buttons on the right hand side. On the left, we have buttons to modify the currently entered numbers and operations. More complex functions, such as exponents, trigonometric ratios (sin, tan, cos,....) and statistics operations, are above the numeric buttons. In the top display, the first 4 values that are entered will be shown, labeled as T, Z, Y, X.
There are a few buttons that are specific to this calculator's requirements, including “sto” and “rcl”, which will display a different view showing the four available registers. Using the rcl button, we can recall the list and make that the current stack. If there is no list present, the sto button will allow the user to create a list and store values inside that list.
 Next, we have the stat button, which opens up a new display that shows some information about the currently selected list of numbers. This display shows the mean, median, mode, standard deviation, minimum and maximum values in the list.
Since this calculator was made with the intent of having statistical curving functions easy to access, there are three dedicated buttons for different curving methods. The root button will implement the square root curve on the list that is currently selected. The function for the root curve is F(x)=(100^(1-a))*(x^a), where x is the grade/value in the list and a is a value that the user gives. The bell button applied the bell curve function on the list and the max button applies a max curve. The bell curve uses the mean and standard deviation to set the grades, distributing them based on the value of the standard deviation. A max curve is when the highest score is set to be considered 100% and uses that new value as the one used to calculate grades for the rest of the class.
Lastly, there is the grd button, which shows a breakdown of the different grades that the class has earned. This shows the number of A’s, B’s,... etc. along with the plus/minus indicators.
This covers all of the extra requirements that this calcular has implemented, along with some of the basics of a calculator. The different displays are shown below, along with sample values that have been entered.

