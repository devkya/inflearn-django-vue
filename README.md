# Vue 학습

[유투브 강의 링크](https://www.youtube.com/watch?v=b0ImUEsqaAA)

## vue 설치

```bash
sudo npm install -g @vue/cli
```

## 구조

- package.json : 프로젝트 구조
  - browserslist : 지원하는 브라우저 정의
- src/main.js : vue 호출

## 프로젝트 생성

```bash
 vue create 'project name'
```

- Manually select features : 사용자 정의 프로젝트 생성 -> <b>정리하기</b>
  - PWA
  - Router : 화면 이동을 할 수 있음
  - Vuex

## Router

최종적으로 올리게 되는 파일은 index.js 파일이다.  
우리가 설치하거나 필요한 파일은 컴파일 되어 chunk-vendors.js 로 들어간다.  
생성된 코드는 컴파일 되어 app.js 로 들어가게 된다.

- router component 연결 방식

1. import 하여 사용
2. lazy load
3. prefetch true - 연관성 있는 파일들끼리 묶어주는게 좋음

## Code Spltting

- Lazy load : vue는 빌드하면 소스코드가 하나의 파일로 생성하는데 큰 프로젝트에서는 파일이 매우 커져서 사용자가 처음 웹사이트를 접속할 때 렌더링 지연되는 문제가 있음. 이것을 라우터 별로 분리(code splitting)하여 현재 라우터에서 필요한 파일만 원격으로 내려받도록 하는 기술
  vue-router에서 주석으로 처리된 "webpackPrefetch : true" 를 넣어주면 적용됨

## Vscode 세팅

- default-formatter : Prettier -> .prettierrc 로 설정 변경

```
# .prettierrc
{
    "semi" : false,
    "bracketSpacing" : true,
    "singleQuote": true,
    "useTabs": false,
    "trailingComma": "none",
    "printWidth": 80
}
```

- package.json -> "rules" : {"space-before-function-paren" : "off" } => function 만들 때, 규칙 off 함

## vue.js

- components vs views
  - views는 화면 전체, components 재사용 가능한 component
  - views 폴더 안에 naming은 ~View.vue
- template 안에는 최상의 태그가 반드시 필요 - div tag 많이 씀
- databinding
  - string : {{ string }}
  - html : v-html
  - checkbox는 반드시 배열과 양방향 소통함
  - radio는 문자열로 소통함
  - readonly 속성이 있을 때 v-model을 사용할 필요 없음, v-bind:value="userId" => 단방향 공유
  - v-bind : attr 값을 변경할 때 사용함
    - attr class 적용 가능 : 동적으로 클래스를 바인딩할 수 있음
  - v-for을 사용할 때는 attr key 가 반드시 필요

* vue user snippets 등록
  Configure User Snippets

```
  "Generate Basic Vue Code": {
    "prefix": "vue-start",
    "body": [
      "<template>\n\t<div></div>\n</template>\n<script>\nexport default {\n\tcomponents: {},\n\tdata() {\n\t\treturn {\n\t\t\tsampleData:''\n\t\t}\n\t},\n\tsetup() {},\n\tcreated() {},\n\tmounted() {},\n\tunmounted() {},\n\tmethods: {}\n}\n</script>"
    ],
    "description": "Generate Basic Vue Code"
  }
```

- v-html, v-model 등 directive
  Html 안에서 vue element 에서 사용되는 특별한 속성

  - v-model : 양방향으로 데이터가 전달됨
  - v-model.number : 숫자로 변환

  * Event
