[TOC]

## 서버 개발자의 Front-end 입문기

### ECMAScript
초창기 Netscape에서 javascript를 처음 적용하였고 Explorer 에서도 Jscript 라는 이름으로 javascript 를 지원하게 된다. Netscape 에서는 표준화를 위해 자바스크립트 표준 규격을 ECMA[^ECMA] 로 넘기게 된다. 이후 ECMA 에서 ECMAScript 라는 이름으로 자바스크립트 표준 규격을 발표하고 있다. 

현재 대부분의 브라우저에서는 ES5 를 지원하며 ES6는 제한적으로 지원한다. 지원 브라우저에 대한 정보를 제공하는 사이트가 있으니 확인해 보도록 한다. 
[http://kangax.github.io/compat-table/es6/](http://kangax.github.io/compat-table/es6/)

ES6로 개발을 하고 싶은데 브라우저 지원이 제한적이므로 ES5로만 개발을 해야 하는가?
ES6로 개발한 코드를 ES5 코드로 변환해주는  [babel]( https://babeljs.io/) 을 이용하면 ES6로 개발이 가능하다.

[^ECMA]:
* ECMA (European Association for Standardizing Information and Communication Systems)
프로그램 언어나 입출력 코드를 포함한 컴퓨터 작동의 형식을 표준화 하는 것을 목적으로 1961년에 설립된 단체


