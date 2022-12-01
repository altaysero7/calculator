import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        title: 'Flutter Demo',
        theme: ThemeData(
          primarySwatch: Colors.grey,
        ),
        home: HomePage());
  }
}

class HomePage extends StatefulWidget {
  @override
  _HomePageState createState() => _HomePageState();
}

class _HomePageState extends State<HomePage> {
  String display = "0";
  int num1 = 0;
  int num2 = 0;
  String operand = "";

  buttonClicked(String button) {
    if (button == "+" || button == "-") {
      num1 = int.parse(display);
      operand = button;
      display = "0";
    } else if (button == "=") {
      num2 = int.parse(display);
      if (operand == "+") {
        display = (num1 + num2).toString();
      }
      if (operand == "-") {
        display = (num1 - num2).toString();
      }
      num1 = 0;
      num2 = 0;
      operand = "";
    } else if (button == "AC") {
      display = "0";
      num1 = 0;
      num2 = 0;
      operand = "";
    } else {
      display = display + button;
    }

    print(display);

    setState(() {
      display = int.parse(display).toString();
    });
  }

  Widget buttons(String button) {
    return Expanded(
      child: GestureDetector(
          onTap: () => buttonClicked(button),
          child: CircleAvatar(
            radius: 40,
            backgroundColor: Colors.grey[400],
            child: Text(
              button,
              style: TextStyle(
                fontSize: 25.0,
                fontWeight: FontWeight.bold,
                color: Colors.black,
              ),
            ),
          )),
    );
  }

  Widget buttons2(String button) {
    return Expanded(
      child: GestureDetector(
          onTap: () => buttonClicked(button),
          child: CircleAvatar(
            radius: 50,
            backgroundColor: Colors.transparent,
            child: Text(
              button,
              style: TextStyle(
                fontSize: 25.0,
                fontWeight: FontWeight.bold,
                color: Colors.red,
              ),
            ),
          )),
    );
  }

  Widget buttons3(String button) {
    return Expanded(
      child: RaisedButton(
        onPressed: () => buttonClicked(button),
        padding: EdgeInsets.all(15),
        color: Colors.amber[400],
        shape: RoundedRectangleBorder(borderRadius: BorderRadius.circular(0)),
        child: Text(
          button,
          style: TextStyle(
            fontSize: 25.0,
            fontWeight: FontWeight.bold,
            color: Colors.black,
          ),
        ),
      ),
    );
  }

  Widget buttons4(String button) {
    return Expanded(
      child: GestureDetector(
          onTap: () => buttonClicked(button),
          child: CircleAvatar(
            radius: 40,
            backgroundColor: Colors.red[400],
            child: Text(
              button,
              style: TextStyle(
                fontSize: 25.0,
                fontWeight: FontWeight.bold,
                color: Colors.black,
              ),
            ),
          )),
    );
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
            title: Center(
          child: Text('Calculator'),
        )),
        body: Container(
            child: Column(
          children: <Widget>[
            Expanded(
              child: Divider(
                color: Colors.transparent,
              ),
            ),
            Container(
                height: 250.0,
                width: 800.0,
                decoration: ShapeDecoration(
                    color: Colors.white,
                    shape: RoundedRectangleBorder(
                        borderRadius: BorderRadius.circular(1.0),
                        side: BorderSide(width: 20, color: Colors.grey))),
                child: Center(
                    child: Text(display,
                        style: TextStyle(
                          fontSize: 48.0,
                          fontWeight: FontWeight.bold,
                        )))),
            Expanded(
              child: Divider(
                color: Colors.black,
                thickness: 5.0,
              ),
            ),
            Column(children: [
              Row(children: [
                buttons("7"),
                buttons("8"),
                buttons("9"),
                buttons4("AC"),
              ]),
              Divider(
                color: Colors.transparent,
              ),
              Row(children: [
                buttons("4"),
                buttons("5"),
                buttons("6"),
                buttons3("+"),
              ]),
              Divider(
                color: Colors.transparent,
              ),
              Row(children: [
                buttons("3"),
                buttons("2"),
                buttons("1"),
                buttons3("-"),
              ]),
              Divider(
                color: Colors.transparent,
              ),
              Row(children: [
                buttons2(""),
                buttons("0"),
                buttons2(""),
                buttons3("="),
              ])
            ]),
            Expanded(
              child: Divider(
                color: Colors.black,
                thickness: 5.0,
              ),
            ),
          ],
        )));
  }
}
