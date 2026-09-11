# 📝 TIL — 2026-09-06

---

## 🗄️ SQL — Estudo e Prática

---

### Conceitos estudados

```sql
-- Filtros
SELECT * FROM tabela WHERE coluna = 'valor';

-- Agrupamento
SELECT coluna, COUNT(*) FROM tabela GROUP BY coluna;

-- Ordenação
SELECT * FROM tabela ORDER BY coluna DESC;

-- JOIN
SELECT a.nome, b.valor
FROM tabela_a a
JOIN tabela_b b ON a.id = b.id;

-- Subquery
SELECT * FROM tabela
WHERE valor > (SELECT AVG(valor) FROM tabela);
```

---

> *"SQL é a linguagem que faz os dados falarem."*
