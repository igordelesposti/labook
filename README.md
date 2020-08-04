# Labook-backend

## Principais tecnologias/ferramentas utilizadas
* Node
* Typescript
* Arquitetura MVC
* MySQL (para construção do banco de dados)
* Knex (para conexão com o banco de dados)
* Express (para interação do código através do protocolo HTTP)
* Dotenv (para acessar informações sensíveis por meio de variáveis de ambiente)
* UUID (para geraração de id)
* Bcryptjs (para criptografar senhas)
* Jsonwebtoken (para gerar tokens de autenticação)

# Escopo
Desenvolver o backend de uma rede social, o LaBook, que nasceu como uma rede de alunos de universidades americanas, e agora parece que já tem um número aceitável de usuários (2 bilhões).

A rede social tem por objetivo de promover a conexão e interação entre seus mais diversos usuários. Os usuários podem criar posts de dois tipos ("evento" ou "normal), comentá-los e curti-los também. O desenvolvedor do frontend é bastante experiente e já preparou uma lista de todos os endpoints que serão necessários para o projeto:

## Endpoints obrigatórios

## Cadastrar

Para o cadastro nessa rede social, o usuário deve fornecer seu nome, seu e-mail e uma senha. Além disso, esse endpoint já tem que realizar o login do usuário, fornecendo seu token de autenticação no retorno da requisição.

## Logar

Para realizar o login, basta informar seu e-mail e a sua senha. O retorno deve conter o token de autenticação do usuário.

## Fazer amizade

Criar uma amizade é simples: basta receber o token de autenticação junto com o Id do usuário com o qual se deseja fazer amizade.

Uma amizade é uma "relação mútua": quando um usuário vira amigo de outro, esse outro "já é amigo" desse primeiro usuário (ou seja, o segundo usuário não precisa virar amigo do outro depois)

Não há a necessidade de "aceitar" uma amizade.

## Desfazer Amizade

Encerrar uma amizade segue o mesmo fluxo de fazer: com o token de autenticação e o id do usuário, já é possível realizar esse processo.

Observação: você deve retornar um erro caso o usuário tente desfazer uma amizade com alguém com quem não tem essa amizade registrada no banco!

## Criar post

O post deve ser criado, passando-se as informações de: foto, descrição, data de criação e tipo ("normal" ou "evento").

## Ver todo o Feed

O feed é composto por todos os posts dos amigos do usuário logado. Os posts devem ser retornado em ordem de criação: do mais recente ao mais antigo.

## Ver apenas um tipo de post do Feed

Esse endpoint deve receber um tipo ("normal" ou "evento") e retornar todos os posts que sejam do tipo especificado. Os posts devem ser retornado em ordem de criação: do mais recente ao mais antigo.


## Por fim, ressaltam-se dois fatos:

Você deve analisar e pensar quais são os endpoints que necessitam do token de autenticação
Lembre-se de que o Backend deve ser muito conciso. Isso significa que você deve prever a maior parte dos erros que possam acontecer e já se precaver contra eles. (Não se preocupe muito com essa parte, mas, se der tempo, foque nisso!)

## Desafios<br>
## Curtir Post

Essa requisição deve receber somente o id do post e retornar uma mensagem de sucesso ou erro. Lembre-se de que um usuário não pode curtir o mesmo post duas vezes.

## Descurtir Post

Essa requisição deve receber somente o id do post e retornar uma mensagem de sucesso ou erro. Lembre-se de que um usuário não pode descurtir um post que não tenha curtido

## Comentar Post

Recebendo o id do post e mensagem do comentário, o endpoint deve funcionar sem problemas. Um usuário pode, se quiser, comentar mais de uma vez o mesmo post.

## Implemente a funcionalidade que permita que o token de autenticação seja atualizado

Também conhecido como "Refresh Token", você deve implementar um endpoint que permita que o Frontend autalize o "acess token", caso este expire.

## Como rodar a aplicação
No terminal, clone o projeto:
```
$ git clone
```
Instale as dependências:
```
$ npm install
```

Execute a aplicação:
```
$ npm run start:dev
```

