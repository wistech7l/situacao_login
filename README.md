# situacao_login

## Importante
Cada aluno terá uma branch especifica com seu nome, caso não tenha a sua criada no repositório, solicitar o professor.

## Iniciando

1) Realizar clone do repositório na maquina
2) `git fetch`
3) `git checkout seu_nome`
4) Alterar os `title` das páginas `login.php` e `bemvindo.php`
5) Realizar `commit` com as alterações na sua respectiva branch 

6) Crie um [Pull Request](https://github.com/wistech7l/situacao_login/compare) da sua branch para `main`
`base:main` <- `compare: sua_branch`


Em seguida o aluno deverá resolver a situação da seguinte maneira

## 1) 
Será necessário construir um banco de dados e uma tabela com nome `users`

a tabela deverá conter as seguites colunas 
* 1) *id:* chave primária, inteiro, AUTO_INCREMENT
* 2) *login:* varchar(50)
* 3) *password:* varchar(100)
* 4) *nome:* varchar(100)
* 5) *tipo:* inteiro

Após criada a tabela utilizar o seguinte comando SQL:

``` SQL
INSERT INTO users (login, password, nome, tipo) VALUES ('admin', '21232f297a57a5a743894a0e4a801fc3', 'Administrador', 1);
```


## 2) 
A página de login enviar uma requisição `POST` para `lib\valida.php`
Na valida.php deverá verificar o login, password e consultar no banco de dados se o login e senha existem e estão corretos.

_Obs.: lembrando que o password deverá ser convertido para `md5`._

Caso o login e password estejam corretos redirecionar o usuário para a página `bemvindo.php` e em caso de erro redirecionar para página de `login.php?error=`contatenado com uma mensagem de error.

## 3)

Criar as configurações do banco de dados utilizando o arquivo `.env` para conectar ao banco de dados. 

## 4) TESTES

Veifique se já contem a PR da sua branch 
_item 6_ da [lista](https://github.com/wistech7l/situacao_login#iniciando) 

Para testar se está tudo ok, basta realizar o commit na sua branch verificar se houve o deploy completo
no [GitHub Actions](https://github.com/wistech7l/situacao_login/actions).

Em seguida depois acessar: 
`http://wistech.epizy.com/<sua_branch>`

_Ex.: http://wistech.epizy.com/main/_

## Referências

* Biblioteca dotenv: https://github.com/vlucas/phpdotenv

* GitHub da concessionária: https://github.com/wistech7l/Crud_Concessionaria