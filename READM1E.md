Clone o Repositório

```bash
git clone https://github.com/DKMA-Tecnologia-e-Marketing/AM_Tech.git
```

Vá para o backend e crie um arquvio .env, dentro do aquivo cole os dados abaixo:

Fill `.env` file with environment variables:

```bash
NODE_ENV=DEVELOPMENT      
BACKEND_URL=http://localhost
FRONTEND_URL=http://localhost:3000
PROXY_PORT=8080
PORT=8080

DB_HOST=127.0.0.1
DB_DIALECT=mysql
DB_USER=amtechUse
DB_PASS=P@ssword1
DB_NAME=am_tech

JWT_SECRET=3123123213123
JWT_REFRESH_SECRET=75756756756

EMAIL_HOST=smtp.gmail.com
PORT_HOST=465
MAIL_USER=amtechdkma@gmail.com
MAIL_PASS='diefolpqppfgybwn'

REDIS_HOST=127.0.0.1
REDIS_PORT=6379
REDIS_PASSWORD=123456


```
Abra o terminal do computador para criar o banco de dados :

```bash
sudo mysql
coloque a senha do seu computador
crie o banco
Create database am_tech;
verifique se foi criado o banco
Show databases;
crie o usuario e snha
CREATE USER 'amtechUse'@'localhost' IDENTIFIED BY 'P@ssword1';
de as permissões
GRANT ALL PRIVILEGES ON am_tech.* TO 'amtechUse'@'localhost';
FLUSH PRIVILEGES;



Instale as dependencias do backend  build app, run migrations and seeds:

```bash
npm install
npm run build
npx sequelize db:migrate
npx sequelize db:seed:all
```

Start backend:

```bash
npm start
```

Abra um novo termnal e vá para o frontend, na pasta do frontend crie outro aquivo .env igual fez no backend mas cole o aquivo abaixo:

```bash

REACT_APP_BACKEND_URL = http://localhost:8080/
```

Depois de fazer o passo acima, rode o comando de install no frontend e depois start 

```bash
npm install -f
npm start
```
Depois é so ir para a branch mais atualiza e dar um git pull origin e o nome da branch