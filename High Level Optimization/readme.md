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


      
