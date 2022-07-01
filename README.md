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

# Code Spltting

- Lazy load : vue는 빌드하면 소스코드가 하나의 파일로 생성하는데 큰 프로젝트에서는 파일이 매우 커져서 사용자가 처음 웹사이트를 접속할 때 렌더링 지연되는 문제가 있음. 이것을 라우터 별로 분리(code splitting)하여 현재 라우터에서 필요한 파일만 원격으로 내려받도록 하는 기술
  vue-router에서 주석으로 처리된 "webpackPrefetch : true" 를 넣어주면 적용됨

## Vscode 세팅

- default-formatter : Prettier -> .prettierrc 로 설정 변경
- package.json -> "rules" : {"space-before-function-paren" : "off" } => function 만들 때, 규칙 off 함
