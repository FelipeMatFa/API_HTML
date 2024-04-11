# Como executar a API

### Crie o arquivo .env com as seguintes informações

```
# DEFINIÇÃO DA PORTA DO SERVIDOR EXPRESS
PORT =

# VARIÁVEIS DE CONEXÃO COM BANCO
DB_HOST = 
DB_USER =
DB_PASSWORD =
DB_DATABASE =
```

### Instale os pacotes npm 

* Faça isso executando no gitBash o seguinte comando

```
npm i express nodemon mysql2 dotenv cors
```

### Crie um arquivo gitignore

* Crie um arquivo chamado .gitignore e coloque o seguinte código

```
node_modules
.env
```

### Crie o seu banco de dados

* No mysql workbrench crie um banco de dados como o abaixo

```
reate database db_tasks;
use db_tasks;
 
drop database db_tasks;
 
create table tasks(
	id int auto_increment primary key,
    title varchar(255) not null,
    description text,
    create_at timestamp default current_timestamp
);
 
select * from tasks;
```

### Execute seu banco de dados

```
npm start
```