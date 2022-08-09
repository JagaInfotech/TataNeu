

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

