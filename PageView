import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

class MyHomePage extends StatefulWidget {
  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  PageController controller = PageController();
  final List<Widget> _list = <Widget>[
    Center(
        child: Pages(
      text: "Page One",
      color: Colors.teal,
    )),
    Center(
        child: Pages(
      text: "Page Two",
      color: Colors.red.shade100,
    )),
    Center(
        child: Pages(
      text: "Page Three",
      color: Colors.grey,
    )),
    Center(
        child: Pages(
      text: "Page Four",
      color: Colors.yellow.shade100,
    ))
  ];
  int _curr = 0;

  @override
  Widget build(BuildContext context) {
    return
      Scaffold(
      appBar: AppBar(
        centerTitle: true,
        title: const Text('PageView'),
        backgroundColor: Colors.lightBlueAccent,
      ),
      body: PageView(
        allowImplicitScrolling: true,
        children: _list,
        scrollDirection: Axis.vertical,
        // reverse: true,
        // physics: BouncingScrollPhysics(),
        controller: controller,
        onPageChanged: (num) {
          setState(() {
            _curr = num;
          });
        },
      ),
    );
  }
}

class Pages extends StatelessWidget {
  final text;
  final color;
  Pages({this.text, this.color});
  @override
  Widget build(BuildContext context) {
    return Container(
      color: color,
      child: Center(
        child: Column(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
              Text(
                text,
                textAlign: TextAlign.center,
                style: const TextStyle(
                    fontSize: 30,
                    fontWeight: FontWeight.w400),
              ),
            ]),
      ),
    );
  }
}
