# 첫 번째 장 HTML

먼저, **HTML** 은 **H**yper **T**ext **M**arkup **L**anguage 라는 약자를 가진 웹 페이지를 위한 마크업 언어입니다. 즉, 웹 브라우저가 콘텐츠를 표현하는 방법을 나타냅니다. 

**HTML**은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것 뿐만 아니라 링크 등과 같은 항목으로 하나의 **문서**를 만들 수 있습니다.

더 나아가기 전에 맛보기를 한번 해볼까요? 준비물은 Atom 이나 VScode 등의 에디터가 필요합니다!

atom 다운로드 : https://atom.io/

VScode 다운로드 : https://code.visualstudio.com/



1. 먼저 바탕화면이나 편한 곳에 폴더를 하나 생성하세요.

![HTML_1](/Users/jieunpark/Desktop/Study-webfront/image/HTML_1.png)

2. 에디터에서 좀 전에 생성한 폴더를 열고, study.html 이라는 파일을 하나 생성하세요!

![HTML_2](/Users/jieunpark/Desktop/Study-webfront/image/HTML_2.png)

3. 그리고, 연 파일에 다음과 같은 코드를 작성해보세요

   ```html
   <p>Hello World!</p>
   ```

   ​

4. 그 다음, 아까 생성한 폴더로 들어가서 study.html 이라는 파일을 더블클릭 해보세요!

![HTML_3](/Users/jieunpark/Desktop/Study-webfront/image/HTML_3.png)

다음과 같은 문구가 출력이 되나요?

이와 같이 HTML 을 이용해서 인터넷 문서들을 작성 할 수 있습니다. 

## 태그 요소 분석

![](https://mdn.mozillademos.org/files/9347/grumpy-cat-small.png)



1. 여는 태그(Opening Tag) : 이곳은 엘리먼트의 이름으로 구성됩니다. 열고 닫는 <> 꺽쇠괄호로 감싸집니다. 이곳은 엘리먼트를 시작하는 곳, 또는 효과를 시작하는 곳을 나타냅니다.
2. 닫는 태그 (closing tag): 이것은 여는 태그와 같지만, 엘리먼트의 이름 앞에 슬래시가 포함된다는 점이 다릅니다. 이것은 엘리먼트의 끝을 나타냅니다 — 이 예제에서는 문단이 끝나는 위치를 나타냅니다.
3. 내용 (content): 이것은 엘리먼트의 컨텐트이고, 이 예제에서는 그냥 문자입니다.
4. 요소 (element): 여는 태그 + 닫는 태그 + 컨텐트는 엘리먼트와 같습니다.



먼저 우리가 이전에 사용한 <p> 태그는 단락(paragraph)을 표시할 때 사용하는 태그입니다. 

이외에도 아래와 같이 다양한 태그들이 있습니다.

|   태그   |                   사용법                    |                  태그 설명                   |
| :----: | :--------------------------------------: | :--------------------------------------: |
|   a    | `<a href = "http://www.naver.com">네이버 </a>` | 웹 문서에 다른 웹 문서나 인터넷 상의 다른 자원으로 연결되는 하이퍼링크(hyperlink)를 넣기 위해 사용합니다. |
| strong |          `<strong>강조!</strong>`          |           텍스트를 강조하기 위해서 사용합니다.           |
|  img   |   `<img src = "/images/hello.jpg" />`    |           이미지를 출력하기 위해 사용합니다.            |
| ul, li |  `<ul><li>리스트1</li><li>리스트2</li></ul>`   |    목록을 나타내는 태그로, ul 태그는 순서가 없는 태그입니다.    |
| ol, li |  `<ol><li>리스트1</li><li>리스트2</li></ol>`   |    목록을 나타내는 태그로, ol 태그는 순서가 있는태그입니다.     |
| input  |        `<input type = "text" />`         |      input 태그는 무언가를 입력할 수 있는 태그입니다.      |
|  div   |              `<div></div>`               | 레이아웃을 구성할 때 쓸 수 있는 태그입니다. 그 위에 css 라는 것을 입히면 모양이 드러나게 됩니다. |



## HTML 문서 분석

이제 지금까지 알아보았던 태그들을 이용해서 어떻게 html 페이지로 구성되었는지 알아봅시다. 

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>My test page</title>
	</head>
	<body>
    	<img src="images/firefox-icon.png" alt="My test image">
 	</body>
</html>
```

- !DOCTYPE html : html의 버전을 나타냅니다. 요즘에는 올바르게 동작하게 하기 위한 역사적인 유물이라고 합니다.
- `<html></html>` : 이 엘리먼트는 전체 페이지의 모든 컨텐츠를 감싸고, 루트 엘리먼트로 알려져 있습니다.
- `<head></head>` : 이 곳은 머리 부분으로, 키워드와 검색 결과로 보여지길 원하는 페이지 설명, 컨텐트를 꾸미기 위한 CSS, 문자 집합, 선언 등과 같은 것들을 포함합니다.
- `<body></body>` : 이것은 페이지에 방문한 모든 웹 사용자들에게 보여주길 원하는 모든 컨텐트를 포함합니다. 문자, 이미지, 비디오, 게임, 실행 가능한 음성, 또는 그 외 등등.
- `<meta charset="utf-8">` : 이 태그는 여러분이 사용해야 하는 문서들을 국제표준인 utf-8 로 인코딩합니다. 
- `<title></title>` : 페이지가 불려질 때, 브라우저 탭에 나타나는 제목을 설정하고, 북마크 할 때 페이지를 설명하기 위해 사용됩니다 