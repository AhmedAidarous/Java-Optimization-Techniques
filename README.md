# Java-Optimization-Techniques
Java is one of the most popular programming languages out there, and most of the time while writing a Java program, the programmer can easilt make simple mistakes that are harmless at first for small applications.
However as the application scales up, the performance of the Java application becomes slower.


## Optimization Levels
There are two levels of optimization in Java, these are<br>
• **Low Level Optimization** <br>
• **High Level Optimization**

**High Level Optimization** is usually performed by the programmer, whereas **Low Level Optimization** is performed at the stage when the source code is compiled into Java bytecode instructions. The following is a diagram which showcases **Low Level Optimization**.

![image](https://user-images.githubusercontent.com/47617364/129666817-2a7a6bed-d49e-43ad-9296-df0874f90d33.png)

The following is a list of Low Level Optimization techniques:
## Constant Folding
This an optimization technique that eliminates expressions a value that can already be determined before code execution. Typically these calculations only reference constant values or expressions that reference variables whose values are constant. <br>
The following is an example that shows this:

    int x = 5 + 1;
    int x = 6;

<br>
The value of variable number will always be 6, so the compiler recognizes it's a constant, and will replace the value of the variable with the constant 6.

## Constant Propogation
This is the process of substituting the values of known constants in expressions. Constant propagation eliminates cases in which values are copied form one variable to another, in order to simplify assign their value to another value. <br>
The following shows this:<br>

    int x = 14;
    int y = 7 - 14 / 2;
    int z = y * (28 / 14 + 2) - 14;

<br> 
Code propagation would substitute the variables x and y with the constant values assigned to them.
<br>

    int x = 14;
    int y = 7 - x / 2;
    int z = y * (28 / x + 2) - x;
<br>

## Useless Expression Elimination 
Whenever there are expressions which aren't used in the program, the following example shows this:
<br>
      
      int num = 1;
      int num2 = 2;
      System.out.print(num);

As you can see, **num2** isn't used in the code above, therefore the compiler would remove this expression.
<br>

## Copy Propogation 
After the assignment of one variable to another, a reference to one variable maybe replaced with the value of the other variable when they are equal.<br>Copy propogation looks as follows:<br>

    int x = y;
    System.Out.print(y);
<br> 
The example given above, the reference y would be removed, since the variable x contains the value now.

<br>

## Reduce Mathematical Strength 
This optimization technique is done by replacing the mathematical expression which requires longer item for computation with expressions which require less time for computing the same thing.

## Dead Code Elimination 
This is an optimization that removes code which does not affect the program results. 

## Code Hoisting 
An optimization technique whihc computes the heavy expressions as early as possible, to help reduce the size of code. Moreover this is done when the compiler **moves code from inside a loop to outside of the loop**, if the code is not dependent on being inside of the loop.








