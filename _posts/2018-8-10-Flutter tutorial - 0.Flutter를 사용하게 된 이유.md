##0. Flutter.   
Flutter에 대한 전반적인 설명은  
[flutter는 왜 혁명적인가 - dan_kim님 번역](https://medium.com/@dan_kim/번역-flutter는-왜-혁명적인가-967c1dfcc5a9)  
위의 링크의 글보다 더 잘 설명할 자신이 없어서 위의 링크를 읽어보시고 오시는 것을 추천드립니다.  
이 글에서는 저의 경험을 바탕으로 **주관적으로** Flutter를 사용하게 된 이유를 설명하겠습니다.  
  
##1. Flutter?  
![flutter vs rn](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/0-1.jpg?raw=true "bb")  
저는 원래 웹 개발을 하다가 앱 개발 업무를 맡게 되어서 cordova를 사용 한 후 react-native(RN)를 사용 하던 도중  
해외 RN 커뮤니티에서 RN과 Flutter를 비교하는 글을 보고 찾아보고 사용해 보게 되었습니다.  

  
##2. Flutter!  
###2-1. cordova  
![cordova](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/0-2.png?raw=true "bb")    
저는 원래 웹 개발을 하던 사람이라 앱 개발을 맡은 첫 프로젝트에 cordova를 통해 앱을 만들었습니다.  
cordova는 단점과 장점이 명확한 플랫폼이었습니다.  
가장 큰 장점은 html+css+js를 이용하여 앱을 빌드 하기 때문에 언어나 플랫폼에 대한 러닝 커브가 거의 없다시피 하다는 것 입니다.  
단점들 중 몇가지를 이야기 하자면 페이지를 이동할때마다 plugin을 사용하기 위해서는 새로운 페이지를 load할 때마다
 deviceready 이벤트를 기다려야 해서 페이지 이동 시간이 늦어지게 되어서 framework7을 사용하여 single page app 형식으로 만들었지만 camera preview 등의 plugin과의 
충돌등의 어려움이 있었고, 성능이 뒤쳐져서 고생을 했습니다.  
###2-2. React-Native  
![react-native](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/0-3.png?raw=true "bb")     
cordova를 이용해서 앱을 출시 후에는 RN을 이용해서 앱을 만들어 보자는 생각이 들었습니다.  
당시에(물론 지금도) RN이 힙(?)하기도 했고, facebook과 airbnb가 실제로 사용한다고 하여서 앱을 개발했습니다.  
장점 중 몇가지를 이용하자면 공식 Document가 정말 잘 되어있고, 리엑트를 알고 있다면 러닝커브가 크지 않습니다.  
그리고 live reload, hot reload가 인상깊었습니다. 그 외에도 풍부한 UI패키지, 넓은 커뮤니티 풀, 풍부한 plugin 등등이 있었습니다.  
그러나 앱이 커지고 로직이 복잡해지면 bridge의 병목현상에 따른 성능 저하, 같은 코드를 작성해도 android, ios의 UI가 다르게 작동하는 부분이 많았고, 그리고 android에서 UI의 미묘한 움직임(특히 ListViewㅜㅜ)이 단점으로 느껴졌습니다.  
###2-3. Flutter  
![flutter](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/0-4.png?raw=true "bb")    
그래서 이번에는 Flutter로 해보자는 생각이 들었습니다.  
dart라는 처음 들어본 언어를 해야 해서 처음에는 망설여 졌지만 예제 소스를 보다보니 Java와 Js를 섞어놓은 느낌? 이 들어서 크게 어렵진 않았습니다. 그리고 애니메이션도 60fps로 나오고, UI 작성시 react-native보다 ios, android의 차이점이 현저히 적었습니다. 전반적인 성능도 Flutter가 체감상으로도 더 좋게 느껴졌습니다.  
물론 document가 RN보다 조금 불친절하고 아직 사용자가 많지 않다보니 자료나 plugin이 많이 없고, react 스타일의 뷰를 알아야 사용하기 편하다는 점이 단점으로 남아 있지만 시간이 지나면 해결 될 것이라고 생각하기 때문에 앞으로는 주로 Flutter를 사용해서 프로젝트를 진행하기로 마음먹었습니다.  
여러 여건에 따라 사용하게 될 플랫폼이 바뀔수도 있겠지만 현재까지는 만족하며 사용하고 있습니다