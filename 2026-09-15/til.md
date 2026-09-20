# 📝 TIL — 2026-09-15

---

## 🍃 NoSQL e MongoDB

---

### O que é NoSQL?

Bancos de dados **não relacionais** que armazenam dados de formas diferentes do SQL tradicional.

| Tipo | Exemplo | Uso |
|---|---|---|
| Documento | MongoDB | Dados flexíveis, JSON |
| Chave-Valor | Redis | Cache, sessões |
| Colunar | Cassandra | Big Data |
| Grafo | Neo4j | Redes, relações |

---

### MongoDB na prática

```javascript
// Inserir documento
db.usuarios.insertOne({{
  nome: "Felipe",
  curso: "Ciência de Dados",
  habilidades: ["Python", "SQL", "Power BI"]
}})

// Buscar
db.usuarios.find({{ nome: "Felipe" }})

// Filtrar
db.usuarios.find({{ curso: "Ciência de Dados" }})

// Atualizar
db.usuarios.updateOne(
  {{ nome: "Felipe" }},
  {{ $set: {{ semestre: 2 }} }}
)

// Deletar
db.usuarios.deleteOne({{ nome: "Felipe" }})
```

---

### SQL vs NoSQL

| | SQL | NoSQL |
|---|---|---|
| Estrutura | Tabelas fixas | Documentos flexíveis |
| Schema | Rígido | Dinâmico |
| Escalabilidade | Vertical | Horizontal |
| Ideal para | Dados estruturados | Dados variados |

---

> *"NoSQL não substitui SQL — cada um tem seu lugar."*
