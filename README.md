# SWE_2021_41_2024_2_week_6
---
## Week 4 Assignment
- https://github.com/kkim-h/SWE_2021_41_2024_2_week_4
```python
def isHappy(n):
  flag = False
  cycle = []
  sum = 0
  n = str(n)
  l = len(n)
  for i in range(l):
      num = int(n[i])**2
      sum+=num
  while(True):
    if(sum==1):
      flag = True
      return flag
    else:
      n = str(sum)
      if(n in cycle):
        return False
      else:
        cycle.append(n)
        sum = 0
        l = len(n)
        for i in range(l):
          num = int(n[i])**2
          sum += num
  return flag
```
- To find a Happy Number, the input integer n is converted to a string to extract each digit\
Each digit is squared and summed, and the result is added to a cycle list\
A loop checks if the resulting sum exists in the cycle list;\
If it does, the function returns False\
If not, the operations are repeated until the result equals 1
