## 변수 Hoisting 이란?
* 건축/ 건설이나 화물 운반에 사용되는 장비를 "HOIST" 라고 나는데 즉, 아래에 위치한 것을 위로 끌어 올리는 역할을 한다.
* javascript 에서 hoisting 은 코드에 선언된 변수 및 함수를 코드 상단으로 끌어올리는 것을 말한다.
* 변수를 선언 시 ,해당 변수가 속한 범위의 최상단으로 올려지는 현상을 말한다.
* 여기서 속한 범위는 BLOCK 레벨이 아닌 FUNCTION 레벨에 해당한다.

### * 함수 내에서 선언한 함수 범위의 변수는, 해당 함수의 최상위로,

### * 함수 밖에서 선언된 전역 (global) 범위의 전역 변수는 스크립트 단위의 최상위로 끌어 올려진다.

> But, 여기서 헷갈리는 부분은 변수의 선언과 할당 모두를 상단으로 끌어올리는 것이 아니다.<br>
>선언(declared) 부분만 분리하여 최상위로 올린다. 변수에 값을 할당하는 내용은 원래 그 라인에 있다.

## "var" 사용시 변수 선언단계와 초기화단계가 동시에 진행한다.
```javascript
    console.log(name) // undefined
    var name = ‘seo’
```
위 코드에서 var 로 선언된 변수는 hoisting 되어 선언과 초기화가 동시에 이뤄지기 때문에 undefined로 출력됩니다.

## "let" 사용 시 변수 선언단계와 초기화단계가 분리되어 진행된다.

```javascript
    console.log(name) // ReferenceError: name is not defined
    let name = ‘seo’
```
let 키워드로 선언된 변수는 hoisting 되어 선언단계가 이뤄지지만 초기화 단계는 실제 let이 사용된 코드에 도착했을 때 이뤄집니다.<br> 초기화 단계 이전에 변수에 접근하려하면 reference 에러가 발생합니다.

## "const" 사용시 변수 선언단계와 초기화단계가 동시에 진행되는 것이 강제된다.
```javascript
    var name;
    name = 'seo' // 분리 가능

    const age;    // const 변수를 선언만 할 경우 에러가 발생
    age  = '29';
```
## var는 함수 레벨 스코프를 가지므로, 블록 내부에 선언되어도 외부에서 접근할 수 있다.

# 결론!!

* var 사용은 권장하지 않는다. 함수 레벨이므로 for 문 변수 선언시 var 사용하면 그대로 적용되는 문제 등, <br>
어디서든 쓰이는 단점이 있다.
* 호이스팅의 문제도 있기 때문에 내가 이 변수를 어디서 어떻게 쓰이는지 파악하기가 힘들고<br>
예상치 못한 문제가 발생할 수 있다. 그래서 사용을 "지양"하자.