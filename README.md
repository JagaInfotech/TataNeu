A.Descriptive Questions:
1. Can we nest the Scaffold widget? Why or Why not?

Solution : Yes,we can nest Scaffold widget because it is just like any other widget but the Scaffold was designed to be the single top level container for a MaterialApp and it's typically not necessary to nest scaffolds.


2. What are the different ways we can create a custom widget ?

Solution : we can create a custom widget by extending either a stateful or stateless widget.


3. How can I access platform(iOS or Android) specific code from Flutter?

Solution : We can access platform by through method channels. It is a named channel for communicating with platform plugins using asynchronous method calls. 

4. What is BuildContext? What is its importance?

 Solution : BuildContext is used to keep track of each widget and their postion in the tree


B.Coding Questions:

1.Refactor the code below so that the children will wrap to the next line when the display width is small for them to fit.

Solution : 

import 'package:flutter/material.dart';

class LongStringWidget extends StatelessWidget{

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Row(
          children: [
            Expanded(
                child: Wrap(
                  children: [
                    Chip(label: Text('I')),
                    Chip(label: Text('am')),
                    Chip(label: Text('looking')),
                    Chip(label: Text('for')),
                    Chip(label: Text('a')),
                    Chip(label: Text('job')),
                    Chip(label: Text('and')),
                    Chip(label: Text('i')),
                    Chip(label: Text('need')),
                    Chip(label: Text('a')),
                    Chip(label: Text('job')),
                  ],
                )
            )
          ],
        ),
      )
    );
  }
}
Screenshot : (https://user-images.githubusercontent.com/37834258/183552238-985dee40-8fa1-48d6-9c6e-4db8181612d9.png)

2. Identify the problem in the following code block and correct it.

String LongOperationMethod(){
  var counting = 0;
  for(var i = 1; i <=1000000000 ; i++){
    counting = i;
  }
  return '$counting! times I print the value';
}

Solution : This code snippet compiles without any error and output is as expected.
https://user-images.githubusercontent.com/37834258/183570570-34d174ff-a1b4-4b24-977c-3bfff56d6bd1.png


3.In the below code, list1 declared with var, list2 with final and list3 with const.
What is the difference between these lists? Will the last two lines compile?

var list1 = ['1','♥','Flutter'];
final list2 = list1;
list2[2] = 'Dart';
const list3 = list1;


Solution :

 list2[2] = 'Dart'; => This code snippet will compile and item at index 2 will be change to "dart" instead of "flutter". 
 const list3 = list1;  => This code snippet shows compile time error because list3 is supposed to be a constant value but since list1 is a variable it is throwing an error
 https://user-images.githubusercontent.com/37834258/183569453-e5b5f35b-9c0e-4ed4-87c6-97e401fb64dc.png

 

