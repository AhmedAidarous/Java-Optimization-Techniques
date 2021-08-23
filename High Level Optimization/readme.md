# High Level Optimization 
The following is a list of high level optimization techniques which are done by the user to enhance programming efficency, and execution speed.

## Use Primitive Strings Rather Than String Objects
The concensus here is whenever your creating strings, you should always use the primitive type, which would store the string in a **constant 
string pool**, rather than in the **heap memory**.
<br> 
So instead of creating strings this way:

      String str = new String("String");
      String str1 = new String();
      String str2 = new String(str1);

You would want to instansiate them this way:

      String str = "String";
      String str1 = "";
      String str2 = str1;


## Use StringBuilder To Concatenate Strings
When performing string concactenation, it's recommended to use the data structure **StringBuilder** rather than primitives, this is because **StringBuilders**
are not thread safe, and offer faster performance. 
<br>
So instead of concactenating strings like this:

      String string = "abc";
      string = "Ahmed" +  "Me";
      
You would concactenate them like this:

      StringBuilder string = new StringBuilder();
      string.append("Ahmed");
      string.append("Me");
      
      

## Be considerate on the collections data structure you use
In computer science, different data structures offer a variety of benefits, each data structure performs operations 
differently, therefore can perform them at different time. 
<br>
The following is a list of the basic collections that can be used in Java with their and time complexities: <br>
• Lists<br>
• Stacks<br>
• Queues<br>
• Vectors<br>
• Linked Lists<br>
• Binary Trees<br>
• Hash Sets<br>
• Tree Sets<br>
• Hash Maps<br>
• Tree Maps<br>
<br>

![image](https://user-images.githubusercontent.com/47617364/130433182-a22c9f74-cd6a-43e1-a572-63c53f6eaba2.png)



## Using ArrayLists Instead of LinkedLists
It's not going to make a huge change, however using ArrayLists is found to have a slightly better performance advantage compared to using Linked Lists.

## Use Short-Circuit Boolean Operators instead of Binary Operators
Whenever you are evaluating **IF statements** it's always best to use short-circuit operators i.e (&& or ||) instead of the binary operator equivalents (& or |). This is because short circuit operators only evaluate the left hand side of the boolean expression first, and if it's true, they don't need to look at the right hand side in most cases. Where as using binary operators would **always evaluate both sides regardless if one side is true.** Therefore using Short-Circuit operators yields more optimal results.
<br>i.e
     
      if (x == 0 || y == 0)
            System.out.println("Output");
      
The above selection statement is more optimal than the one below, and also is faster.

      if (x == 0 | y == 0)
            System.out.println("Output");

      


## Avoid Using Multiple IF ELSE statements
Try to miminize the use of multiple IF statements, if you can, mainly try to use IF, and then allow the program to continue execution as the Else part of the statement.


## Use == More Than .equals()
Using the operator == has a higher performance than using .equals() method. This is because .equals() compares objects stored in the heap, rather than == which compares objects stored in the stack.


## Minimize The Use of .toString()
It's tempting to use this method a lot! However too much of converting data types to strings would inevitably slow down the performance of the program, so try to find ways to reduce using this method, and transition to using other means such as primitive **TypeCasting**.

## Use ForEach() loops instead of index for loops
The for-each loop, introduced in release 1.5, gets rid of the clutter and the opportunity for error by hiding the iterator or index variable completely.

ie. 

      for (Element e : elements) {
            doSomething(e);
        }

When you see the colon (:), read it as “in.” Thus, the loop above reads as “for each element e in elements.” Note that there is no performance penalty for using the for-each loop, even for arrays. In fact, it may offer a slight performance advantage over an ordinary for loop in some circumstances, as it computes the limit of the array index only once.


## Use Primitive Types Whenever Possible
Primitive types are stored in what is known as the **Stack Memory**, whereas objects, that being both user defined and collections are mainly stored in the **Heap Memory**. Data access to the stack memory is way faster than heap memory, so it's always beneficial to use i.e int over Integer or double over Double.
i.e
    
      int x = 0;

Stores the refernece x in the stack, rather than

      Integer x = new Integer(0);
      
Which stores the reference x in the Heap memory.



## Avoid Recursion
In functional programming languages, recursion is often the most efficient way to iterate through data structures, or simply perform loop-based operations. However in the OOP paradigm, or mainly the imperative programming paradigm, recursion is very in-efficient. Therefore avoid using recursion and instead use while / for loops.

## Use String.isEmpty() instead of str.length == 0
Whenever you want to see if a string value is empty, it's prefered to use .isEmpty() method instead of str.length == "". The difference in performance is negilible, however its better ot use .isEmpty()


## When Handling large datasets use Maps
When you have large datasets, use HashMaps, since HashMaps have the following time complexities:
<br>
• Accessing : O(1)
<br>
• Insertion : O(1)
<br>
• Deletion :  O(1)
<br>
• Searching : O(1)

Which is faster than say using Lists (with Random Access feature), as lists have the following time complexities:
<br>
• Accessing : O(1)
<br>
• Insertion : O(n)
<br>
• Deletion :  O(n)
<br>
• Searching : O(n)

