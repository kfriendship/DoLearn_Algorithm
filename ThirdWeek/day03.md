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
  
  
----
  
* 다시 푼 코드
```Python3

a,b=map(int,input().split())
miro = [[0]*b for _ in range(0, a)]

for i in range(a): #미로만들어주기
   c=input()
   for j in range(b):
      miro[i][j]=int(c[j])
      
visited = [[0]*b for _ in range(a)] #visit배열 만들기
      
dx=[-1,1,0,0]
dy=[0,0,-1,1]


def bfs(x,y):
	q = [(x,y)]
	visited[x][y] = 1 #시작값은 1로 설정
	
	while q: #q 비어있을때까지 실행
		x,y=q.pop(0)
		for i in range(4):
			cx=x+dx[i]
			cy=y+dy[i]
			if cx>=0 and cy>=0 and cx<a and cy<b :
				if visited[cx][cy]==0 and miro[cx][cy]==1:
					q.append((cx,cy))
					visited[cx][cy] = visited[x][y]+1 #한칸씩 이동할때마다 1씩 증가시켜서 저장
						
bfs(0,0)
print(visited[a-1][b-1])
						
					
	
 

```
  
  
* 채점 결과  

성공!!

						
					
	
 
  
  


