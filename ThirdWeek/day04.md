# __Day04_단지번호__

* 문제

https://www.acmicpc.net/problem/2667

<img width="593" alt="3-4_" src="https://user-images.githubusercontent.com/29175001/51959855-afd3cb80-2499-11e9-928e-60d4f1bf018c.png">


  

* 내가 작성한 코드
```Python3

a=int(input())
miro = [[0]*a for _ in range(0, a)]

for i in range(a):
	b=input()
	for j in range(a):
		miro[i][j]=int(b[j])
		
def dfs(miro, count, x, y):
	dx=[-1,1,0,0]
	dy=[0,0,-1,1]
	miro[x][y]=0
	
	for i in range(4):
		cx=x+dx[i]
		cy=y+dy[i]
		
		if cx>=0 and cy>=0 and cx<a and cy<a :
			if miro[cx][cy]==1:
				count= dfs(miro, count+1 , cx, cy)
				
	return count
	
one =[]
for k in range(a):
	for r in range(a):
		if miro[k][r]==1:
			one.append(dfs(miro,1,k,r))
			
print(len(one))
for item in sorted(one):
	print(item)
        
```


* 채점 결과

힘들게 성공!
  
  

