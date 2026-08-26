# 📝 TIL — 2026-08-22

---

## 🐍 Python — Revisão de Conceitos Básicos e Avançados + Estrutura de Dados

---

### Conceitos básicos revisados

```python
# Tipos de dados
inteiro = 10
flutuante = 3.14
texto = "Felipe"
lista = [1, 2, 3]
dicionario = {"nome": "Felipe"}
tupla = (1, 2, 3)       # imutável
conjunto = {1, 2, 3}    # sem duplicatas

# Funções
def saudacao(nome):
    return f"Olá, {nome}!"

# List comprehension
quadrados = [x**2 for x in range(10)]

# Lambda
dobro = lambda x: x * 2
```

---

### Conceitos avançados revisados

```python
# Decorators
def meu_decorator(func):
    def wrapper():
        print("Antes")
        func()
        print("Depois")
    return wrapper

# Generators
def contar():
    yield 1
    yield 2
    yield 3

# *args e **kwargs
def func(*args, **kwargs):
    print(args, kwargs)
```

---

### Estruturas de Dados

| Estrutura | Característica | Exemplo Python |
|---|---|---|
| **Lista** | Ordenada, mutável | `[1, 2, 3]` |
| **Tupla** | Ordenada, imutável | `(1, 2, 3)` |
| **Dicionário** | Chave-valor | `{"a": 1}` |
| **Conjunto** | Sem duplicatas | `{1, 2, 3}` |
| **Pilha (Stack)** | LIFO | `lista.append() / pop()` |
| **Fila (Queue)** | FIFO | `collections.deque` |

---

> *"Rever o básico é sempre útil — é onde estão as bases de tudo que vem depois."*
