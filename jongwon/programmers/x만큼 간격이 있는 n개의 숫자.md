# [프로그래머스] x만큼 간격이 있는 n개의 숫자

</br>

### 문제 설명
함수 solution은 정수 x와 자연수 n을 입력 받아, x부터 시작해 x씩 증가하는 숫자를 n개 지니는 리스트를 리턴해야 합니다. 다음 제한 조건을 보고, 조건을 만족하는 함수, solution을 완성해주세요.

### 제한 조건
x는 -10000000 이상, 10000000 이하인 정수입니다.
n은 1000 이하인 자연수입니다.

</br>

### 입출력 
| x | n | return |
|:---:|:---:|:---:|
| 2 | 5 | [2,4,6,8,10] |  
| 4 | 3 | [4,8,12] | 
| -4 | 2 | [-4, -8] |

<br>


### 풀이

```python
def solution(x, n):
    answer = []
    a = x
    
    for i in range(n):
        answer.append(a)
        a += x
    
    return answer

```

</br>

### 다른 사람 풀이 분석
- 매우 간단하다.

```python

def solution(x, n):
    return [x*(i+1) for i in range(n)]

```


