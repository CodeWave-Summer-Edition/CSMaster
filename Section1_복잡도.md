# Section1. 복잡도
## 0. 복잡도
*복잡도란?* 해당 문제를 해결하는데 지불해야하는 비용과 입력값의 크기 사이의 상관관계를 나타내는 척도.   
이 척도는 문제를 해결하는 알고리즘 및 자료구조를 최적화 하기 위함.   

## 1. 시간 복잡도(Time Complexity)
**해당 문제를 해결하는 시간적 비용과 입력값의 크기 사이의 상관관계를 나타내는 척도**
### 빅 오(Big Oh) 표기법
![BigOh](https://github.com/CodeWave-Summer-Edition/CSMaster/assets/43038815/141641b7-68b5-4443-b36f-b6b61e71ab15)   
이미지 출저 : [www.cs.washington.edu](https://player.slideplayer.com/31/9739625/#)
```
모든 n > n0 > 0 에 대해서 0 <= f(n) <= k*g(n) 인 양의 상수 k와 n0가 존재한다면, f(n) = O(g(n)) 을 만족한다.
```
- 최악의 경우의 시간복잡도
- 시간복잡도의 상한 점근
- 표기는 O(n), O(n^2), O(nlogn) 등등..

### 빅 오메가(Big Omega) 표기법
```
두 함수 f(n), g(n) 이 있을 때, n1 <= n , f(n) >= C*g(n) 이 성립하는 상수 C, n1이 존재하면, f(n) = Ω(g(n)) 을 만족한다.
```
- 최선의 경우의 시간복잡도
- 시간복잡도의 하한 점근

### 빅 세타(Big Theta) 표기법
```
두 함수 f(n), g(n)이 있을 때, n1<=n, C1*g(n) <= f(n) <= C2*g(n) 이 성립하는 상수 C1, C2, n1이 존재하면 f(n) = θ(g(n)) 을 만족한다.
```
- Big-Oh 와 Big Omega의 중간. 평균적인 값

## 시간복잡도 표현
- 시간 복잡도는 보통 최악의 경우인 `Big-Oh` 로 표현한다.
- 시간 복잡도는 상수를 제외하고 표현합니다.
    - O(2n+10) -> x
    - O(n) -> o

## 대표적인 Big-Oh
![TimeComplexityGraph](https://miro.medium.com/v2/resize:fit:1053/1*kO69dq_xml2q3o2NH9OZ3g.png)   
[이미지 출저 : oscarnieves100.medium.com](https://oscarnieves100.medium.com/computational-complexity-simply-explained-add2b99cf48c)


## 2. 공간 복잡도
**해당 문제를 해결하는 공간적 비용과 입력값의 크기 사이의 상관관계를 나타내는 척도**
```java
int[] arr = new int[n];
```
위에 대한 공간 복잡도는 O(n)이 된다.

## 3. 시간복잡도와 공간복잡도의 존재 이유
- 효율적인 코드로 개선하는 데 쓰이는 척도