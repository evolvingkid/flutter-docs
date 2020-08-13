# Material App

The material app gives us access to all the material design components that we can you on the app.

[https://material.io/develop/flutter](https://material.io/develop/flutter)

Yes it is true we can make widgets without the material app like text.

```dart
// using column wigets without material app bar

void main() {
  runApp(Column(
    children: [],
  ));
}

```

But if you try to use AppBar or CricleAvatar widgets then it will not work. These widgets need Material App to work.

Material App also help us to navigate around the pages too. We will look into it more on material section.



example for material app

```dart
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
        visualDensity: VisualDensity.adaptivePlatformDensity,
      ),
      home: HomePage(),
    );
  }
}
```



