# Day 01:

### Function which returns a random number in the given range

Create a function which returns a random number in the given range of values both inclusive

### Answer

```javascript
function randomNumberGeneratorInRange(rangeStart, rangeEnd) {
    return Math.floor(Math.random() * (rangeEnd - rangeStart + 1)) + rangeStart
}

console.log(`My random number: ${randomNumberGeneratorInRange(5, 100)}`)
```

## 내용 정리

[출처](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/random)

### Math.random()의 반환 값

`Math.random()`는 0 이상 1 미만(`[0, 1)`)의 부동소숫점 의사 난수를 반환한다.

### 두 값 사이의 난수 생성하기

아래의 함수는 min 이상 max 미만의 난수를 반환한다.

```javascript
function getRandomArbitrary(min, max) {
  return Math.random() * (max - min) + min
}
```

### 두 값 사이의 정수 난수 생성하기

아래의 함수는 min(min이 정수가 아니면 min 보다 큰 최소의 정수) 이상 max 미만의 정수인 난수를 반환한다.

```javascript
function getRandomInt(min, max) {
  min = Math.ceil(min)
  max = Math.floor(max)
  return Math.floor(Math.random() * (max - min)) + min
}
```
### 최댓값을 포함하는 정수 난수 생성하기

위 `getRandomIntInclusive()` 함수는 최솟값을 포함하지만, 최댓값은 포함하지 않는다.

최솟값과 최댓값을 모두 포함하는 결과가 필요할 경우, 아래의 `getRandomIntInclusive()` 함수를 사용할 수 있다.

```javascript
function getRandomIntInclusive(min, max) {
  min = Math.ceil(min)
  max = Math.floor(max)
  return Math.floor(Math.random() * (max - min + 1)) + min
}
```

위 문제는 최솟값과 최댓값을 모두 포함하는 결과가 필요했기 때문에 `getRandomIntInclusive()` 함수를 적절히 활용해 풀었다.
