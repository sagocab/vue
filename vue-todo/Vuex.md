Vuex - 상태관리 라이브러리
-------------------------------------------------------------------------
목차
* Vuex라이브러리 소개
  복잡한 애플리케이션의 컴포넌트들을 효율적으로 관리
* Flux 패턴 소개
* Vuex 컨셉과 구조
* Vuex 설치 및 시작하기
* Vuex 기술요소(state, getters, mutations, actions)
* Vuex Helpers
* Vuex로 프로젝트를 구조화 하는 방법과 모듈 구조화 방법\
-------------------------------------------------------------------------
> Vuex 란?
> 무수히 많은 컴포너트의 테이터를 관리하기 위한 상태관리 패턴이자 라이브러리
> React와 Flux 패턴에서 기인함
> Vue.js 중고급 개발자로 성장하기 위한 필수 관문

> Flux란?
** MVG 패턴의 복잡한 데이터 흐름 문제를 해결하는 개발 패턴 - Unidirectional data flow (한방향 데이터 흐름)
** Action -> Dispatcher -> Model -> View
1. action : 화면에서 발생하는 이벤트 또는 사용자의 입력
2. dispatcher : 데이터를 변경하는 방법, 메서드
3. model : 화면에 표시할 데이터
4. view : 사용자에게 비춰지는 화면


Vuex 컨셉
- State : 컴포넌트 간에 공유하는 데이터 data()
- View : 데이터를 표시하는 화면 template
- Action : 사용자의 입력에 따라 데이터를 변경하는 methods

Action -> State -> View -> Actioin (단방향 데이터 흐름 처리)

Vuex 구조
컴포넌트 -> 비동기 로직 -> 동기 로직 -> 상태

자바스크립트 비동기 처리와 콜백 함수 글 링크(클릭) 
https://joshua1988.github.io/web-development/javascript/javascript-asynchronous-operation/\

자바스크립트 Promise 쉽게 이해하기 글 링크(클릭)
https://joshua1988.github.io/web-development/javascript/promise-for-beginners/


Vue.use : Plug in 사용

@@ Vuex 기술 요소
> state : 여러 컴포넌트에 공유되는 데이터
> getter : 연산된 state 값을 접근하는 속성 computed
> mutation : state 값을 변경하는 이벤트 로직.메서드 method
> actions : 비동기 처리를 선언하는 메서드 async method

@state 란?
