# [백준] 1008번 A/B

## 1. 출처

[1008번: A/B](https://www.acmicpc.net/problem/1008)

## 2. 문제

두 정수 A와 B를 입력받은 다음, A/B를 출력하는 프로그램을 작성하시오.

## 3. 입력

첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)

## 4. 출력

첫째 줄에 A/B를 출력한다. 실제 정답과 출력값의 절대오차 또는 상대오차가 $10^{-9}$ 이하이면 정답이다.

## 5. 예제

| 입력 | 출력 |
| --- | --- |
| 1 3 | 0.33333333333333333333333333333333 |
| 4 5 | 0.8 |

## 6. 문제풀이

```java
package week07;

import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		double A, B;
		A = sc.nextDouble();
		B = sc.nextDouble();
		
		System.out.println(A / B);
		
		sc.close();

	}

}
```

- 데이터 타입
    - 정수형 : **`int`** / **`long`**
        - **`int`** : 2147483648 ~ 2147483647 까지 표현
        - **`long`** : 9223372036854775808 ~ 9223372036854775807 까지 표현
            - **`long`** 변수의 값이 2147483647보다 큰 경우 접미사 L 붙이기
                
                ex) **`long a = 9223372036854775807L;`**
                
    - 실수형 : **`float`** / **`double`**
        - **`float`** : $±3.4*10^{-37}$  ~ $±3.4*10^{38}$ 까지 표현, 지수의 길이 8bit, 소수부분 6자리까지 오차 없이 표현
        - **`double`** : $±1.7*10^{-307}$  ~ $±1.7*10^{308}$ 까지 표현, 지수의 길이 11bit, 소수부분 15자리까지 오차 없이 표현
            - **`float`** 변수의 값에는 접미사 f 또는 F 붙이거나, 값 앞에 (float) 붙이기
                
                ex) **`float a = f3.14;`** 또는 **`float a = (float)3.14;`**