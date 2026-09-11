# 📝 TIL — 2026-09-08

---

## 🐍 Python — Estudo e Prática

---

### Conceitos estudados

```python
# Manipulação de listas
numeros = [1, 2, 3, 4, 5]
pares = [x for x in numeros if x % 2 == 0]

# Dicionários
pessoa = {"nome": "Felipe", "idade": 19}
pessoa["curso"] = "Ciência de Dados"

# Funções
def calcular_media(valores):
    return sum(valores) / len(valores)

# Tratamento de erros
try:
    resultado = 10 / 0
except ZeroDivisionError:
    print("Não é possível dividir por zero")

# Leitura de arquivo
with open("dados.csv", "r") as f:
    conteudo = f.read()
```

---

> *"Python é simples o suficiente para começar e poderoso o suficiente para nunca parar."*
