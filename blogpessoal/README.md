# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some Oxlint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the Oxlint configuration

If you are developing a production application, we recommend enabling type-aware lint rules by installing `oxlint-tsgolint` and editing `.oxlintrc.json`:

```json
{
  "$schema": "./node_modules/oxlint/configuration_schema.json",
  "plugins": ["react", "typescript", "oxc"],
  "options": {
    "typeAware": true
  },
  "rules": {
    "react/rules-of-hooks": "error",
    "react/only-export-components": ["warn", { "allowConstantExport": true }]
  }
}
```

See the [Oxlint rules documentation](https://oxc.rs/docs/guide/usage/linter/rules) for the full list of rules and categories.

Axios ---

HTTP: verbos - GET, POST, PUT e DELETE
Promises - utiliza funções assíncronas
Funções assíncronas -> permitem que tarefas mais demoradas, como requisições HTTP ou acesso ao 
banco de dados, sejam executadas em segundo plano
Promises -> É um objeto que representa o resultado futuro de uma operação assíncrona.
Estados da Promise:
pending (pendente) --> estado inicial, aguardando resolução;
fulfilled (resolvida) --> operação concluída com sucesso;
rejected (rejeitada) --> operação falhou;

Síntaxe (como criar uma promise):
new Promise (resolve, reject) => {
  //lógica da operação assíncrona
};

Async/Await
async: define uma função como assíncrona, permitindo o uso do await dentro dela.
await: pausa de execução da minha função até que a minha Promise seja resolvida ou mesmo rejeitada, retornando o resultado diretamente.

Biblioteca AXIOS: é uma biblioteca JavaScript de comunicação HTTP, baseada em Promise, que permite que desenvolvedores façam requisições para a sua própria API (backend da aplicação) ou para APIs de terceiros.

Como funciona o AXIOS?
URL: endereço do endpoint que será consumido
Método HTTP: GET, POST, PUT e DELETE
Cabeçalhos (Headers): por exemplo TOKEN JWT
Corpo da requisição (BODY): dados que serão enviados, se necessário.

Enviar requisição:
Node.js usando a biblioteca interna HTTP
Navegador: API-XMLHttpRequest

Métodos do Axios:

axios.get(url,options)
axios.post(url,data,options)

Consumo do Axios:

import axios from  "axios"

async function carregarPost(){
  try{
    const resposta = await axios.get("https://jsonplaceholder.typicode.com/posts");
    consolo.log(resposta.data);
  }catch(erro){
    console.error(erro);
  }
}


Interfaces Model

Model: arquivos TypeScript que definem o Modelo de Dados(data).
Service: são scripts TypeScript compostos por funções assíncronas.
Gerenciamento de Estado Global: processo de controlar e compartilhar estados(dados) que precisam ser acessados ou mesmo modificados por vários componentes da minha aplicação.

