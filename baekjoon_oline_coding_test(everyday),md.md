# 1075-나누기

## 문제

두 정수 N과 F가 주어진다. 지민이는 정수 N의 가장 뒤 두 자리를 적절히 바꿔서 N을 F로 나누어 떨어지게 만들려고 한다. 만약 가능한 것이 여러 가지이면, 뒤 두 자리를 가능하면 작게 만들려고 한다.

예를 들어, N=275이고, F=5이면, 답은 00이다. 200이 5로 나누어 떨어지기 때문이다. N=1021이고, F=11이면, 정답은 01인데, 1001이 11로 나누어 떨어지기 때문이다.

## 입력

첫째 줄에 N, 둘째 줄에 F가 주어진다. N은 100보다 크거나 같고, 2,000,000,000보다 작거나 같은 자연수이다. F는 100보다 작거나 같은 자연수이다.

## 출력

첫째 줄에 마지막 두 자리를 모두 출력한다. 한자리이면 앞에 0을 추가해서 두 자리로 만들어야 한다.

```python
N = 2000018283
F = 88

a = str(N) # a를 str로 변환

b = a[-2:] # b를 문자열로 변환해 준다음에 마지막 두자리 수를 뽑아낸다.

c = 99-int(b)

d = N - int(b) # d값은 뒤에 두자리수가 00 
e = N + c # e값은 뒤에 두자리수가 99

min = [] # for 문을 통해 00부터 시작해서 주어진 정수까지 나머지가 0인 값을 추출한다.
for i in range(d, e):
  if i % F == 0:   
    min.append(i)

f = str(min[0]) # d에 첫번째 수를 뽑아준 다음

g = f[-2:] # e에 마지막

print(g)
```