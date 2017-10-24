# 두 번째 장 CSS
이전 강좌 (HTML이란?) 를 통해 HTML에 대해 간단하게 알아보았습니다. HTML을 간단히 요약하자면 문서의 구조를 작성하는 언어라고 할 수 있습니다. 하지만 HTML 만으로는 문서를 예쁘게 만드는 것에 한계가 있습니다. 그래서 이번에는 HTML로 만들어진 문서를 꾸며줄 수 있는 CSS에 대해서 알아보도록 하겠습니다.

## CSS 란?
CSS 는 Cascading Style Sheets의 약자로 HTML 등의 마크업 언어가 보여지는 방법을 기술하는 언어입니다.
HTML이 웹페이지의 몸통을 담당한다고 한다면 css는 옷이나 화장처럼 꾸며주는 역할을 한다고 할 수 있죠.

이전장을 통해 HTML의 개본적인 태그들을 숙지하셨을 것 입니다. 아래는 HTML의 기본 태그들을 꾸며주는 CSS의 예제 입니다.


```css
body {
    background-color: lightblue;
}

h1 {
    color: white;
    text-align: center;
}

p {
    font-family: verdana;
    font-size: 20px;
}
```

결과 : https://www.w3schools.com/css/tryit.asp?filename=trycss_default

이처럼 CSS는 HTML로 작성된 문서를 한층 더 꾸며주는 언어 입니다.



## CSS 기초 문법
![](https://www.w3schools.com/css/selector.gif)

CSS의 기본적인 문법은 위와 같습니다. 선택자로 HTML의 태그를 선택하고 중괄호 안에 꾸미고 싶은 속성이름과 속성으로 구성되어 있습니다. 위의 사진에서는 h1 태그를 선택하여 color를 파란색(blue)로, font 크기를 12px로 만들어 주게 됩니다.

### 태그 선택자
스타일 속성을 부여하기 위해서는 어떤 태그에 속성을 부여할지 알려주어야 합니다. 따라서 선택자라는 개념을 사용하는데요, 아래 예제를 통해 어떻게 태그를 선택하고 스타일 속성을 부여하는지 알아보도록 하겠습니다.


html 코드
```HTML
<html>
  <body>
    <div>
      검정색 배경
    </div>
  </body>
</html>
```
CSS 코드
```CSS
div{
  background-color: black;
}
```

위와 같이 div를 통해 div HTML 태그를 선택하고 뒤의 중괄호 안에 스타일 속성의 이름과 속성을 적어 원하는 속성을 원하는 태그에 적용할 수 있습니다.

### 클래스 선택자
div, span, p 등의 HTML 기본적인 태그들에만 스타일 속성을 부여할 수 있다면, CSS로 표현할 수 있는 범위가 매우 한정적일 것 입니다. 하지만 CSS에서는 클래스라는 개념을 이용하여 같은 div 태그이더라도 다른 스타일 속성을 부여할 수 있습니다.


html 코드
```HTML
<html>
  <body>
    <div class="background-black">
      검정색 배경
    </div>
    <div class="background-white">
      하얀색 배경
    </div>
  </body>
</html>
```
css 코드
```css
.background-black{
  background-color: black;
}
.background-white{
  background-color: white;
}
```

위의 예제를 살펴보면 html에는 class라는 것이 생겼고 css의 선택자에는 .이 붙었다는 것을 알 수 있습니다. 이는 CSS의 클래스라는 개념 입니다. div, p 등의 html 태그만 가지고 style 속성을 주게 되면 세부적이고 다양한 디자인을 할 수 없을 것 입니다.

그래서 class라는 개념을 통해 같은 div 태그더라도 다른 스타일 속성을 부여할 수 있습니다. 위의 예제처럼 클래스를 사용하는 방법은 태그에 class="클래스 이름" 을 적고 css에서는 .클래스 이름 { 속성이름: 속성 } 이와 같이 선택자에 .을 붙이면 됩니다.

클래스의 이름에는 알파벳, 숫자 언더스코어(_), - 등을 사용할 수 있습니다.


### ID 선택자
태그와 클래스 외에도 CSS 속성을 부여할 수 있는 방법이 있습니다. 바로 아이디를 이용하는 것 인데요, HTML 태그에 id 속성을 주고 이를 선택하여 사용할 수 있습니다.

```HTML
<html>
  <body>
    <div id="black">
      검정색 배경
    </div>
  </body>
</html>
```
CSS 코드
```CSS
#black{
  background-color: black;
}
```

위와 같이 div 태그에 id="black"을 적어 black이라는 아이디를 가진 div 태그를 만들고, #black으로 black이라는 아이디를 가진 태그를 선택하여 스타일 속성을 적용하게 됩니다.

아이디 선택자는 보통 문서에 단일로 존재하는 element에만 사용하는 것을 권장합니다.


## CSS의 속성과 값들
