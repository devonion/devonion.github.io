
## 서버 개발자의 Front-end 입문기

### ECMAScript
초창기 Netscape에서 javascript를 처음 적용하였고 Explorer 에서도 Jscript 라는 이름으로 javascript 를 지원하게 된다. Netscape 에서는 표준화를 위해 자바스크립트 표준 규격을 ECMA 로 넘기게 된다. 이후 ECMA 에서 ECMAScript 라는 이름으로 자바스크립트 표준 규격을 발표하고 있다. 

```
ECMA (European Association for Standardizing Information and Communication Systems)  
프로그램 언어나 입출력 코드를 포함한 컴퓨터 작동의 형식을 표준화 하는 것을 목적으로 1961년에 설립된 단체
```

현재 대부분의 브라우저에서는 ES5 를 지원하며 ES6는 제한적으로 지원한다. 지원 브라우저에 대한 정보를 제공하는 사이트가 있으니 확인해 보도록 한다. 
[http://kangax.github.io/compat-table/es6/](http://kangax.github.io/compat-table/es6/)

ES6로 개발을 하고 싶은데 브라우저 지원이 제한적이므로 ES5로만 개발을 해야 하는가?
ES6로 개발한 코드를 ES5 코드로 변환해주는  [babel]( https://babeljs.io/) 을 이용하면 ES6로 개발이 가능하다.


### ECMAScript 적응하기

#### 변수 선언

var  
변수를 선언.  
let  
블록 범위(scope) 지역 변수를 선언.  
const   
읽기 전용 상수를 선언.  

- var 키워드는 지역 및 전역 변수 선언에 모두 이용 가능.
- let은 블록 범위 지역 변수 선언에 사용
- const는 상수 선언에 사용되면 읽기만 가능.
- x = 3 로 선언하면 전역 변수로 지정.
- 블록 범위에 대한 개념은 ES6 부터 적용.

#### 변수 호이스팅(hoisting)

var 키워드를 사용하여 나중에 선언한 변수를 참조 할 수있다. 이러한 호이스팅 특성 때문에 모든 var 문은 가능한 함수 상단에 두는 것이 코드를 더 명확하게 한다.

호이스팅으로 인해 아래 두 코드는 동일하게 볼 수 있다.

<pre><code>
console.log(x === undefined); // logs "true"
var x = 3;

----------------------------------------------------

var myvar = "my value";

(function() {
  console.log(myvar); // undefined
  var myvar = "local value";
})();
</code></pre>

<pre><code>
var x;
console.log(x === undefined); // logs "true"
x = 3;

----------------------------------------------------

var myvar = "my value";

(function() {
  var myvar;
  console.log(myvar); // undefined
  myvar = "local value";
})();
</code></pre>

#### 전역 변수

전역 변수는 global 변수의 속성으로 웹 페이지에서 global 객체는 widnow 이므로 window.variable 구문을 통해 전역 변수를 설정하고 접근할 수 있다.

#### 상수

const 상수는 let 과 같이 블록 범위를 가진다. 

<pre><code>
function test() {
    const MAX_VAL = 15;
}

console.log(MAX_VAL); //ReferenceError: MAX_VAL is not defined
</code></pre>


#### 데이터 형

원시 데이터형  
- Boolean. true와 false  
- null. null 값을 나타내는 특별한 키워드. JavaScript는 대소문자를 구분하므로, null은 Null, NULL 혹은 다른 변형과도 다릅니다.  
- undefined. undefined 값인 최상위 속성.  
- Number. 42 혹은 3.14159.  
- String. "안녕"  
- Symbol. (ECMAScript 6에 도입) 인스턴스가 고유하고 불변인 데이터 형.  

그 외  
- Object  

문자열을 숫자로 변화

- parseInt()  
- parseFloat()  

parseInt(string, radix) 사용 시 디폴트는 10진법이 적용되기는 하나 명시적으로 지정하는 것이 좋다.

Symbol????????????

#### 리터럴

문자열 템플릿 리터럴
<pre><code>
var name = "Bob", time = "today";
console.log(`Hello ${name}, how are you ${time}?`);
</code></pre>
