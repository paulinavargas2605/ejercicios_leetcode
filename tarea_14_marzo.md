## Solucion
<img width="1862" height="879" alt="image" src="https://github.com/user-attachments/assets/1ecb386d-b968-4ac0-9cd5-952689bd34e8" />

---
## Subproblema
dp[i]=máximo dinero que puedo robar hasta la casa i

---
## Recurrencia
Para cada casa 𝑖:

'''python
𝑑𝑝[𝑖]=max⁡(𝑑𝑝[𝑖−1],𝑑𝑝[𝑖−2]+𝑛𝑢𝑚𝑠[𝑖])

dp[i−1]: no robo la casa actual
dp[i−2]+nums[i]: robo la casa actual
'''

---
## Casos base
dp[0]=nums[0]
dp[1]=max(nums[0],nums[1])

---
## Complejidad
Para el tiempo O(n)
Para el espacio O(1)
