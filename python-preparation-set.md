## [1. Say "Hello, World!" With Python](https://www.hackerrank.com/challenges/py-hello-world/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    print("Hello, World!")
```
## [2. Python If-Else](https://www.hackerrank.com/challenges/py-if-else/problem?isFullScreen=true)
```python
import math
import os
import random
import re
import sys

if __name__ == '__main__':
    n = int(input().strip())
    if n%2!=0:
        print("Weird")
    elif 2<=n<=5:
        print("Not Weird")
    elif 6<=n<=20:
        print("Weird")
    else:
        print("Not Weird")
```
## [3. Arithmatic Operators](https://www.hackerrank.com/challenges/python-arithmetic-operators/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a+b)
    print(a-b)
    print(a*b)
```
## [4. Python: Division](https://www.hackerrank.com/challenges/python-division/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    a = int(input())
    b = int(input())
    print(a//b)
    print(a/b)
```
## [5. Loops](https://www.hackerrank.com/challenges/python-loops/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    n = int(input())
    for i in range(n):
        print(i**2)
```
## [6. Write a function](https://www.hackerrank.com/challenges/write-a-function/problem?isFullScreen=true)
```python
def is_leap(year):
    leap = False
    if year%4==0:
        if year%100==0:
            if year%400==0:
                leap = True
        else:
            leap = True
    
    # Write your logic here
    
    return leap
```
## [7. Print Function](https://www.hackerrank.com/challenges/python-print/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    n = int(input())
    print(*range(1, n+1), sep="")
```
## [8. List Comprehensions](https://www.hackerrank.com/challenges/list-comprehensions/problem?isFullScreen=true)
```python
x = int(input())
y = int(input())
z = int(input())
N = int(input())
newlist = [[a,b,c] for a in range(x+1) for b in range(y+1) for c in range(z+1) if (a+b+c) != N]
print(newlist)
```
## [9. Find the Runner-Up Score!](https://www.hackerrank.com/challenges/find-second-maximum-number-in-a-list/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    n = int(input())
    arr = map(int, input().split())
    sorted_list = sorted(list(arr), reverse=True)
    for i in range(1, len(sorted_list)):
        if sorted_list[i]<sorted_list[0]:
            print(sorted_list[i])
            break
```
## [10. Nested Lists](https://www.hackerrank.com/challenges/nested-list/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    list1 = []
    list2 = []
    for _ in range(int(input())):
        name = input()
        score = float(input())
        list1.append([name, score])
        list2.append(score)
    list3 = sorted(list2)
    list4=[]
    for i in range(1, len(list3)):
        if list3[i]>list3[0]:
            for j in range(len(list1)):
                if list3[i] in list1[j]:
                    list4.append(list1[j][0])
            break
    list4.sort()
    for k in list4:
        print(k)
```
## [11. Finding the percentage](https://www.hackerrank.com/challenges/finding-the-percentage/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    n = int(input())
    student_marks = {}
    for _ in range(n):
        name, *line = input().split()
        scores = list(map(float, line))
        student_marks[name] = scores
    query_name = input()
    
    marks = student_marks[query_name]
    percentage = (sum(marks)/len(marks))
    print("{:.2f}".format(percentage))

```
## [12. Lists](https://www.hackerrank.com/challenges/python-lists/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    N = int(input())
    list1 = []
    for i in range(N):
        to_do = list(map(str, input().split()))
        command = to_do[0]
        
        if command == "insert":
            list1.insert(int(to_do[1]), int(to_do[2]))
        elif command == "remove":
            list1.remove(int(to_do[1]))
        elif command == "append":
            list1.append(int(to_do[1]))
        elif command == "sort":
            list1.sort()
        elif command == "pop":
            list1.pop()
        elif command == "reverse":
            list1.reverse()
        elif command == "print":
            print(list1)
        else:
            print("Invalid command")
```
## [13. sWAP cASE](https://www.hackerrank.com/challenges/swap-case/problem?isFullScreen=true)
```python
def swap_case(s):
    swp = ""
    for i in s:
        j = ord(i)
        if 65<= j <= 90:
            swp+=chr(j+32)
        elif 97<= j <= 122:
            swp+=chr(j-32)
        else:
            swp+=i
    return swp
```
## [14. String Split and Join](https://www.hackerrank.com/challenges/python-string-split-and-join/problem?isFullScreen=true)
```python
def split_and_join(line):
    a = line.split(" ")
    l = "-".join(a)
    return l
```
## [15. What's Your Name?](https://www.hackerrank.com/challenges/whats-your-name/problem?isFullScreen=true)
```python
def print_full_name(first, last):
    print(f"Hello {first} {last}! You just delved into python.")
```
## [16. Mutations](https://www.hackerrank.com/challenges/python-mutations/problem?isFullScreen=true)
```python
def mutate_string(string, position, character):
    l= list(string)
    l[position] = character
    l = "".join(l)
    return l
```
## [17. Find a string](https://www.hackerrank.com/challenges/find-a-string/problem?isFullScreen=true)
```python
def count_substring(string, sub_string):
    count=0
    for i in range(len(string)-len(sub_string)+1):
        if string[i:i+len(sub_string)] == sub_string:
            count+=1
    return count
```
## [18. String Validators](https://www.hackerrank.com/challenges/string-validators/problem?isFullScreen=true)
```python
if __name__ == '__main__':
    s = input()
    alnum = False
    alpha = False
    digit = False
    lower = False
    upper = False
    
    for i in s:
        if i.isdigit() == True:
            digit = True
            alnum = True
        elif i.islower() == True:
            lower = True
            alpha = True
            alnum = True
        elif i.isupper() == True:
            upper = True
            alpha = True
            alnum = True
              
    print(alnum)
    print(alpha)
    print(digit)
    print(lower)
    print(upper)
```
## [19. Text Wrap](https://www.hackerrank.com/challenges/text-wrap/problem?isFullScreen=true)
```python
def wrap(string, max_width):
    return textwrap.fill(string, max_width)
```
## [20. String Formatting](https://www.hackerrank.com/challenges/python-string-formatting/problem?isFullScreen=true)
```python
def print_formatted(number):
    l = len("{0:b}".format(number))
    for i in range(1, number+1):
        print("{0:{w}d} {0:{w}o} {0:{w}X} {0:{w}b}".format(i,w=l))
```
## [21. Detect Floating Point Number](https://www.hackerrank.com/challenges/introduction-to-regex/problem?isFullScreen=true)
```python
for i in range(int(input())):
    st = str(input())
    fl = False
    if st.count(".")==1:
        fr = "+-."
        nm = "0123456789"
        if st[0] in fr or st[0] in nm:
            r = st.find(".")
            if r != len(st)-1:
                for i in range(1, len(st)):
                    if st[i] not in nm and st[i] !=".":
                        fl = False
                        break
                    else:
                        fl = True
                        
    print(fl)
```