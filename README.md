# 파이썬 코딩테스트 연습

- 리스트 형식으로 입력 받기

<pre><code>list(map(int, input().split()))
</code></pre>

- 리스트에 이름과 숫자 받기
```
for i in range(n):
  data = input().split()
  array.append((data[0], int(data[1])))
```

- n x n 리스트 입력 받기
```
li = []
for i in range(n):
  li = list(map(int, input().list()))
```
또는
```
for i in range(n):
  li.append(list(map(int, input())))
```

- n x n 공간
```
dx = [0, 0, -1, -1]
dy = [-1, 1, 0, 0]
move = ['L', 'R', 'U', 'D']

for ~ :
  for ~ :
    if str == move[i]:
      nx = x + dx
      ny = y + dy
```

- n x n 공간 응용(체스판)
```
row = int(data[1])
col = int(ord(data[0])) - int(ord('a')) + 1
# ord(): 특정한 한 문자를 아스키 코드 값으로 변환

steps = [(-2, - 1), (-1, -2), (1, -2), (2, -1), (2, 1), (1, 2), (-1, 2), (-2, 1)]

for step in steps:
  bla bla~
```

- n x m 공간에 숫자로 채우기
```
n, m = map(int, input().split())
d = [[0] * m for _ in range(n)]
```

- 반복과 재귀의 차이
```
# 반복
def factorial_iterative(n):
  result = 1
  for i in range(1, n+1):
    result *= i
   return result
   
# 재귀
def factorial_recursive(n):
  if n <= 1:
    return 1
   
  return n * factorial_recursive(n - 1)
```


- 리스트 요소 한줄로 출력
```
for i in list:
  print(i, end='')
```
