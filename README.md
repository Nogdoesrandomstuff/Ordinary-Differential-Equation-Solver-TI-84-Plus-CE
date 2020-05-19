# Ordinary-Differential-Equation-Solver-TI-84-Plus-CE
A quick run through of how it works/ how to run and use the program.
1. User determines the set of first order differential equations corresponding to the given differential equation.
ex: y''+ y' + 3y + x = 5 => y' = Q(x); Q'(x) = -Q(x) - 3y - x +5
2. User writes the functions in the function editor (y= button) in order using PQRSTUVWYZ. P corresponds with y, Q corresponds with y', etc. (As there are only 10 y vars, the program can only handle up to 10th order differential equations). X input remains the same as usual. 
(You may want to disable output of each function for easier reading of the graph later)
Write in the form of "y(n) = (dy(n)/dx)." For example, for y' = Q(x), input y1 = Q. 
For Q'(x) = -Q(x) - 3y - x +5, input y2 = -Q - 3P - X + 5.
3. Run the program 
4. Set number of function outputs to the number of functions you wrote in step 2
5. Input the span of the approximation. This is the minimum and maximum x value that the ODE will be approximated at, ex: {0,10}
6. Input initial values. Ex: Write y(0) = 0, y'(0) = 3 as {0,3}
7. Input change in x. How small this is will increase accuracy of the approximation.
8. The function will run for a while depending on the size of the span and the smallness of the change in x. This is an issue I've tried to work on, but this may just be due to the limitations of the ti-84. If you look at the code and see something causing a large performance drop, PLEASE let me know.
9. The function will store the y values for each x values in the lists FN1 -> FN10 and will store the x values in XVALS. It also shows these values in a scatter plot. Just hit the Graph button. 


The ODE4L file is the light version of the file. This file only allows for 3rd order differential equation solving but also increases execution speed by about 15% (Not heavily tested). 3rd order differential equations should be enough for most engineering applications. 
