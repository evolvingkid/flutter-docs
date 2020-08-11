# Stateless and Statefull

### Stateless

In stateless widgets we cannot change the state during the runtime of the applications. It means widgets cannot be redrawn when application is running.

```text
// This is demo code
// this is written in stateless
String headingTxt = 'This is title';

Column(children:[
 Text(headingTxt),
 FlatButton(onpressed:(){
 headingTxt = 'This is secound title';
 },
  child: Text('Change Text')),
])

```

\(For Beginners\)

In the above code when the button is press it will trigger headingTxt = 'This is secound title'. but the edit will not happen on the view because it is stateless widgets. The edit will not be redrawn to the UI of the application. 







