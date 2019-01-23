# **Day06_포도주시식**

* 문제

https://www.acmicpc.net/problem/2156

<img width="423" alt="2-5" src="https://user-images.githubusercontent.com/29175001/51533568-9d98d280-1e86-11e9-92f5-91fc4a6c4555.png">

  

* 내가 작성한 코드
```Python3

a=int(input())
result=[]
for i in range(a):
    b=int(input())
    result.append(b)
    
ss=[]
ss.append(0)
ss.append(result[0])
ss.append(result[0]+result[1])

if a>2 :
    for k in range(3,a+1):
        ss.append(max(ss[k-1], ss[k-2]+result[k], ss[k-3]+result[k-1]+result[k]))
    
print(ss[a])
        
```


* 채점 결과

실패...포도주를 그냥 마시면되지...휴
  
  


