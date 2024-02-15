<h1>Sobre o Projeto</h1>
<p>Este é um projeto de sistema de enquete desenvolvido em Node.js utilizando TypeScript, Docker, Prisma, Redis e Fastify.

O sistema permite que os usuários criem enquetes, votem nelas e visualizem os resultados em tempo real. Ele utiliza WebSocket para atualizações em tempo real e armazenamento em cache com Redis para uma melhor performance.</p>

<br>

<h1>Pré-requisitos</h1>
<ul>
    <li>Node</li>
    <li>Docker</li> 
</ul>
</p>

Se você não tiver o [Node](https://nodejs.org/en) <strong>(Recomendável versão LTS)</strong> <br><br>
Se você não tiver o [Docker](https://docs.docker.com/engine/install/) <strong>(Escolha a versão conforme seu sistema operacional)</strong>
<br>

<h1>Instalação</h1>
<p>Para executar o projeto localmente, siga estas etapas no terminal:</p>

1 - Clone esse repositório em sua máquina local:

```
git clone https://github.com/CaioCesarMDS/PollProject.git
```

2 - Navegue até o diretório do projeto:

```
cd Polls
```

3 - Instale as dependências do projeto:

```
npm install
```

<br>

<h1>Execução</h1>
<p>Para testar o projeto, siga esses passos:</p>

1 - Inicie os contêineres Docker usando o Docker Compose:

```
docker-compose up -d
```
2 - Inicie o servidor:
```
npm run dev
```

3 - Utilize algum aplicativo/ferramenta de testes em APIs como o Postman ou Thunder Client, do Vscode:
<ul>
  <li> 3.1 - Testando a criação de enquetes:</li> <br>
  <p>Utilizando o método POST, coloque "http://localhost:3333/polls" no campo de URL da sua ferramenta de teste. No body da requisição, coloque um objeto com um título da enquete e as opções dela, abaixo um exemplo.</p>
   
    {
      "title": "Qual é a melhor IDE?",
      "options": ["VScode", "Spider", "JetBrains", "SublimeText"]
    }
    
  <li>3.2 - Visualizando informações da enquete:</li> <br>
  <p>Utilizando o método GET, coloque "http://localhost:3333/polls/pollId" no campo de URL da sua ferramenta de teste. O pollId deve ser criado no passo anterior.</p>

  <li> 3.1 - Testando a votação na enquete:</li> <br>
  <p>Utilizando o método POST, coloque "http://localhost:3333/polls/pollId/votes" no campo de URL da sua ferramenta de teste. No body da requisição, coloque um objeto com o pollOptionId. O pollOptionId deve ser pego com o passo anterior</p>
  
  <li> 3.1 - Visualizando o resultado da enquete:</li> <br>
  <p>Utilizando o request WebSocket, coloque "ws://localhost:3333/polls/pollId/results" no campo de URL da sua ferramenta de teste.
</ul>

<br>

<h1>Funcionalidades</h1>
<p>
  1 - Criar enquetes; 
  <br>
  <br>
  2 - Votar em enquetes;
  <br>
  <br>
  3 - Visualizar resultado em tempo real;
  <br>
</p>

<br>

<h1>Tecnologias</h1>
<p>Essas foram as principais tecnologias utilizadas no projeto:</p>

 <br>
<ul>
    <li><strong>Node</strong>: plataforma de código aberto que executa JavaScript do lado do servidor, permitindo a construção de aplicativos web escaláveis e de alto desempenho.</li>
    <br>
    <li><strong>Docker</strong>: plataforma que facilita a criação, implantação e execução de aplicativos em contêineres, permitindo que os aplicativos sejam executados de forma consistente em diferentes ambientes.</li>
    <br>
    <li><strong>TypeScript</strong>: linguagem de programação que estende o JavaScript adicionando tipagem estática opcional, permitindo o desenvolvimento de código mais seguro e com menos erros.</li>
    <br>
    <li><strong>Prisma</strong>: ORM (Object-Relational Mapping) moderno e poderoso para Node.js e TypeScript, que simplifica o acesso ao banco de dados e oferece uma API de banco de dados mais segura e expressiva.</li>
    <br>
    <li><strong>Redis</strong>: banco de dados em memória de chave-valor de código aberto, que é usado neste projeto para armazenamento em cache e gerenciamento de filas, proporcionando um desempenho rápido e escalabilidade.</li>
    <br>
    <li><strong>Fastify</strong>: estrutura web rápida e eficiente para Node.js, que é usada para lidar com solicitações HTTP no servidor, fornecendo baixa latência e alto desempenho.</li>
    <br>
    <li><strong>WebSocket</strong>: protocolo de comunicação bidirecional em tempo real, que é usado neste projeto para comunicação assíncrona em tempo real entre o servidor e os clientes, permitindo atualizações em tempo real dos resultados da enquete.</li>
    <br>
</ul>

<br>

<h1>Autor</h1>
<p>Esse Projeto foi desenvolvido por <strong>Caio Cesar 🔥</strong></p>
<br>

