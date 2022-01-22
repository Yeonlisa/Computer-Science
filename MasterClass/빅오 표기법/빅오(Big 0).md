# 빅오 표기법이 필요한 이유
코드를 일반화하고 코드에 대해 말해주고 코드의 상대적 성과를 비교하기 위함
## 종류
- 시간 복잡도(time complexity)
```js
function addUpTo(n) {
  return n * (n + 1) / 2;
} // O(1)
```
```js
function addUpTo(n) {
  let total = 0;
  for (let i = 1; i <= n; i++) {
    total += i;
  }
  return total;
} // O(n)
```
```js
function countUpAndDown(n) {
  console.log("Going up!");
  for (let i = 0; i < n; i++) {
    console.log(i);
  }
  console.log("At the top!\nGoing down...");
  for (let j = n - 1; j >= 0; j--) {
    console.log(j);
  }
  console.log("Back down. Bye!");
} // O(n)
```
```js
function printAllPairs(n) {
  for (var i = 0; i < n; i++) {
    for (var j = 0; j < n; j++) {
      console.log(i, j);
    }
  }
} // O(n^2)
```
![스크린샷 2022-01-23 오전 3 23 38](https://user-images.githubusercontent.com/72447026/150650879-201558ac-fad0-468f-9e9e-73e087902cdb.png)
- 공간 복잡도(space complexity)
```js
function sum(arr) {
  let total = 0; // one number
  for (let i = 0; i < arr.length; i++) { // another number
    total += arr[i];
  }
  return total;
} // O(1)
```
```js
function double(arr) {
  let newArr = [];
  for (let i = 0; i < arr.length; i++) {
    newArr.push(2 * arr[i]);
  }
  return newArr; // n numbers
} // O(n)
```
## log 읽는 법
log<sub>2</sub>(8) = 3 -> 2<sup>3</sup> = 8 <br>
log<sub>2</sub>(value) = exponent -> 2<sup>exponent</sup> = value <br>
log === log<sub>2</sub>
