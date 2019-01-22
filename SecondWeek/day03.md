# **Day03_다이나믹 프로그래밍 (피보나치 수)**

* 문제

https://www.acmicpc.net/problem/1003

<img width="573" alt="2-3" src="https://user-images.githubusercontent.com/29175001/51527420-c5cd0500-1e77-11e9-85c0-96e8f3f9235f.png">
  
  
** 피보나치표 **
<img width="658" alt="default" src="https://user-images.githubusercontent.com/29175001/51527491-ea28e180-1e77-11e9-9a39-090d41098653.png">
  
표를 보면 0과1의 호출횟수도 피보나치 수열을 따른다는 것을 알 수 있다.  
이것을 이용해 코드를 짜보면

* 내가 작성한 코드
```Python3

a=int(input())

zero = [1,0,1]
one = [0,1,1]
 
def fibo(num):
    a = len(zero)
    if a <= num:
        for i in range(a,num+1):
            zero.append(zero[i-1]+zero[i-2])
            one.append(one[i-1]+one[i-2])
    print("%d %d"%(zero[num],one[num]))
 
for i in range(a):
    b = int(input())
    fibo(b)
        
```


* 채점 결과

성고응!  
  
  


