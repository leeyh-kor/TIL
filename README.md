# TIL
오늘(2020.10.16)부터 매일 매일 배운고 공부한것을 기록하도록 하겠읍니다.

오늘은 API 불러와서 LISTVIEW 실습하다가 하루가 끝나버렸읍니다.... 결국 실패 했는데,

아따 어떻게 해야 되는겨? 오늘의 질문사항 

1. 그동안 써왔던 첫 글자가 대문자인 HTML 이것은 무엇인가요?

    that is component !!!! 이것은 html을 반환하는 함수입네다 react는 html도 지원하지만 react-native 는 html을 지원하지 않기때문에 재사용 가능한 컴포넌트와 스타일 옵션을 만들어 놓는것은 매우 좋은 습관이야.

    <Home/>와 같이 이렇게 쓰는 문법을 JSX라고 하는데 이것은 자바스크립트의 모든 기능을 지원하는 확장 버젼이야

    React를 사용할때 무조건 JSX를 사용해야 하는것은 아니지만, JSX는 REACT의 장점을 극대화 시켜주기 때문에 꼭 사용하는 것이 좋아.

```jsx
import React from 'react';
//import Home from './home.js' 컴포넌트로 쓸 함수의 첫글자는 무조건 대문자여야한다. 이처럼 임포트 할 수도 있고 직접 전언도 가능!

function Home (){
return(<h1> Hello<h1/>)
}
<Home/> #이렇게 home.js를 불러올 수 잇슴 이것이 바로 리액트의 장점이자 모든것인 component

```

다음은 하위 컴포넌트에 값을 보내는 방법을 알아보도록 할게.

우선 코드는 다음과 같은 형태로 작성할 수 있어

```jsx
import React from 'react';
function Home (name){
return(<h1> {name}<h1/>)
}

function App(){
return (<Home name = "kimchi"/>) }

```

여기에서 Home 함수가 입력받은 모든것은 props가 되는데 이 경우에는 name이 되겠지. 정말 신기한것은 입력받을 값을 미리 정의하지 않아도 된다는것?! hahahaha but,, 불러올 수 도 잇나?..>> 확인 결과 불러올 수는 없고 입력은 할 수 있네! 다시 불러오려면 미리 정의를 해야해!!~!@@!

2.map은 무엇:??  무엇이든 안되면 그 본질로 파고들어야 한다. 껍데기만 핥은 오늘의 교훈

map이란 어떠한 array에 대하여 그 array의 각각의 요소들에 대한 함수를 실행시키고 결과를 리턴하는 javascript의 함수야... 정말 어려운 설명이지??.. 코드를 통해 함께 보자~! 쉬울거야 that's easy@

이 코드를 f12누르고 콘솔창에 실행시켜봐!  chicken 의 값은 바뀌지 않지만 하하하 

```jsx
const chicken =["BHC","BBQ","ZzangDDARK","PURADARK!","OUTDARK!"]
chicken.map(brand =>{
console.log(brand); return 0;})
```

3.axios는 무엇인가? Oct 16, 2020 하루종일 이놈이랑 map때문에 골머리를 앓았다.

axios란 https에서 자료를 얻어오기위한 node.js기반의 http 클라이언트입니다. /// 어렵다..

쉽게 이해하면 자료 받아올때 내놔! 라고 소리쳐주는 형같은 느낌이야 ? 오늘 준혁이형 해어져서 술마신다고 불려나가느라 완성을 못했다.. : 아래 내일 공부할 자료 링크들을 올리는것으로 마무리 짓고 내일 진짜 마무리 해야겠다.

당장 되도 않는 코드를 작성하며 골머리를 앓는것 보다는 어느정도 개념을 잡아가며 코드를 적자!.  내가 적는 코드의 기능은 완벽히 파악하며 적기

[https://joshua1988.github.io/web-development/javascript/javascript-asynchronous-operation/](https://joshua1988.github.io/web-development/javascript/javascript-asynchronous-operation/)

[https://joshua1988.github.io/web-development/javascript/promise-for-beginners/](https://joshua1988.github.io/web-development/javascript/promise-for-beginners/)

[https://joshua1988.github.io/web-development/javascript/js-async-await/](https://joshua1988.github.io/web-development/javascript/js-async-await/)

[https://reactnative.dev/docs/flatlist.html](https://reactnative.dev/docs/flatlist.html)
