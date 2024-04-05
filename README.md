# Jade
<h1>Projeto de Desenvolvimento Web: Jade</h1>
 
<h2>Status: Done!🙌</h2>
 
<h3>O que é o Jade?</h3>

Jade é uma plataforma//um site de venda de joias!
Usamos um banco de dados populado com joias diversas para
dar vida ao site.
Explorando o projeto, o usuário pode criar sua conta através da opção Perfil. 
Após inserir um nome própio, e-mail, senha e data de nascimento válidos, o usuário poderá prosseguir com a adição de itens ao seu carrinho de compras, e, posteriormente finalizar a compra dos itens escolhidos, podendo determinar o endereço de entrega e método de pagamento (cartão ou boleto bancário). Existem endereços e cartões dispostos na tela de finalizar pedido como forma de exemplo, porém para finalizar a simulação de uma compra é necessário inserir um cartão e endereço válido.

**Todos os campos de cadastro são validados**
- Nome própio não pode ter caracteres especiais nem números
- E-mail deve conter um domínio (ex: @gmail.com)
- Senha é criptografada para um salthash antes de ser enviada ao BD
- Data de nascimento deve constar que o usuário tem mais de 18 anos
- Campos do formulário de Endereço não podem conter caracteres especiais e em alguns casos números.
- CVV do cartão de crédito não passa de 3 caracteres
- Data de vencimento do cartão não pode fugir do padrão MM/YYYY

>Como testar o Jade?🤔

Para utilizar e testar o projeto em sua máquina será necessário o NodeJS e o Docker.
O Docker irá reproduzir uma imagem do banco de dados, que por sua vez foi feito em MySQL.
NodeJS será necessário para rodar o servidor local e suas rotas para as requisições.

>Comandos

**É necessário NodeJS e Docker instalado no computador (Esse tutorial é apenas para o sistema operacional Windows)**

- Primeiro inicialize o docker, para que a sua IDE de desenvolvimento possa reconhecer os contâiners que serão criados ou os já existentes;
- Após isso dentro do terminal da IDE navegue até a pasta backend atráves do comando "cd _Nome_da_pasta_" ou caso deseje regrassar a pasta anterior "cd ..";
- Ao chegar na pasta backend inicialize o contâiner docker com o seguinte comando "docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql";
- Depois faça a criação do banco de dados com o seguinte comando "Get-Content "$(Get-Location)/init.sql" | docker exec -i mysql mysql -uroot -proot";
- por fim inicialize o NodeJS com o comando "npm start".

<h2>Agora aproveite o sistema Jade😊</h2>
