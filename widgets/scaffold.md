# Scaffold

Scaffold is one of the widgets that comes with material app widget. 

It provide us with basic material design that we can use in flutter app.

Property of scaffold

```text
Key
appBar
body
floatingActionButton
floatingActionButtonLocation
floatingActionButtonAnimator
persistentFooterButtons
drawer
endDrawer
bottomNavigationBar
bottomSheet
backgroundColor
resizeToAvoidBottomPadding // this is set default as true
primary // this is set default as true
```

example of simple scaffold screen

```dart
class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: SafeArea(
          child: Column(
        children: <Widget>[
         
        ],
      )),
    );
  }
}
```



