# Jade

Site de venda de joias, com **cadastro e login**, catálogo por categoria, carrinho de compras e finalização do pedido. Projeto acadêmico de desenvolvimento web.

## Tecnologias

HTML · CSS · JavaScript · Node.js · Express · MySQL (com Docker) · bcrypt

## Funcionalidades

- **Cadastro com validações:** nome sem números ou caracteres especiais, e-mail com domínio, data de nascimento com maioridade e senha guardada com hash (bcrypt).
- **Login** com middleware de validação.
- **Catálogo** com produtos, categorias e página "ver mais".
- **Carrinho:** adicionar, atualizar a quantidade e remover itens.
- **Perfil:** consultar e editar os dados.
- **Finalização do pedido:** endereço e cartão, com validação dos campos (por exemplo, CVV e vencimento no formato MM/AAAA).

## Estrutura

```
backend/
  src/Controllers/   rotas de cada recurso
  src/Models/        acesso ao banco
  src/Middlewares/   validação do login
  init.sql           criação e carga inicial do banco
frontend/
  html/ css/ javascript/   telas do site
```

## Como rodar

Requisitos: Node.js e Docker.

```bash
cd backend
npm install
cp .env.example .env     # defina as variáveis do banco
docker run --name mysql -e MYSQL_ROOT_PASSWORD=<sua-senha> -p 3306:3306 -d mysql
# cria o banco com o init.sql
npm start
```

Depois abra `frontend/html/Telainicial.html` no navegador.

## Autor

Mayronn Gomes Viana.
