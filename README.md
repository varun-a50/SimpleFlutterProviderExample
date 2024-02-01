This has only 3 pages to demonstrate simple provider use.

just imp part of code....

counter_model.dart
import 'package:flutter/material.dart';

class CounterModel extends ChangeNotifier {
  int _count = 0;
  int get count => _count;

  void increment() {
    _count++;
    notifyListeners();
  }
}
===========================================
home_page.dart
 return Consumer<CounterModel>(
        builder: (context, value, child) => Scaffold(
              appBar: AppBar(
==========================================

main.dart
void main() {
  runApp(
    ChangeNotifierProvider(
      create: (context) => CounterModel(),
      child: const MyApp(),
    ),
  );
}

