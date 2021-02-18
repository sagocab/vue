ES6 ( ECMAScript 2015)
- 2015년은 ES5(2009)이래로 진행한 첫 메이저 업데이트가 승인된 핸
- 최신 Front-End Framework인 React, Angular, Vue에서 권고하는 언어 형식
- ES5에 비해 문법이 간결해져서 익숙해지면 코딩을 훨씬 편하게 할 수 있음.

* Babel
- ES6의 문번을 각 브라우저의 호환 가능한 ES5로 변환하는 컴파일러

* 함수 표현식
var sum = function(){
    return 10 + 20;
};

------------------------------------------------------------------------
const & let - 새로운 변수 선언 방식
- 블록단위 {}로 변수의 범위가 제한되었음
- const : 한번 선언한 값에 대해서 변경할 수 없음(상수 개념)
- let : 한번 선언한 값에 대해서다시 선언할 수 있음.

let sum = 0;
for(let i = 1 ; i <= 5 ; i++){
    sum = sum + 1;
}
console.log(sum);//10
console.log(i);//error

const로 지정한 값 변경 불가능
const a = 10;
a = 20;//Uncaught TypeError : Assignment to constant variable

하지만, 객체나 배열의 내부는 변경 가능
const a = {};
a.num = 10;

const a = [];
a.push(20);
------------------------------------------------------------------------
Arrow Function
- 함수를 정의할때 function 이라는 키워드를 사용하지 않고 => 대체
- 흔히 사용하는 콜백 함수의 문번을 간결화
//ES5
var sum = function(a, b){
    return a + b;
};
//ES6
var sum = (a, b) => {
    return a + b;
}

sum(10, 20);

//ES5
var arr = ["a","b","c"];
arr.forEach(function(value){
    console.log(value);
});

//ES6
var arr = ["a","b","c"];
arr.forEach(value => console.log(value));

------------------------------------------------------------------------
Enhanced Object Literals
var dictionary = {
    words : 100,
    //ES5
    lookup : function(){
        console.log("find words");
    },

    //ES6
    lookup(){
        console.log("find words");
    }
};
------------------------------------------------------------------------
Modules
- 자바스크립트 모듈 로더 라이브러리(AMD, Common JS)기능을 js 언어 자체에서 지원
- 호출되기 전까지는 코드 실행과 동작을 하지 않는 특징이 있음
// libs/math.js
export function sum(x,y) {
    return x + y;
}

export var pi = 3.141593;

//main.js
import {sum} from 'libs/math.js';
sum(1,2);

- vue.js에 마주칠 default export
  한개의 하나만 export 됨.
// util.js
export default function(x){
    return console.log(x);
}

// main.js
import util from 'util.js'
console.log(util); // function (x) { return console.log(x); }\
util("hi");

//app.js
import log from 'util.js'
console.log(log);
log("hi");
------------------------------------------------------------------------

