# **Day04_123 더하기**

* 문제

https://www.acmicpc.net/problem/9095

<img width="412" alt="2-4" src="https://user-images.githubusercontent.com/29175001/51530988-8a363900-1e7f-11e9-8179-634c5f43b1f4.png">

  

* 내가 작성한 코드
```Python3

a = int(input())
 
result = []
result.insert(0, 0) 
result.insert(1, 1) # 1을 넣을 경우 경우의 수 1가지(1)
result.insert(2, 2) # 2를 넣을 경우 경우의 수 2가지(1+1, 2)
result.insert(3, 4) # 3을 넣을 경우 경우의 수 3가지 (1+1+1, 1+2, 2+1, 3)
 
for i in range(0, a):
    n = int(input())
    for j in range(4, n+1):
        result.insert(j, result[j-1] + result[j-2] + result[j-3])
    print(result[n])
        
```


* 채점 결과

성고응!  
  
  


