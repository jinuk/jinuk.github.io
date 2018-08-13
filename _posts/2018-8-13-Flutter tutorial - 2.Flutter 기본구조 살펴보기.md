## 1.Hello Flutter!  
우리는 앞서 처음으로 Flutter 프로젝트를 생성했습니다.  
프로젝트에서 실제 앱의 코드는 `lib/main.dart`에 위치해 있습니다.  
그리고 `pubspec.yaml`에서는 의존성 관리를 담당합니다. 추후에 다뤄보겠습니다.  
일단 `lib/main.dart`안의 전체 코드를 밑의 코드로 바꾸어 줍니다.  
```dart
import 'package:flutter/material.dart';

void main()=>runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home:
      Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: Text('Hello Flutter!'),
        ),
      ),
    );
  }
}
```
코드를 바꾸어 준 후 저장이나 hot reload 버튼을 클릭하면 앱의 화면이 다음과 같이 표시됩니다.  
![image2](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/2-1.png?raw=true "aa")  
##2. 기본 구조
그럼 코드를 하나하나 살펴 보겠습니다.
    
`import 'package:flutter/material.dart';`  
맨 첫번째 위의 코드는 `flutter/material`패키지를 사용하겠다는 것인데 거의 필수적으로 import 시켜놔야 하는 패키지 입니다.  
`void main()=>runApp(MyApp());`  
Flutter는 시작할때 `main.dart`안의 `main()`함수를 찾아서 실행시킵니다.
`main()`함수는 `runApp`함수를 실행시켜서 앱을 실행시킵니다.  
javascript es6를 사용해 보신 분들은 알겠지만 `=>` 화살표 함수식을 풀어서 쓰면 아래와 의미가 같습니다.  
```dart
void main(){
  runApp(MyApp()); 
}
``` 
  
  
  
```dart
class MyApp extends StatelessWidget {
  //....
}
```  
Flutter에서 앱 화면을 포함한 화면에 표시 될 수 있는 거의 모든 것들은 위젯 입니다.  
MyApp 클래스의 의미는 State가 없는 위젯을 상속하는 클래스라는 의미인데 이 예제에서는 앱 전체의 화면을 의미합니다. State는 추후에 다루어 보겠습니다.    
MyApp 클래스는 `runApp`함수 안에서 객체로 생성되는데 dart에서는 객체를 생성할때 `new` 키워드가 생략 가능합니다.  
`void main()=>runApp(MyApp());` = `void main()=>runApp(new MyApp());`  
  

```dart
@override
Widget build(BuildContext context) {
  return MaterialApp(
      //....
  )
}
```  
`MyApp`클래스가 상속하고 있는 `StatelessWidget`클래스 안에 `build`함수를 오버라이드 한 함수입니다.  
반환형이 `Widget`인 이 함수는 이 클래스가 나타내는 위젯을 반환합니다.  
이 예제에서 `MyApp` 클래스 안의 `build` 함수는 앱 전체의 화면을 반환합니다.  
`MaterialApp`은 Material Design 을 따르는 앱에 일반적으로 필요한 여러 위젯을 래핑 해 놓은 위젯 입니다.  
  
```dart
title: 'Welcome to Flutter',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Welcome to Flutter'),
        ),
        body: Center(
          child: Text('Hello Flutter!'),
        ),
      ),
```  
위의 내용은 `MeterialApp` 위젯을 구성하는 코드 입니다.  
`title` 속성은 안드로이드의 '최근 앱' 탭의 앱 상단 텍스트, IOS의 'App Switcher' 에서 상단 텍스트를 정의합니다.  
`home` 속성은 앱 기본 화면의 위젯을 정의합니다. `home` 속성에 `Scaffold`는 Material 디자인의 기본 화면 구조를 구현하는 클래스 입니다.  
그 안에는 현재 `appBar`와 `body`가 있는데 appBar는 현재 화면에서 상단에 위치한 하늘색 부분이고 body는 그 밑의 부분 입니다.  
각각의 부분에는 'Welcome to Flutter'라는 텍스트를 가진 위젯과 'Hello Flutter!'라는 텍스트를 가운데 정렬한 위젯이 있습니다.  
##3. Scaffold/MaterialApp 이 없다면?(안 봐도 무방합니다.)
저는 이 구조를 처음 봤을 때, '굳이 써야 하나?'라는 생각을 했습니다.  
그래서 한번 빼봤습니다.  
일단 Scaffold 없이 앱을 만들어 보겠습니다.  
```dart 
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Welcome to Flutter',
      home: Center(
        child: Text('Hello Flutter!'),
      ),
    );
  }
}
```  
![image2](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/2-2.jpg?raw=true "aa")  
일단 Scaffold가 없으니 appBar를 사용 할 수 없습니다.  
위의 화면을 통해 Scaffold가 텍스트의 색, 크기, 밑줄 등을 정해주고 앱의 바탕 화면을 잡아 주고 있다는 것을 알 수 있습니다.  
  
이번에는 MaterialApp도 없에보겠습니다.  
```dart 
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Center(
          child: Text(
            "Hello Flutter!",
            textDirection: TextDirection.ltr,
          ),
        );
  }
}
```  
![image2](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/2-3.jpg?raw=true "aa")    
여기서 보면 글씨가 또 달라졌습니다. 그 전의 예제에서의 글씨는 MaterialApp클래스에서 정의 하고 있었다는 것을 알수 있습니다.  
그리고 추가된 속성 `textDirection: TextDirection.ltr`을 안넣고 빌드하면 오류가 발생합니다.  
이것도 이전에는 MaterialApp에서 정의 하고 있었다는 것을 알수 있습니다.  
  
  하나하나 정의 하면서 하면 앱을 만들 수는 있겠지만 정신건강을 위해 MeterialApp과 Scaffold를 사용하는 것을 권장합니다.