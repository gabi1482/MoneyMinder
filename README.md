# MoneyMinder

## Requisitos


- [ ] CRUD Movimentações 
- [ ] CRUD Categorias
- [ ] Dashboard
- [ ] Autenticação (varios usuários)

##Endpoints

##Categorias

`GET` /categoria
Lista todas as categorias cadastradas no sistema

**Codigos de Status**
`200` sucesso

---

`GET` /categoria/{id}
Retorna os detalhes de uma categoria com o `íd` informado.

**Codigos de Status**
`200` sucesso
`404` id nao encontrado

---

`POST`/categoria
Cadastrar uma nova categoria.

**Codigos de Status**
`201` criado com sucesso
`400` validação falhou (algum campo obrigatorio nao foi enviado, ou o tipo foi outro)

---

| campo | tipo | obrigatório | descrição
| ------|------|:-------------:|----------
| nome| string | sim | Um nome curto para identificar a categoria
| icone | sring | nao | Um nome do icone conforme biblioteca do material design


`DELETE` /categoria/{id}
Apaga a categoria com o ID informado.

**Codigos de Status**
`204` apagado com sucesso (sem conteudo para motrar)
`404` id nao encontrado

---

`PUT` /categoria/{id}
Altera a categoria com o ID informado.

| campo | tipo | obrigatório | descrição
| ------|------|:-------------:|----------
| nome| string | sim | Novo nome curto para identificar a categoria
| icone | sring | sim | Novo nome do icone conforme biblioteca do material design

**Codigos de Status**
`200` sucesso
`404` id nao encontrado
`400` validação falhou

-- no put ele tem que mandar todos os dados, independente se ele nao ira usar -- 

---

**Scheme**
```js
{
  "id": 1,
  "nome": "Alimentação",
  "icone": "fast-food"
}
```

