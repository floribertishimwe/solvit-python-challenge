# solvit-python-challenge

# Challenge #1
The provided code stub will read in a dictionary containing key/value pairs of name:[marks] for a list of students. Print the average of the marks array for the student name provided, showing 2 places after the decimal.


# Example
## marks key value pairs are
- 'alpha':[20,30,40]
- 'beta':[30,50,70]
The query_name is 'beta'. beta's average score is
(30+50+70)/3=50.0

## Input Format
The first line contains the integer ```n```, the number of students' records. The next ```n```  lines contain the names and marks obtained by a student, each value separated by a space. The final line contains
#### query_name the name of a student to query.

# Constraints
``` 
2 <= n <= 10
0 <= marks i < 100
length of marks arrays = 3

```
### Output Format
```
3
Krishna 67 68 69
Arjun 70 98 63
Malika 52 56 60
Malika
```
### Sample Output 0
```
56.00
```
#### Explanation 0
```
Marks for Malika are {52, 56, 60} whose average is (52+56+60)/3 => 56
```
#### Sample Input 1
```
2
Harsh 25 26.5 28
Anurag 26 28 30
Harsh
```

#### Sample Output 1
```
26.50 
```
My Answer 
=========
n = int(input())
marks = {}
avg = 0
scores_sum = 0
for i in range(n):
    name, *mark = input().split()
    scores = list(map(float, mark))
    marks[name] = scores
   
query_name = input()
for i in marks[query_name]:
    scores_sum += i
    
avg = scores_sum/3
print("{:.2f}".format(avg))
