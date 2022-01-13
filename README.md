# 1일차
```javascript
function sayHi() {
  console.log(name);
  console.log(age);
  var name = 'Lydia';
  let age = 21;
}

sayHi();
```
답 : D

풀이 : `var`는 `런타임 이전`에 선언되고 할당되었지만 값이 부여되지 않았기 때문에 undefined가 나온다. `let`은 선언은 되었지만 메모리가 할당되지 않았기 때문에 ReferenceError가 발생한다.

```javascript
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}

for (let i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 1);
}
```
답 : C

풀이 : `var i`의 반복문은 반복문의 횟수만큼 메모리의 값이 할당되고나서 i의 값이 메모리 각각에 들어가기 때문에 최종 값인 3이 들어간다. `let i`의 반복문은 메모리의 값이 할당됨과 동시에 i의 값이 들어가기 때문에 순차적으로 0, 1, 2라는 값이 출력된다.

ps : 추가 설명 필요