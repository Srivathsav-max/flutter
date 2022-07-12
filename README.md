# Flutter Testing 

### *Note - Using **Pubspec** VS code Extension for adding different packages in flutter yaml File

In general we are two types of testing
* Manual - Which in person tests every functionality and performance of an app 
* Automated - Here we instructs the software by a program which run in an automated way which like UnitTests Without a human prescence.

Flutter in which we can bulid websites or apps for different platforms using a single codebase.And With this we are having Testing in the same codebase which we can add all code for our testing

Flutter Comes under an automated testing platform Which It consists in three types.
* Unit Testing
* Widget Testing
* Integration Testing

> As per my learning i really preffer the following testing preferences - Unit Testing -> Integration Testing -> Widget Testing 

> Below Table Shows the Total Efficency and performance of each Testing Methods.

|                   | Unit          | Widget        | Integration |
| -------------     | ------------- | ------------- | ------------- |
| Confidence        | Low           | Higher        | Highest  |
| Maintenance cost  | Low           | Higher        | Highest  |
| Dependencies      | Few           | More          | Most  |
| Execution speed   | Quick         | Quick         | Slow  |

### Unit Testing
* These are Useful for evaluating the behaviour of an single method, class or a function.
* Here the `test package` provides the core framework for writing unit tests, and the `flutter_test` package provides additional utilities for testing widgets. 
> Firstly Initalizing the test packages in our flutter as follows -
* Go Into pubspec.yaml file and add configuration as in `dependencies`.
```
dependencies:
  flutter:
    sdk: flutter
  provider: ^5.0.0            # new Testing provider package 
```
* And also add test packages in  `dev_dependencies` as follows
```
dev_dependencies:
  flutter_test:
    sdk: flutter
  integration_test:           # new for performing integration testing.
    sdk: flutter              # new
  test: ^1.14.4               # new for other packages for unit or widget testing.
```
### Widget Testing

```
testWidgets('Add and remove a todo', (tester) async {
   // Testing Using Function name
  await tester.pumpWidget(const "FunctionName"());

  // Enter 'hi' into the TextField.
  await tester.enterText(find.byType(TextField), 'hi');
});
```



