# **Day02-1_조교는 새디스트야!**

* 문제

https://www.acmicpc.net/problem/14656

<img width="781" alt="2-1_problem" src="https://user-images.githubusercontent.com/29175001/51030989-82080f00-15de-11e9-81d8-38f0506a1ad7.png">






* 내가 작성한 코드
```Python3

import sys
lines=sys.stdin.readlines()
a=lines[0]
b=lines[1].split()
result =0 

for i in range(0,int(a)) :
    if ( i+1 != int(b[i])):
        result += 1
        
print(result)
        
    return answer
```

입력받을때 input()보다 sys.stdin.readlines()를 쓰는게 속도가 더 빠르다고 한다.

간단한 문제였는데 자료형때문에 오래 걸렸다 ㅜㅜ

* 채점 결과

성고응!




# **Day02-2_X보다 작은 수**

* 문제

https://www.acmicpc.net/problem/10871

<img width="571" alt="2-2_problem" src="https://user-images.githubusercontent.com/29175001/51031414-e11a5380-15df-11e9-8593-c9917a12b403.png">

* 내가 작성한 코드

```Python3

a,b = map(int, input().split())
c =input().split()

for i in range(a):
    if b > int(c[i]):
        print(int(c[i]), end=' ')
    
```
> split의 결과를 매번 int로 변환해주려니 귀찮기때문에 map을 함께 사용하면 된다.

map에 int와 input().split()을 넣으면 split의 결과를 모두 int로 변환해준다(실수로 변환할 때는 int 대신 float) 

ex) 

변수1, 변수2 = map(int, input().split())

변수1, 변수2 = map(int, input().split('기준문자열'))

> 출력값을 이어서 출력하려면 end =' '


* 채점 결과

성고응
