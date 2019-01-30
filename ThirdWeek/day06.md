# __Day06_안전영역__

* 문제

https://www.acmicpc.net/problem/2468

<img width="655" alt="3-6_1" src="https://user-images.githubusercontent.com/29175001/51961190-42c33480-249f-11e9-9731-7b73b998d577.png">
<img width="659" alt="3-6_2" src="https://user-images.githubusercontent.com/29175001/51961195-45be2500-249f-11e9-9299-42009f33605a.png">

* 내가 작성한 코드
```Python3

# your code goes here
a=int(input())
land = [[0]*a for _ in range(0, a)]

for i in range(a):
    c=input().split()
    for j in range(a):
        land[i][j]=int(c[j])
        

def bfs(visited,land,x,y,num):
	queue = [(x,y)]
	
	dx=[-1,1,0,0]
	dy=[0,0,-1,1]
	
	
	while queue:
		n=queue.pop(0)
		x = n[0]
		y = n[1]
		if n not in visited:
			visited.append(n)
			for i in range(4):
				cx=x+dx[i]
				cy=y+dy[i]
				if cx>=0 and cy>=0 and cx<a and cy<a :
					if land[cx][cy] > num :
						queue.append((cx,cy))
					
	return visited
	
visited=[]	
safe=[]				
safe_max=[]
for num in range(1,10):
	for k in range(a):
		for r in range(a):
			if land[k][r] > num:
				if (k,r) not in visited:
					l=bfs(visited,land,k,r,num)
	safe.append(len(l))
	safe_max.append(len(safe))
print(max(safe_max))
        
```


* 채점 결과

망망망~
  
