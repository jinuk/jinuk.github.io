## 0.android, ios 개발 환경 세팅
Flutter는 android, ios 환경에서 동작하는 앱 임으로, android와 ios중 빌드할 환경 세팅을 우선적으로 진행합니다.  
  
## 1. Flutter sdk 다운로드
https://flutter.io/get-started/install/ 에 접속합니다.  
저의 개발 환경은 MAC OS, IDE는 intellij를 사용하겠습니다.  
해당 페이지에서 자신의 OS에 맞는 페이지를 들어간 후 SDK 파일을 다운받습니다.  
SDK 파일을 적절한 위치에 위치시키시면 됩니다.  
그 후 .bash_profile파일에  
export PATH=${PATH}:/flutter sdk 경로/flutter/bin  
텍스트를 추가해 줍니다.

## 2. intellij Flutter 플러그인 설치
intellij에서 Flutter를 편하게 구동하기 위해 Flutter 플러그인을 설치하겠습니다.  
일단 intellij를 실행 하시고 [Preference]->[Plugin] 화면에서 flutter를 입력합니다.  
![플러그인 검색 이미지](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-1.png?raw=true "aa")
그 후 오른쪽에서 Install을 클릭합니다(저는 이미 설치되어 있어서 Uninstall이 표시됩니다.)  

## 3. 프로젝트 생성
이제 준비는 끝났고 프로젝트를 생성해 보겠습니다.  
[Create New Project] -> [Flutter]  
![프로젝트 생성](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-2.png?raw=true "bb")  
우측의 Flutter SDK path에는 다운로드 받았던 sdk파일의 경로를 입력합니다.(경로/flutter 까지만)  
이제 Next를 누르고 프로젝트 이름 등을 입력하고 Finish를 클릭합니다.  
  
![프로젝트 생성2](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-3.png?raw=true "cc")  
  
## 4. 구동하기
![프로젝트 첫화면](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-4.png?raw=true "cc")  
2018년 8월 11일 intellij 기준으로 Flutter 프로젝트를 생성하면 소스코드 창 상단에  
**Dart SDK is not configured** 라는 메세지가 뜨게 된다.  
이를 수정하기 위해서는 [Preference]->[Languages & Frameworks]->[Flutter]에서 Flutter SDK path
를 다시 설정 해 주면 됩니다.  
![프로젝트 첫화면](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-5.png?raw=true "cc")  
  
이제 구동을 하기 위해 디바이스를 연결하거나 시뮬레이터를 실행 한 후 Run 버튼을 클릭하면 기본 앱이 실행됩니다.  
![시뮬레이터](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-6.png?raw=true "cc")  
  
![첫화면](https://www.github.com/jinuk/jinuk.github.io/blob/master/_posts/post-images/1-7.png?raw=true "cc")
