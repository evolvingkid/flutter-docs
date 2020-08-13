# Stateful widgets

Unlike stateless widgets the stateful widgets can be drawn multiple time. These widgets can change their state and can redraw the widgets or UI any number of time they want.

```dart
class HomePage extends StatefulWidget {

  @override
  _nameState createState() => _nameState();
}

class _nameState extends State<HomePage> {
  @override
  Widget build(BuildContext context) {
    return Container(
       child: child,
    );
  }
}
```

In this we write our widgets \(UI\) in the build method in nameState class which extends State&lt;HomePage&gt;. That doesn't mean you use nameState as widgets. Like stateless widgets Homepage is the widgets we use. In Homepage it override the createState method which return nameState which have our widgets \(UI\). 

Does this means all our changes on UI can be seen when application works? \(Will the UI will be rebuild when ever changes happen?\)

Actually No.

```text
String headingTxt = 'This is title';

Column(children:[
 Text(headingTxt),
 FlatButton(onpressed:(){
 headingTxt = 'This is secound title';
 },
  child: Text('Change Text')),
])

```

If we execute the above code in build method of the statefull widgets we still see like stateless widgets. Changes cannot be seen.

For changes to happen or Rebuild need to happen we need to use **setState**.

```text
setState(() { });
```

setState is only available for stateful widgets not stateless widgets. setState take a functions where we can write code needed to be updated.

```text
// asume code written inside build method of stateful widgets.

String headingTxt = 'This is title';

Column(children:[
 Text(headingTxt),
 FlatButton(onpressed:(){
 // This is where code is updated
 // so we use setstate and insert code update inside in it.
 setState(() { 
 headingTxt = 'This is secound title';
 });
 
 },
  child: Text('Change Text')),
])
```

When setstate is called in your code when automatically the build method will be called thus result in drawing of the UI again.

> Note That since setstate will rebuild the UI again this can cause performance issue. Since building of UI takes load on your devices.



