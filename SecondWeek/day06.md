# **Day05_1만들기**

* 문제

https://www.acmicpc.net/problem/2156

<img width="423" alt="2-5" src="https://user-images.githubusercontent.com/29175001/51533568-9d98d280-1e86-11e9-92f5-91fc4a6c4555.png">

  

* 내가 작성한 코드
```Python3

# your code goes here
a=int(input())

result = []
result.insert(0,0)
result.insert(1,0)
result.insert(2,1)
result.insert(3,1)


for i in range(4,a+1):
	result.insert(i,1+result[i-1])
	if (i%2 == 0) :
		result[i]=min(result[i],1+result[i//2])
	if (i%3 == 0) :
		result[i]=min(result[i],1+result[i//3])

		
print(result[a])
        
```


* 채점 결과

성고응!  
  
  


