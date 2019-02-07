# __Day05 토메이로___

* 문제

https://www.acmicpc.net/problem/7576

<img width="435" alt="3-5_1" src="https://user-images.githubusercontent.com/29175001/51960414-45705a80-249c-11e9-982a-42497fbf1fd8.png">
<img width="440" alt="3-5_2" src="https://user-images.githubusercontent.com/29175001/51960418-4903e180-249c-11e9-9ca2-b41b6e308cb9.png">
  

* 내가 작성한 코드
```Python3

a,b =map(int,input().split())
miro = [[0]*a for _ in range(0, b)]

for i in range(b):
    c=input().split()
    for j in range(a):
        miro[i][j]=int(c[j])
        

def bfs(q,miro,x,y):
	dx=[-1,1,0,0]
	dy=[0,0,-1,1]
	
	
	for i in range(4):
		cx=x+dx[i]
		cy=y+dy[i]
		
		if cx>=0 and cy>=0 and cx<b and cy<a :
			if miro[cx][cy]==0:
				q.append((cx,cy))
				miro[cx][cy] = miro[x][y] + 1
				

	
q=[]
for k in range(b):
	for r in range(a):
		if miro[k][r]==1:
			q.append((k,r))
			while q :
				q.pop(0)
				bfs(q,miro,k,r)
        
```


* 채점 결과

실패..토마토는 원래 혼자 알아서 잘 익는데..  
  
  
----

  

* 두번째 시도
```Python3

a,b =map(int,input().split())
miro = [[0]*a for _ in range(0, b)]

for i in range(b):
    c=input().split()
    for j in range(a):
        miro[i][j]=int(c[j])

visited = [[0]*a for _ in range(b)] #visit배열 만들기

dx=[-1,1,0,0]
dy=[0,0,-1,1]

def bfs():
	while q:
		x,y=q.pop()
		for i in range(4):
			cx=x+dx[i]
			cy=y+dy[i]
			if cx>=0 and cy>=0 and cx<b and cy<a :
				if visited[cx][cy]==0 and miro[cx][cy]==0:
					q.append((cx,cy))
					miro[cx][cy] = 1
					visited[cx][cy] = visited[x][y]+1
					
				elif visited[cx][cy]==0 and miro[cx][cy]== -1 :
					visited[cx][cy] = -1
					
  
def day():
	max=0
	for k in range(b):
		for r in range(a):
			if miro[k][r]==0 :
				return -1
				
			elif visited[k][r]>max :
				max = visited[k][r]
				
	return max-1	

q=[]

for k in range(b):
	for r in range(a):
		if miro[k][r]==1 and visited[k][r]==0:
			q.append((k,r))
			visited[k][r]= 1

bfs()	
print(day())
	



	
        
```


* 채점 결과

테스트케이스 3번째 빼고 
