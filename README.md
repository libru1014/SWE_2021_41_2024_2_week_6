# SWE_2021_41_2024_2_week_6
---
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
* Explanation: First, get the sum of the squares of each digits. Second, repeat it. If the sum is 1, return true. Otherwise, store the sum. If the sum has already existed, return false, because it entered into the cycle.
---
## Week 5 Assignment
> ```bash
> docker exec <your container> cat /etc/os-release
> ```
>> Explanation: Print container's os.  
>> Output  
>> PRETTY_NAME="Ubuntu 24.04.1 LTS"  
>> NAME="Ubuntu"  
>> VERSION_ID="24.04"
>> VERSION="24.04.1 LTS (Noble Numbat)"
>> VERSION_CODENAME=noble  
>> ID=ubuntu
>> ID_LIKE=debian
>> HOME_URL="https://www.ubuntu.com/"
>> SUPPORT_URL="https://help.ubuntu.com/"
>> BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
>> PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
>> UBUNTU_CODENAME=noble  
>> LOGO=ubuntu-logo
> ```bash
> docker exec <your container> git --version
> ```
>> Explanation: Print container's git version.    
>> Output  
>> git version 2.43.0
> ```bash
> docker exec <your container> python3 --version
> ```
>> Explanation: Print container's python3 version.  
>> Output  
>> Python 3.12.3
> ```bash
> docker inspect --format="{{ .HostConfig.Binds }}" <your container>
> ```
>> Explanation: Print path of mounted directory of the specified container.  
>> Output  
>> [./ossp_host_dir:/mnt/ossp_container_dir]
