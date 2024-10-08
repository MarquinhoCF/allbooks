# AllBooks

O AllBooks é uma loja virtual que vende livros da Casa do Código. 
É um MVP que tá só começando e ainda tem muitas funcionalidades novas para serem desenvolvidas.

# JSONServer + JWT Auth

Essa é ma API Rest mockada, utilizando json-server e JWT.

## 🛠️ Instalação

```bash
$ npm install
$ npm run start-auth
```
## 🛠️ Como se registrar?

Você pode fazer isso efetuando uma requisição post para:

```
POST http://localhost:8000/public/registrar
```

Com os seguintes dados:


```
{
    "nome": "vinicios neves",
    "email": "vinicios@alura.com.br",
    "senha": "123456",
    "endereco": "Rua Vergueiro, 3185",
    "complemento": "Vila Mariana",
    "cep": "04101-300"
}
```

Repare que o e-mail é um campo único e usuários com e-mails duplicados não serão persistidos.

## 🛠️ Como fazer login?

Você pode fazer isso efetuando uma requisição post para:

```
POST http://localhost:8000/public/login
```

Com os seguintes dados:


```
{
  "email": "vinicios@alura.com.br",
  "senha":"123456"
}
```

Você vai receber um token no seguinte formato:

```
{
   "access_token": "<ACCESS_TOKEN>",
   "user": { ... dados do usuário ... }
}
```

## Autenticar próximas requests?

E então, adicionar este mesmo token ao header das próximas requisições:

```
Authorization: Bearer <ACCESS_TOKEN>
```

## Como inicializar um repositório Github

1) Criar um novo repositório no Github

2) Inicializar o repositório localmente com:

```
git init
```

3) Definir uma branch:

```
git branch -M main
```

4) Fazer a conexão do repositório local com o online

```
git remote add origin [URL_DO_REPOSITÓRIO_ONLINE]
```

## Troubleshooting

Caso você se depare com a seguinte mensagem ao tentar executar algum comando git, você precisará configurar a autenticação por token em sua conta.

```
Logon failed, use ctrl+c to cancel basic credential prompt.
remote: Support for password authentication was removed on August 13, 2021. Please use a personal access token instead.
remote: Please see https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/ for more information.
fatal: unable to access ‘<repositório Git>’: The request URL returned error: 403 
```

Para fazer essa configuração, você pode seguir este tutorial no nosso artigo sobre "Nova exigência do Git de autenticação por token, o que é e o que devo fazer?":
https://www.alura.com.br/artigos/nova-exigencia-do-git-de-autenticacao-por-token-o-que-e-o-que-devo-fazer

## Criando um commit

1) Checar status de commit:

```
git status
```

2) Adicionar os arquivos para o commit, você pode adicionar um a um a partir do nome do arquivo e extensão ou você pode usar "." para adicionar todos:

```
git add .
```

3) Criar um commit com uma mensagem, registrando as alterações:

```
git commit -m "Adiciona projeto inicial"
```

4) Checar as alterações:

```
git log
```

5) Enviar as alterações para o repositório online (origin) na branch (main):

```
git push origin main
```