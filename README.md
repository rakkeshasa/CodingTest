# 파이썬 코딩테스트 연습

- 리스트 형식으로 입력 받기

<pre><code>list(map(int, input().split()))
</code></pre>

- n x n 리스트 입력 받기
```
for i in range(n):
  li = list(map(int, input().list()))
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

steps = [(-2, - 1), (-1, -2), (1, -2), (2, -1), (2, 1), (1, 2), (-1, 2), (-2, 1)

for step in steps:
  bla bla~
```
