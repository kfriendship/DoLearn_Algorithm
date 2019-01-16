# **Day03-1_네 수**

* 문제

https://www.acmicpc.net/problem/10824

<img width="523" alt="3-1_problem" src="https://user-images.githubusercontent.com/29175001/51032638-22146700-15e4-11e9-8e04-11f491022681.png">




* 내가 작성한 코드
```Python3
a,b,c,d = input().split()
print(int(a+b)+int(c+d))
```

GOOD !!!

* 채점 결과

성고응!




# **Day03-2_상수**

* 문제

https://www.acmicpc.net/problem/2908


<img width="782" alt="3-2_problem" src="https://user-images.githubusercontent.com/29175001/51033209-f1353180-15e5-11e9-82cc-48f635db17f0.png">

* 내가 작성한 코드

```Python3
a,b=input().split()

if int(a[::-1])>int(b[::-1]) :
    print(a[::-1])
elif int(a[::-1])<int(b[::-1]) :
    print(b[::-1])
    
```
[::-1]은 문자를 거꾸로 바꿔준다. 

* 채점 결과

성고응
  
  
  
#### __<스터디 복습>__
  
 
* 다른 코드

```Python3
def my_reverse(arg):
    ret = ''
    length = len(arg)
    for i in range(length - 1, -1, -1):
        ret += arg[i]
    return ret


# python >= 2.5
def my_max(arg1, arg2):
    return arg1 if arg1 > arg2 else arg2


a, b = input().split()
a = my_reverse(a)
b = my_reverse(b)
mx = my_max(int(a), int(b))
print(mx)
    
```
  
최대값을 구하는 함수에서 삼항연산자 사용!
https://blueshw.github.io/2016/01/22/python-conditional-ternary-operator/ python 삼항연산자 개념
