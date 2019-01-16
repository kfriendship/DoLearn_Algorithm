# **Day01-1_같은 숫자는 싫어**

* 문제

https://programmers.co.kr/learn/courses/30/lessons/12906

<img width="348" alt="day1-1_problem" src="https://user-images.githubusercontent.com/29175001/50890840-51896f00-143e-11e9-855d-0a0311be3088.png">












* 내가 작성한 코드
```Python3

def solution(arr):
    answer = []
    for i in range(len(arr)):
        if (i==0) :
            answer.append(arr[i]) 
        else :
            if (arr[i] != arr[i-1] ) :
                answer.append(arr[i]) 
        
    return answer
```
* 채점 결과

정확성: 71.9

효율성: 21.1

합계: 93.0 / 100.0

---
#### __<스터디 복습>__  

* 다른 코드
```Python3

def solution(arr):
    answer = []
    cur_num = -1
    for item in arr:
        if cur_num != item:
            cur_num = item
            answer.append(item)
    return answer
```







# **Day01-2_두 정수 사이의 합**

* 문제

https://programmers.co.kr/learn/courses/30/lessons/12912

<img width="346" alt="1-2_problem1" src="https://user-images.githubusercontent.com/29175001/50960062-d2f90400-1507-11e9-87ae-7bb6b7a6c1cc.png">
<img width="131" alt="1-2_problem2" src="https://user-images.githubusercontent.com/29175001/50960066-d5f3f480-1507-11e9-85be-7400d43d41f8.png">


* 내가 작성한 코드

```Python3

def solution(a, b):
    answer = 0
    if (a < b) :
        for i in range(a,b+1) :
            answer += i 
    elif (a == b) :
        answer = a
    else :
        for i in range(b, a+1) :
            answer += i
    return answer
    
```

* 채점 결과

채점 결과

정확성: 100.0

합계: 100.0 / 100.0

kiki

---
#### __<스터디 복습>__  

* 다른 코드(swap)
```Python3
def solution(a, b):
    answer = 0
    if a > b:
        a, b = b, a
    for i in range(a, b + 1):
        answer += i
    return answer
```
나는 a>b 일때랑 a>b 일때 나눠서 구했는데<br>
a,b=b,a 를 이용해 swap해주면 더 간단하게 짤수있다!  
good  
  
  
또한 고등학교때 배웠던 등차수열 합 공식을 이용하는 방법도 있다.  
https://www.youtube.com/watch?v=5cYZX47w7gQ 공식 증명 관련
  
  
* 다른 코드(등차수열 합)
```Python3
def solution(a, b):
    answer = 0
    if a > b:
        a, b = b, a
    a = a - 1
    answer = b*(b+1)/2 - a*(a+1)/2
    return answer
```  
  
등차수열 합 공식을 이용하게 되면 반복문을 사용하지 않기때문에  
실행속도가 빨라진다
