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


- 리스트 내 요소를 n개씩 순서대로 추출(2020카카오)
```
for step in range(1, len(n) // 2 + 1):
  prev = s[0: step]
  
  for j in range(step, len(n), step):
    if prev == s[j: j + step]:
      bla bla bla..
    else:
      prev = s[j: j + step]
```


- n x n 공간에서 90도 회전(2020카카오)
```
def rotate_a_matrix_by_90_degree(a):
        n = len(a)  # 행 길이
        m = len(a[0])  # 열 길이
        
        result = [[0] * n for _ in range(m)]
        
        for i in range(n):
            for j in range(m):
                result[j][n-i-1] = a[i][j]
                
        return result
```

- unpacking 기법
```
d = {'b': 2, 'a': 1}
li = [2, 1]

def func(a, b):
    print(a, b)

func(a=1, b=2)
func(*li)
func(**d)
```

- 향상된 for문
```
members = [
    ['이숙번', 'enuma', '통영'],
    ['이고잉', '오튜', '서울'],
    ['솔님', '솔앤유', '제주'],
]

for i in range(3):
    print(members[i])

for m in members:
    print(m[0], m[1], m[2])
    
for name, company, location in members:
    print(name, company, location)
```

- 사전형의 경우(items)
```
animals = {'cat': 1, 'dog': 2, 'sheep': 4, 'fish': 2}

for k, v in animals.items():
    print(k, v)
```

- enumerate
```
animals = ['cat', 'dog', 'sheep', 'fish']

for i in range(4):
    print(i, animals[i])

for i, e in enumerate(animals):
    print(i, e)
```

- zip함수
```
names = ['이숙번', '이고잉', '솔님']
company = ['enuma', '오튜', '솔앤유']

for i in range(len(names)):
    print(names[i], company[i])

for n, c in zip(names, company):
    print(n, c)
```

- 다익스트라 그래프 초반 구현
```
n, m = map(int, input().split())
graph=[[] for i in range(n + 1)]
distance = [-1] * (n + 1)

for _ in range(m):
  a, b = list(map(int, input().split()))
  graph[a].append(b)
```

- BFS구현(큐)
```
def BFS(graph, start, visited):
  q = deque([start])
  visited[start] = True

  while q:
    now = q.popleft()
    print(now, end = ' ')

    for connect in graph[now]:
      if visited[connect] == False
        q.append(connect)
        visited[connect] = True
```

- DFS구현(재귀함수)
```
def DFS(graph, start, visited):
  visited[start] = True
  print(start, end = ' ')

  for connect in graph[start]:
    if not visited[connect]:
      DFS(graph, connect, visited)
```

- 다익스트라 구현(BFS + 코스트)
```
def Dijkstra(start):
  q = []
  heapq.heappush(q, (0, start))
  distance[start] = 0

  while q:
    dist, now = heapq.popleft()
    if distance[now] < dist:
      continue

    for connect in graph[now]:
      cost = dist + connect[1]

      if distance[connect[0]] > cost:
        distance[connect[0]] = cost
        heapq.heappush(q, (cost, connect[0]))
```

- 플로이드워셜 구현
```
for k in range(1, n + 1):
  for a in range(1, n + 1):
    for b in range(1, n + 1):
      dist[a][b] = min(dist[a][b], dist[a][k] + dist[k][b])
```
