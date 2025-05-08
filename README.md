# 🛍️ API RESTful de Gerenciamento de Produtos

Esta é uma API simples desenvolvida com **Node.js** e **Express** para gerenciar produtos, permitindo criar, listar, editar e excluir registros. Ideal para fins de aprendizado ou como base para projetos maiores.

---

## 📌 Objetivo

Fornecer uma API REST básica com operações CRUD para produtos, com validações e mensagens de erro claras, pronta para ser testada com ferramentas como **Insomnia** ou **Postman**.

---

## 🚀 Tecnologias Utilizadas

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [body-parser](https://www.npmjs.com/package/body-parser)
- [express-validator](https://express-validator.github.io/)

---

## 🧰 Funcionalidades

- ✅ Listar todos os produtos
- ✅ Criar um novo produto
- ✅ Editar um produto existente
- ✅ Excluir um produto
- ✅ Validações nos dados de entrada

---

## 🔧 Instalação

1. **Clone o repositório:**

```bash
git clone https://github.com/ArafelD/api-produtos.git
cd api-produtos
```

2. **Instale as dependências:**

```bash
npm install
```

3. **Execute o servidor:**

```bash
node server.js
```

> A API estará disponível em `http://localhost:3000`

---

## 📬 Endpoints

### 1. `GET /produtos`

Retorna a lista de todos os produtos.

📤 Resposta:

```json
[
  {
    "id": 1,
    "nome": "Notebook",
    "descricao": "Notebook Dell",
    "preco": 3500.0
  }
]
```

---

### 2. `POST /produtos`

Cria um novo produto.

📥 Requisição:

```json
{
  "nome": "Mouse Gamer",
  "descricao": "Mouse com RGB",
  "preco": 120.00
}
```

📤 Resposta:

```json
{
  "id": 2,
  "nome": "Mouse Gamer",
  "descricao": "Mouse com RGB",
  "preco": 120.00
}
```

---

### 3. `PUT /produtos/:id`

Edita um produto existente.

📥 Requisição:

```json
{
  "nome": "Mouse Gamer Pro",
  "descricao": "Atualizado com sensor 4K",
  "preco": 180.00
}
```

---

### 4. `DELETE /produtos/:id`

Exclui o produto com o ID especificado.

📤 Resposta:

- `204 No Content`

---

## 🔒 Validações

Todos os campos são obrigatórios para criação e edição:

| Campo       | Regra                                   |
|-------------|------------------------------------------|
| `nome`      | obrigatório, mínimo de 3 caracteres      |
| `descricao` | obrigatório                              |
| `preco`     | obrigatório, número > 0                  |

📤 Exemplo de erro:

```json
{
  "erros": [
    {
      "msg": "O nome é obrigatório.",
      "param": "nome",
      "location": "body"
    }
  ]
}
```

---

## 🧪 Testando com Insomnia

Você pode usar o [Insomnia](https://insomnia.rest/) para testar os endpoints. Crie requisições com os seguintes métodos:

- `GET http://localhost:3000/produtos`
- `POST http://localhost:3000/produtos`
- `PUT http://localhost:3000/produtos/1`
- `DELETE http://localhost:3000/produtos/1`

Se quiser, posso enviar uma **coleção Insomnia JSON pronta** para importar.

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 🙋‍♂️ Autor

Desenvolvido por **Rafael Dias**  
💼 GitHub: [github.com/ArafelD](https://github.com/ArafelD)