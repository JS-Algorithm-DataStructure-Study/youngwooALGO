# 섹션 3 : 배열과 오브젝트의 성능평가

## 객체의 빅오

```jsx
let instructor = {
	firstName= "youngwooo",
}
```

객체 - 정렬되어 있지 않을때, 빠른 접근, 삽입, 삭제시 사용

Insertion, Removal, access O(1)

Searching - O(N) → 정렬되어있지 않기 때문임

해쉬맵으로 구현되어있음

탐색은 선형시간임 → value를 찾는 경우 모든 value를 확인해야함

Object.keys - O(N) - 키 배열

Object.values - O(N) - 밸류 배열

Object.entries - O(N) - 키, 밸류 배열 리턴

hasOwnProperty - O(1) - 키 있는지 없는지 찾음

## 배열안의 데이터에 접근이 느린이유

배열 - 정렬되어있는 데이터 사용하고 싶을때 사용

Searching - O(N)

Access - O(1)

Insertion, Removal

배열 뒤에 삽입, 제거 → O(1)  

배열 앞에 삽입, 제거 → O(N)

탐색 → 노정렬 → O(N)

## 빅오 배열 메소드

push - O(1)

pop - O(1)

shift - O(N)

unshift - O(N)

concat - O(N) - 배열 합침

slice - O(N) - 배열 일부, 전체 가져옴(복사)

splice - O(N) - 배열 엘리먼트 추가, 삭제, 교체

sort - O(N * log N)

forEach, map, filter, reduce… - O(N)

당연한 것들이고, shift, unshift, slice, splice 사용법 한번씩 익히면 될듯