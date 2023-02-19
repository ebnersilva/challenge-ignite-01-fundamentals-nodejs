<img alt="GoStack" src="https://storage.googleapis.com/golden-wind/bootcamp-gostack/header-desafios.png" />

<h3 align="center">
  Ignite 2023 - Desafio: 01 - Fundamentos do Node.js
</h3>

<p align="center">“Não espere para plantar, apenas tenha paciência para colher”!</blockquote>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/ebnersilva/challenge-ignite-01-fundamentals-nodejs?color=%2304D361">

  <img alt="License" src="https://img.shields.io/badge/license-MIT-%2304D361">

  <a href="https://github.com/ebnersilva/challenge-ignite-01-fundamentals-nodejs/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/ebnersilva/challenge-ignite-01-fundamentals-nodejs?style=social">
  </a>
</p>

<p align="center">
  <a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#calendar-entrega">Entrega</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#memo-licença">Licença</a>
</p>

## :rocket: Sobre o desafio

Nesse desafio, você deve criar uma aplicação para treinar o que você aprendeu até agora no Node.js!

Essa será uma aplicação para armazenar tasks, que irá permitir a criação, listagem, atualização e remoção de tasks, também deve permitir que as tasks sejam finalizadas ou reabertas e para finalizar, deve conseguir importar arquivos CSV utilizando streams do Node.JS .

### Rotas da aplicação

- **`POST /tasks`**: A rota deve receber `title`, `description` dentro do corpo da requisição. Ao cadastrar uma nova task, ela deve ser armazenada dentro de um objeto no seguinte formato: `{ id: 'uuid', title: 'Desafio Node.js', description: 'description', completed_at: null, created_at: "data atual", updated_at: "data da última atualização" }`; Certifique-se que o ID seja um UUID.

- **`GET /tasks`**: Rota que lista todas as tasks, nessa rota existe um query param denominado: search onde o valor de search será pesquisado no title e description caso haja valor;

- **`PUT /tasks/:id`**: A rota deve alterar apenas o `título`, e `description` e `updated_at` da task que possua o `id` igual ao `id` presente nos parâmetros da rota;

- **`DELETE /tasks/:id`**: A rota deve deletar a task com o `id` presente nos parâmetros da rota;

- **`POST /tasks/:id/complete`**: A rota deve completar a task do `id` presente nos parâmetros da rota, a cada chamada dessa rota, se a task estava finalizada, ela deve ficar aberta novamente ou vice-versa;

### Importação do csv

Existe um arquivo chamado: "csv-stream-http-server.js" ao rodar esse arquivo com o node o mesmo se encarregará de ler o csv que está dentro do assets do projeto e fará a importação de todas as tasks que estão dentro do CSV

### Banco de dados

Ao iniciar a API um banco de dados DB.json é criado na pasta raiz do projeto, dessa forma todos os dados salvos estão sendo salvos nesse arquivo DB.json

## :memo: Licença

Esse projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE.md) para mais detalhes.

---

Feito com 💜 by Ebner Silva :wave: