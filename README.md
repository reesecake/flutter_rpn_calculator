# WIP Flutter RPN Calculator

RPN calculator with Flutter

## Overview
As the title states, this project is an RPN grading calculator made using Flutter. The calculator itself is a basic model of the Free42 re-implementation of the HP-42S scientific calculator. The purpose of the calculator is for grading and features curving methods to substitute for spreadsheets.


### UI/UX
For the look and feel of the calculator, a basic layout was modeled after a basic mobile calculator. From there, additional buttons were added for more functionality (sqrt, pi). A dark orange was chosen for the background and the two main containers have their own colors. The display uses a gradient of black to darken the background color from right to left. The keypad uses gray and orange for the buttons.

Most of the calculator’s buttons perform normal functions (ie. numbers, operations). Using listeners and Dart streans, the calculator is able to perform its functions upon button presses.

### Operations Guide
When the calculator is first opened, the user will see the general layout of a simple calculator, shown above, with numeric buttons along with operator buttons on the right hand side. More complex functions, such as exponents, trigonometric ratios (sin, tan, cos,....) and statistics operations, WILL go above the numeric buttons. In the top display, the output is shown as a string.

Since this calculator is made with the intent of having statistical curving functions easy to access, there are three dedicated buttons for different curving methods. The root button will implement the square root curve on the list that is currently selected. The function for the root curve is F(x)=(100^(1-a))*(x^a), where x is the grade/value in the list and a is a value that the user gives. The bell button will apply the bell curve function on the list and the max button will apply a max curve. The bell curve uses the mean and standard deviation to set the grades, distributing them based on the value of the standard deviation. A max curve is when the highest score is set to be considered 100% and uses that new value as the one used to calculate grades for the rest of the class.
Lastly, there is a grd button, which shows a breakdown of the different grades that the class has earned. This shows the number of A’s, B’s,... etc. along with the plus/minus indicators.

