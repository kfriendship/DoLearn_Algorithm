# **Day03_미로 탐색**

* 문제

https://www.acmicpc.net/problem/2178

<img width="652" alt="3-3_1" src="https://user-images.githubusercontent.com/29175001/51959758-4784ea00-2499-11e9-9292-166531ccdd1f.png">
<img width="433" alt="3-3_2" src="https://user-images.githubusercontent.com/29175001/51959762-49e74400-2499-11e9-9852-8c603fd55e28.png">

  

* 내가 작성한 코드
```Python3

a,b=map(int,input().split())
miro = [[0]*b for _ in range(0, a)]

for i in range(a):
   c=input()
   for j in range(b):
      miro[i][j]=int(c[j])
      
visit = [[0]*y for _ in range(x)]

def dfs_recursive ():
        
```


* 채점 결과

모르겠다..다시 풀고임 일단 보류!
  
  


