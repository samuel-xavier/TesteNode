Teste Node para rodar no UBUNTU - EC2 - AWS

- Criar o diretorio

- Criar o projeto:
  - no diretório: yarn init -y

- Instalar o express
  - no diretório: yarn add express

- Atraves do VsCode, incluir o arquivo index.js
*************************************************
const { request, response } = require('express');
const express = require('express');

const app = express();

app.use(express.json());

app.get('/',(request,response)=> {
    return response.json({message:'Server UBUNTU is up'});
})

app.post('/teste',(request,response)=>{
    const {name,date} = request.body;

    return response.json({name,date});

})
*************************************************

- Para testar:
  executar: node index.js
  verificar no explorer: http://localhost:3333

- Se necessário, apagar o diretorio node_modules. Para restaurar, rodar o npm istall
app.listen(3333)