# SWE_2021_41_2024_2_week_6
## Week 4 Assigment
* Link: https://github.com/libru1014/SWE_2021_41_2024_2_week_4
```python
def isHappy(n):
  a = list()
  s = 0
  t = n
  result = False
  while True:
    s += (t % 10) ** 2
    while (t // 10) != 0:
      t = t // 10
      s += (t % 10) ** 2

    if s == 1:
      result = True
      break

    if s in a:
        break
    else:
        a.append(s)
        t = s
        s = 0

  return result
```
