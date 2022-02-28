# 28.02.2022
Задача 1. 
a = input().split()
for i in range(0, len(a), 2):
    print(a[i])
Задача 2. 
s=input()
a=[int(s) for s in s.split()]
for i in a:
    if int(i)%2 == 0:
       print(i, end=' ')
Задача 3. 
print(len(list(i for i in map(int, input().split()) if i >= 0)))
Задача 4. 
a = [int(i) for i in input().split()]
for i in range(1, len(a)):
    if a[i] > a[i - 1]:
        print(a[i])
Задача 5. 
a = [int(i) for i in input().split()]
for i in range(1, len(a)):
    if a[i - 1] * a[i] > 0:
        print(a[i - 1], a[i])
        break
Задача 6. 
a = [int(i) for i in input().split()]
counter = 0
for i in range(1, len(a) - 1):
    # о боги, разве так можно писать?
    if a[i - 1] < a[i] > a[i + 1]:
        counter += 1
print(counter)
Задача 7. 
index_of_max = 0
a = [int(i) for i in input().split()]
for i in range(1, len(a)):
    if a[i] > a[index_of_max]:
        index_of_max = i
print(a[index_of_max], index_of_max)
Задача 8.
a=list(map(int, input().split()))
n=a[0]
count=0
for i in range(len(a)):
    if a[i]>0:
        count+=1
    if a[i]<n and a[i]>0:
        n=a[i]
if count>0:
    print(str(n))
Задача 9.
lst = list(filter(lambda x : x % 2, list(map(int, input().split()))))
print(min(lst) if lst else 0)
Задача 10.
a = [int(i) for i in input().split()]
x = int(input())
pos = 0
while pos < len(a) and a[pos] >= x:
    pos += 1
print(pos + 1)
Задача 11.
a = [int(i) for i in input().split()]
num_distinct = 1
for i in range(0, len(a) - 1):
    if a[i] != a[i + 1]:
        num_distinct += 1
print(num_distinct)
Задача 12.
s = list(input())
for i in reversed(s):
    print(i, end='')
Задача 13.
a = [int(i) for i in input().split()]
for i in range(1, len(a), 2):
    a[i - 1], a[i] = a[i], a[i - 1]
print(' '.join([str(i) for i in a]))
Задача 14.
a = [int(s) for s in input().split()]
index_of_min = 0
index_of_max = 0
for i in range(1, len(a)):
    if a[i] > a[index_of_max]:
        index_of_max = i
    if a[i] < a[index_of_min]:
        index_of_min = i
a[index_of_min], a[index_of_max] = a[index_of_max], a[index_of_min]
print(' '.join([str(i) for i in a]))
Задача 15.
a = [int(s) for s in input().split()]
k = int(input())
for i in range(k + 1, len(a)):
    a[i - 1] = a[i]
a.pop()
print(' '.join([str(i) for i in a]))
