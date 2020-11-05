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


<p align="center">
  <img src="https://lh3.googleusercontent.com/OjHKrYKZ8jzRMSK1lUjZyq83_cLZAZiav0kDimQ765by6EJLHPO2b-tjTodNdDxLLw30erHCMdCN7eGDhHPRW-n6l4AiGzt53Z2DrfDkZGJrXZV-FEZX7XHrs5TLydmHb6lPFJ0YQuQv2SpJkz75M3U0CSQVwxIwP0MP1psW2YjgbLny4wKggLzgeDFp3sac9zQU00sxSb3hBDOZl5YpS_TTk1ZpQmnL7Hh1sjejLTB3NRKHKhkNcdT1gf-PMcKF5HWabpwOY7feSMIj9rDslhq-FCEPCJmxVyhLc9VctlSzxHRSl3oKFN0ZRT1Q5qho4pRTIUm_X6EdD4vEflucC5tb1Cr0G121DljAY3pjLooajjE4FvPxmijZLXoE2F2ku8tRcGQHY3TTCxK5Ngg250H0qpxUJKJAR6m5G1bizZIXlt3K94mWSlefEqGAYd7mio1DzBnIfa8j7dctFEHv7Hau4RlVFjfBUXeUzfo0lff-uFb04hgHUS4RljMvTKSwsrO1wWjFt_ITtKzEpcGM8SEWp-l8a35bdrmUJbV9UE1GZwGZqeaLf9vOzflash1M1NLMY5_1HSNqPRBQ6lKdEBw7NgqKPP9wn68FSXaPpmk7he6mfzjT8WL3QXR8op3oTwmsXxAaVzoFDo9kaQ19_Go1kHbhqmGKBQ3ijyoFU9c55g66ARl-6aavo3jE=w444-h937-no?authuser=1" />
  <caption>Calculator on Pixel emulator</caption>
</p>
