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
---
## Week 5 Assignment
> ```bash
> docker exec ossp-container cat /ets/os-release
> ```
> - __COMMANDLINE DESCRIPTION__  
This is the code that displays the OS information of my container  
You can see various details about OS, such as the type, version, and name of it
> - __OUTPUT__  
PRETTY_NAME="Ubuntu 24.04.1 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.1 LTS (Noble Numbat)"
VERSION
_CODENAME=noble
1D=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU CODENAME=noble
LOGO=ubuntu-logo

> ```bash
> docker exec ossp-container git --version
> ```
> - __COMMANDLINE DESCRIPTION__  
This is the code that displays the git version installed in the container  
My git version is 2.43.0
> - __OUTPUT__  
git version 2.43.0

> ```bash
> docker exec ossp-container python3 --version
> ```
> - __COMMANDLINE DESCRIPTION__  
This is the code that displays the python version installed in the container  
My python version is 3.12.3
> - __OUTPUT__  
Python 3.12.3

> ```bash
> docker inspect --format="{{ .HostConfig.Binds }}" ossp-container
> ```
> - __COMMANDLINE DESCRIPTION__  
This is the code that displays bind mount of the container  
In this case, it will show the directory of the bind mount
> - __OUTPUT__  
/Users/hyeok/Desktop/2024_2nd_ossp/ossp_host_dir:/mnt/ossp_host_container_dir
