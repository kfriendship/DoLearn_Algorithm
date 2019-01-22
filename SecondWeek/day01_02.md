# **Day01_병합정렬**

* 문제

https://www.acmicpc.net/problem/1427

<img width="506" alt="2-day1" src="https://user-images.githubusercontent.com/29175001/51438213-832af180-1cec-11e9-9586-943483b994e8.png">




* 내가 작성한 코드
```Python3

a=input()
merge_list =[]
for i in range(0,len(a)):
	merge_list.append(int(a[i]))
	
def merge_sort(merge_list): ## 리스트 나누는 함수
	mid = len(merge_list)//2    ## 리스트 나누기
	left = merge_list[:mid]
	right = merge_list[mid:]
	
	left1 = merge_sort(left)  ##재귀 이용하여 나눈 것 또 나누기
	right1 = merge_sort(right)
	
	return merge(left1,right1)
	
def merge(left, right):  ##나눈부분 내림차순 정렬하는 함수
	a=0
	b=0
	sorted_list=[]
	
	while (a<len(left)) & (b<len(right)):
		if left[a]<right[b] :
			sorted_list.append(right[b])
			b+=1
		else:
			sorted_list.append(left[a])
			a+=1
			
	while (a<len(left)) :
		sorted_list.append(left[a])
		a+=1

	while (b<len(right)) :
		sorted_list.append(right[b])
		b+=1
		
	return sorted_list
	
for j in merge_sort(merge_list):
	print(j,end="")
        
```


* 채점 결과

성고응!  
  
  



# **Day02_퀵 정렬**

* 문제

문제는 위와 동일. (내림차순 정렬)


* 내가 작성한 코드

```Python3

a=input()
unsorted_list =[]
for i in range(0,len(a)):
	unsorted_list.append(int(a[i]))
	
def quick_sorted(arr):
    if len(arr) > 1:
        pivot = arr[len(arr)-1]
        left, mid, right = [], [], []
        for i in range(len(arr)-1):
            if arr[i] > pivot:
                left.append(arr[i])
            elif arr[i] < pivot:
                right.append(arr[i])
            else:
                mid.append(arr[i])
        mid.append(pivot)
        return quick_sorted(left) + mid + quick_sorted(right)
    else:
        return arr
		

for j in quick_sorted(unsorted_list):
	print(j,end="")
    
```

후...
