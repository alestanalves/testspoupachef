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
