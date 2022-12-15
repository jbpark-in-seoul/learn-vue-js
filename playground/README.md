## 용어 및 개념 정리
* 뷰 컴포넌트
    * 컴포넌트는 화면의 영역을 구분하여 개발할 수 있는 뷰의 기능입니다.
    * 컴포넌트 기반으로 화면을 개발하게 되면 `재사용성`이 올라가고 빠르게 화면을 제작할 수 있습니다.
* 전역 컴포넌트와 지역 컴포넌트의 차이
    * 전역 컴포넌트
        * 선언된 전역 컴포넌트는 어떤 인스턴스에서든 사용이 가능하다.
        * 주로 라이브러리 혹은 플러그인을 등록할 때 사용한다.
    * 지역 컴포넌트
        * 생성된 인스턴스에서만 사용이 가능하다.
* 컴포넌트 통신 방식
    * 뷰 컴포넌트는 각각 고유한 데이터 유효 범위를 갖는다.
    * 컴포넌트 간에 데이터를 주고 받기 위해서는 특정 규칙을 갖는다.
        * 상위 컴포넌트 -> 하위 컴포넌트 : `props` 속성을 이용하여 데이터 전송
        * 하위 컴포넌트 -> 상위 컴포넌트 : `event` 전송
        * 동일 계층 컴포넌트 : 상위 컴포넌트 전달 후 동일 계층 컴포넌트로 전송 (`emit` -> `props`)
    * 통신된 데이터는 `reactivity`가 적용된다.
* 뷰 라우터
    * 뷰 라우터는 뷰 라이브러리를 이용하여 싱글 페이지 애플리케이션을 구현할 때 사용하는 라이브러리이다.
    * `router-view`
        * 브라우저의 주소 창에서 URL이 변경되면, 앞에서 정의한 `routes` 속성에 따라 해당 컴포넌트가 화면에 뿌려진다. 이때 뿌려지는 지점이 템플릿의 `<router-view>`다.
    * `router-link`
        * 일반적으로 웹 페이지에서 페이지 이동을 할 때는 사용자가 URL을 입력해서 이동하지 않는다.
        * 클릭해서 페이지를 이동할 수 있게 해주는게 `<router-link>`다.
        * 코드를 실행하면 `<a>` 태그로 변형되서 나타난다.
* 액시오스(axios)
    * 뷰에서 권고하는 HTTP 통신 라이브러리는 엑시오스(Axios)이다.
    * Promise 기반의 HTTP 통신 라이브러리이며 상대적으로 다른 HTTP 통신 라이브러리들에 비해 문서화가 잘되어 있고 API가 다양하다.
    * 자바스크립트의 비동기 처리 패턴
        * `callback`
        * `promise`
        * `promise` + `generator`
        * `async` & `await`
* 템플릿 문법
    * 데이터 바인딩
        ```html
        <div>{{ message }}</div>
        ```
    * 뷰 디렉티브   
        ```html
        <div>Hello <span v-if="show">Vue.js</span></div>
        ```
* Vue CLI 버젼별 차이점
    * [Vue CLI 2.x]
        * vue init '프로젝트 템플릿 유형' '프로젝트 폴더 위치'
        * vue init webpack-simple '프로젝트 폴더 위치'
    * [Vue CLI 3.x]
        * vue create '프로젝트 위치'
* 뷰 코드 컨벤션
    * `.vue` 파일은 두 단어 이상으로 조합
        * 프로그램 입장에서는 `HTML` 속성 예약어와 구분이 안되기 때문에 두 단어로 조합해야함
    * 파일명은 `파스칼케이스` 사용


    

* 학습 참고 사이트
    * [Vue.js 공식 사이트](https://vuejs.org/)
    * [네비게이션 가드](https://joshua1988.github.io/web-development/vuejs/vue-router-navigation-guards/)
    * [자바스크립트 비동기 처리와 콜백 함수](https://joshua1988.github.io/web-development/javascript/javascript-asynchronous-operation/)
    * [자바스크립트 Promise 이해하기](https://joshua1988.github.io/web-development/javascript/promise-for-beginners/)
    * [자바스크립트 async와 await](https://joshua1988.github.io/web-development/javascript/js-async-await/)
    * [자바스크립트의 동작원리: 엔진, 런타임, 호출 스택](https://joshua1988.github.io/web-development/translation/javascript/how-js-works-inside-engine/)