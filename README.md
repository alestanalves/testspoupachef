# Poupachef - Job opportunity - Data Science
Coding tests - Poupachef

## Test 2
``` 
n = int(input("Qual termo você quer encontrar: "))
u=1 #ultimo numero
p=1 #penultimo numero

if (n==1) or (n==2): #Condição inicial do fibonacci é que o termo 1 e o termo 2 valem 1
    print("1")
else:
    for count in range(2,n): 
        termo = u + p  # O próximo número da série é sempre a soma dos dois anteriores
        p = u
        u = termo
        count += 1
    print(termo)
```

## Test 3

```
alfab = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"

def pegarcoluna(num):
    num_colu = 1
    min_range, max_range = 1, 26
    while num > max_range:
        num_colu += 1
        min_range = max_range
        max_range += len(alfab) ** num_colu

    chars = list()
    for _ in range(num_colu):
        intervalo = ((max_range - min_range + 1) // len(alfab))
        colu_pos = 0
        prev, curr = min_range, min_range + intervalo
        while num >= curr:
            colu_pos += 1
            prev = curr
            curr = prev + intervalo
        chars.append(alfab[colu_pos])
        num -= prev
        min_range, max_range = prev, curr

    return "".join(chars)

# Para testar coloque > pegarcoluna(1) o número é correspondente a coluna respectiva
``` 
