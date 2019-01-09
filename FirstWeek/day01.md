# **Day01_같은 숫자는 싫어**

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


채점 결과
정확성: 71.9

효율성: 21.1

합계: 93.0 / 100.0
