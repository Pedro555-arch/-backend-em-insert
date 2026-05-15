# Evidências — Partes 1 e 2
 
## Identificação
 
Nome do aluno: Pedro Henrique Ribeiro Pereira
Turma: 3°EM-B
Data: 15-0502026
 
---
 
## 1. Link do meu repositório GitHub
 
Cole abaixo o link do seu repositório:
 
https://github.com/Pedro555-arch/-backend-em-insert
 
---
 
# Parte 1 — Clonagem, configuração e publicação
 
## 2. Comprovação do remote configurado
 
Execute no terminal:
 
git remote -v
 
Cole abaixo o resultado:
 origin  https://github.com/Pedro555-arch/-backend-em-insert.git (fetch)
origin  https://github.com/Pedro555-arch/-backend-em-insert.git (push)
cole aqui o resultado do comando
 
---
 
## 3. Comprovação dos commits
 
Execute no terminal:
 
git log --oneline
 
Cole abaixo o resultado:
 dd269db (HEAD -> main, origin/main, origin/HEAD) Atualiza rota raiz com pesquisa por data
7a0b4da Configura projeto insert
4ffe899 Rename project section from 'Parte 2' to 'Insert'
ea330b7 Inserção de 3 registros de leituras
dba6585 Filtra Leituras por data
ba38040 Update DB_PASSWORD in .env-exemplo
3a9d2b0 Commit inicial
(END)
cole aqui o resultado do comando
 
O resultado deve mostrar commits como:
 
Configura projeto insert
Atualiza rota raiz com pesquisa por data
 
---
 
## 4. Comprovação do status do projeto
 
Execute no terminal:
 
git status
 
Cole abaixo o resultado:
 Untracked files:
  (use "git add <file>..." to include in what will be committed)
        EVIDENCIAS_PARTES_1_E_2.md

nothing added to commit but untracked files present (use "git add" to track)
cole aqui o resultado do comando
 
---
 
## 5. Comprovação da execução do projeto
 
Execute no terminal:
 
npm run dev
 
Cole abaixo a mensagem exibida no terminal:
 backend-em-parte-2@1.0.0 dev
> nodemon src/server.js

[nodemon] 3.1.14
[nodemon] to restart at any time, enter `rs`
[nodemon] watching path(s): *.*
[nodemon] watching extensions: js,mjs,cjs,json
[nodemon] starting `node src/server.js`
Banco db_em já existe.
Conexão com PostgreSQL realizada com sucesso.
Tabela sincronizada com sucesso.
Tabela leituras já possui dados.
Servidor rodando em http://localhost:3000
cole aqui o resultado do terminal
 
---
 
## 6. Teste da rota de todas as leituras
 
Acesse no navegador:
 
http://localhost:3000/api/leituras
 
Cole abaixo parte do resultado exibido:
 [{"id":1,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T11:00:00.000Z","temperature_c":24.5,"humidity_pct":72.1},{"id":2,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T12:00:00.000Z","temperature_c":25.8,"humidity_pct":69.4},{"id":3,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T13:00:00.000Z","temperature_c":27.2,"humidity_pct":65.8},{"id":4,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-02T11:00:00.000Z","temperature_c":23.9,"humidity_pct":74.3},{"id":5,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-02T12:00:00.000Z","temperature_c":25.1,"humidity_pct":70.6},{"id":6,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-02T13:00:00.000Z","temperature_c":26.7,"humidity_pct":67.2}]
cole aqui parte do resultado da rota /api/leituras
 
---
 
# Parte 2 — Alteração da rota raiz e pesquisa por data
 
## 7. Comprovação da rota raiz alterada
 
Acesse no navegador:
 
http://localhost:3000/
 
Cole abaixo o resultado exibido:
 
cole aqui o resultado da rota /
 
O resultado deve mostrar as rotas disponíveis, incluindo:
 
GET /api/leituras
[
  {
    "id": 1,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-01T11:00:00.000Z",
    "temperature_c": 24.5,
    "humidity_pct": 72.1
  },
  {
    "id": 2,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-01T12:00:00.000Z",
    "temperature_c": 25.8,
    "humidity_pct": 69.4
  },
  {
    "id": 3,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-01T13:00:00.000Z",
    "temperature_c": 27.2,
    "humidity_pct": 65.8
  },
  {
    "id": 4,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-02T11:00:00.000Z",
    "temperature_c": 23.9,
    "humidity_pct": 74.3
  },
  {
    "id": 5,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-02T12:00:00.000Z",
    "temperature_c": 25.1,
    "humidity_pct": 70.6
  },
  {
    "id": 6,
    "station_id": "EM-ARACATUBA-01",
    "timestamp": "2026-04-02T13:00:00.000Z",
    "temperature_c": 26.7,
    "humidity_pct": 67.2
  }
]
GET /api/leituras/data/2026-04-01
 {"dataPesquisada":"2026-04-01","total":3,"leituras":[{"id":1,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T11:00:00.000Z","temperature_c":24.5,"humidity_pct":72.1},{"id":2,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T12:00:00.000Z","temperature_c":25.8,"humidity_pct":69.4},{"id":3,"station_id":"EM-ARACATUBA-01","timestamp":"2026-04-01T13:00:00.000Z","temperature_c":27.2,"humidity_pct":65.8}]}
---
 
## 8. Teste da rota de pesquisa por data
 
Acesse no navegador:
 
http://localhost:3000/api/leituras/data/2026-04-01
 
Cole abaixo parte do resultado exibido:
 
cole aqui parte do resultado da rota /api/leituras/data/2026-04-01
 {
  "dataPesquisada": "2026-04-01",
  "total": 3,
  "leituras": [
    {
      "id": 1,
      "station_id": "EM-ARACATUBA-01",
      "timestamp": "2026-04-01T11:00:00.000Z",
      "temperature_c": 24.5,
      "humidity_pct": 72.1
    },
    {
      "id": 2,
      "station_id": "EM-ARACATUBA-01",
      "timestamp": "2026-04-01T12:00:00.000Z",
      "temperature_c": 25.8,
      "humidity_pct": 69.4
    },
    {
      "id": 3,
      "station_id": "EM-ARACATUBA-01",
      "timestamp": "2026-04-01T13:00:00.000Z",
      "temperature_c": 27.2,
      "humidity_pct": 65.8
    }
  ]
}
---
 
## 9. Teste de data inválida
 
Acesse no navegador:
 
http://localhost:3000/api/leituras/data/01-04-2026
 
Cole abaixo o resultado exibido:
 {"mensagem":"Formato de data inválido. Use o formato YYYY-MM-DD.","exemplo":"2026-05-11"}
cole aqui o resultado da validação de data inválida
 {
  "mensagem": "Formato de data inválido. Use o formato YYYY-MM-DD.",
  "exemplo": "2026-05-11"
}
---
 
## 10. Código alterado na rota raiz
 
Cole abaixo o trecho da rota raiz alterada no arquivo src/server.js:
 app.get('/', (req, res) => {
  return res.json({
    mensagem: 'API Estação Meteorológica',
    descricao: 'API para consulta de leituras meteorológicas armazenadas no PostgreSQL.',
    rotasDisponiveis: {
      listarTodasAsLeituras: 'GET /api/leituras',
      pesquisarLeiturasPorData: 'GET /api/leituras/data/2026-04-01',
    },
    formatoDaData: 'YYYY-MM-DD',
    exemploDeUso: 'http://localhost:3000/api/leituras/data/2026-04-01',
  });
});
cole aqui o código da rota app.get('/')
  require('dotenv').config();

const express = require('express');
const cors = require('cors');

const ensureDatabaseExists = require('./loaders/ensureDatabase');
const sequelize = require('./config/database');
const seedLeiturasIfEmpty = require('./loaders/seedLeituras');
const leiturasRoutes = require('./routes/leiturasRoutes');

const app = express();
const PORT = Number(process.env.PORT || 3000);

app.use(cors());
app.use(express.json());

app.get('/', (req, res) => {
  return res.json({
    mensagem: 'API Estação Meteorológica',
    descricao: 'API para consulta de leituras meteorológicas armazenadas no PostgreSQL.',
    rotasDisponiveis: {
      listarTodasAsLeituras: 'GET /api/leituras',
      pesquisarLeiturasPorData: 'GET /api/leituras/data/2026-04-01',
    },
    formatoDaData: 'YYYY-MM-DD',
    exemploDeUso: 'http://localhost:3000/api/leituras/data/2026-04-01',
  });
});

app.use('/api', leiturasRoutes);

async function startServer() {
  try {
    await ensureDatabaseExists();
    await sequelize.authenticate();
    console.log('Conexão com PostgreSQL realizada com sucesso.');

    await sequelize.sync();
    console.log('Tabela sincronizada com sucesso.');

    await seedLeiturasIfEmpty();

    app.listen(PORT, () => {
      console.log(`Servidor rodando em http://localhost:${PORT}`);
    });
  } catch (error) {
    console.error('Erro ao iniciar a aplicação:', error.message);
  }
}

startServer();

---
 
## 11. Observação final
 
Consegui clonar, configurar, executar, testar, alterar a rota raiz, testar a pesquisa por data e publicar o projeto no meu GitHub.