# CodeForDartPad
https://dartpad.dev/?null_safety=true&id=e75b493dae1287757c5e1d77a0dc73f1
// Copyright (c) 2019, the Dart project authors.  Please see the AUTHORS file
// for details. All rights reserved. Use of this source code is governed by a
// BSD-style license that can be found in the LICENSE file.

import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
//     This is how we get to use material design elements
    return MaterialApp(
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    String name = "Dash";
    return Scaffold(
        body: Center(
            child: Container(
                color: const Color(0xFF181718),
                child: Column(children: [
                  Image.network(
                      "https://i.ibb.co/7NXstVH/97bf62e3c8e5a598b02d0aa541a40c54.png",
                      scale: 3),
                  RichText(
                    text: TextSpan(
                      style: DefaultTextStyle.of(context).style,
                      children: const <TextSpan>[
                        TextSpan(
                            text: 'D',
                            style: TextStyle(
                                color: Colors.blue,
                                decoration: TextDecoration.none,
                                fontWeight: FontWeight.w100)),
                        TextSpan(
                            text: 'ash',
                            style: TextStyle(
                                color: Colors.white,
                                decoration: TextDecoration.none,
                                fontWeight: FontWeight.w100)),
                      ],
                    ),
                  ),
                  Container(
                    padding: EdgeInsets.all(6),
                    child: TextFormField(
                        decoration: const InputDecoration(
                            prefixIcon: Icon(Icons.email, color: Colors.white),
                            fillColor: Color(0xFF7C88A7),
                            filled: true,
                            border: OutlineInputBorder(),
                            hintText: "Enter E-mail Address Here"),
                        style: TextStyle(color: Colors.white)),
                  ),
                  Container(
                    padding: EdgeInsets.all(6),
                    child: TextFormField(
                        obscureText: true,
                        decoration: const InputDecoration(
                            prefixIcon: Icon(Icons.lock, color: Colors.white),
                            fillColor: Color(0xFF7C88A7),
                            filled: true,
                            border: OutlineInputBorder(),
                            hintText: "Enter Password Here"),
                        style: TextStyle(color: Colors.white)),
                  ),
                  Row(children: [
                    Checkbox(
                        value: true,
                        onChanged: (value) {},
                        shape: CircleBorder(),
                        activeColor: Colors.white,
                        checkColor: Color(0xFF299DD0),
                        side: BorderSide(
                          color: Colors.white,
                        )),
                    Text(
                      "Keep me logged in.",
                      style: TextStyle(
                          color: Colors.white, height: 2, fontSize: 15),
                    ),
                  ]),
                  SizedBox(height: 20),
                  SizedBox(
                      height: 30,
                      width: 280,
                      child: TextButton(
                          style: ButtonStyle(
                              backgroundColor: MaterialStateProperty.all<Color>(
                                  Color(0xFF68A2F9))),
                          child: Text("LOGIN",
                              style:
                                  TextStyle(color: Colors.white, fontSize: 20)),
                          onPressed: () {})),
                  SizedBox(height: 10),
                  Row(children: [
                    Text("Forgot password?",
                        style: TextStyle(color: Colors.white)),
                    TextButton(onPressed: () {}, child: Text("Recover here"))
                  ], mainAxisAlignment: MainAxisAlignment.center),
                  SizedBox(height: 10),
                  Row(children: [
                    Text("Don't have an account?",
                        style: TextStyle(color: Colors.white)),
                    TextButton(onPressed: () {}, child: Text("Sign up here"))
                  ], mainAxisAlignment: MainAxisAlignment.center),
                ])
//         child: Container(
//             child: Image.network(
//                 "data:image/png;base64,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"),
//             color: const Color(0xFF181718))
                )));
  }
}
// [] - A list/array. A list is a collection of items
//           https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content#examples

/// Flutter code sample for TextEditingController

// This example creates a [TextField] with a [TextEditingController] whose
// change listener forces the entered text to be lower case and keeps the
// cursor at the end of the input.

// import 'package:flutter/material.dart';

// void main() => runApp(const MyApp());

// /// This is the main application widget.
// class MyApp extends StatelessWidget {
//   const MyApp({Key? key}) : super(key: key);

//   static const String _title = 'Flutter Code Sample';

//   @override
//   Widget build(BuildContext context) {
//     return const MaterialApp(
//       title: _title,
//       home: MyStatefulWidget(),
//     );
//   }
// }

// /// This is the stateful widget that the main application instantiates.
// class MyStatefulWidget extends StatefulWidget {
//   const MyStatefulWidget({Key? key}) : super(key: key);

//   @override
//   State<MyStatefulWidget> createState() => _MyStatefulWidgetState();
// }

// /// This is the private State class that goes with MyStatefulWidget.
// class _MyStatefulWidgetState extends State<MyStatefulWidget> {
//   final TextEditingController _controller = TextEditingController();

//   @override
//   void initState() {
//     super.initState();
//     _controller.addListener(() {
//       final String text = _controller.text.toLowerCase();
//       _controller.value = _controller.value.copyWith(
//         text: text,
//         selection:
//             TextSelection(baseOffset: text.length, extentOffset: text.length),
//         composing: TextRange.empty,
//       );
//     });
//   }

//   @override
//   void dispose() {
//     _controller.dispose();
//     super.dispose();
//   }

//   @override
//   Widget build(BuildContext context) {
//     return Scaffold(
//       body: Container(
//         alignment: Alignment.center,
//         padding: const EdgeInsets.all(6),
//         child: TextFormField(
//           controller: _controller,
//           decoration: const InputDecoration(border: OutlineInputBorder()),
//         ),
//       ),
//     );
//   }
// }
