## Solución
<img width="1850" height="816" alt="image" src="https://github.com/user-attachments/assets/15b4fadc-8a15-4efe-9122-7c3c7a3cc072" />

```python
class Solution:
    def eraseOverlapIntervals(self, intervals):
        # Ordenamos por el tiempo de finalización
        intervals.sort(key=lambda x: x[1])
        
        count = 0  # número de intervalos que eliminamos
        end = intervals[0][1]  # fin del primer intervalo
        
        for i in range(1, len(intervals)):
            # Si hay solapamiento
            if intervals[i][0] < end:
                count += 1  # eliminamos este intervalo
            else:
                end = intervals[i][1]  # actualizamos el final
        
        return count
```

---

## 2. Estrategia Greedy

Se usa un enfoque greedy donde primero se ordenan los intervalos por el que termina más rápido. Luego se van recorriendo y, si alguno se cruza con el actual, se elimina. La idea es quedarse siempre con el que deja más espacio para los siguientes. La complejidad es O(n log n) por el ordenamiento y luego O(n) por el recorrido.
