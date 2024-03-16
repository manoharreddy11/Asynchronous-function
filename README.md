import 'package:flutter/material.dart';

class MyWidget extends StatelessWidget {
  void fetchData() {
    print('Fetching data...');

    Future.delayed(Duration(seconds: 2), () {
      print('Data fetched successfully!');
    });

    print('Fetching data request initiated.');
  }

  @override
  Widget build(BuildContext context) {
    fetchData();

    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text('Asynchronous Function')),
        body: Center(child: Text('wait for output')),
      ),
    );
  }
}

void main() {
  runApp(MyWidget());
}
