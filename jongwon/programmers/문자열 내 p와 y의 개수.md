# [프로그래머스] 문자열 내 p와 y의 개수

</br>

### 문제 설명
대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

### 제한사항
문자열 s의 길이 : 50 이하의 자연수
문자열 s는 알파벳으로만 이루어져 있습니다.

</br>

### 입출력 
| s | return |
|:---:|:---:|
| "pPoooyY" | true | 
| "Pyy" | false | 

<br>

### 입출력 예 설명
입출력 예 #1
'p'의 개수 2개, 'y'의 개수 2개로 같으므로 true를 return 합니다.

입출력 예 #2
'p'의 개수 1개, 'y'의 개수 2개로 다르므로 false를 return 합니다.

</br>

### 풀이



```python
def solution(s):
    answer = True
    a = 0
    b = 0
    
    for i in s[:]:
        if i == "p" or i == "P":
            a += 1
        elif i == "y" or i == "Y":
            b += 1
            
    if a != b:
        answer = False
        
    return answer

```

</br>

### 다른 사람 풀이 분석

- 대소문자 구분이 없기 때문에 모두 소문자로 만들기
- p 와 y 를 count 하며 바로 비교 후 리턴

```python

def solution(s):
    return s.lower().count('p') == s.lower().count('y')

```


