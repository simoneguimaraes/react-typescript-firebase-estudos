## React, Firebase & TypeScript

- [ReactJs](#react)
- [Firebase](#firebase)
- [TypeScript](#typescript)

Referências: 
- [Fonte](https://app.rocketseat.com.br/node/mission-react-js?fbclid=IwAR0QJRwQOXh3XIs9qYirdp_2SW5pn8SKyEpb823zl3h__3h85DmsuNpy6qQ)
- [Whimsical](https://whimsical.com/): aplicação web para criação de Flowchart

## <a name="react"></a>ReactJs
### Biblioteca JavaScript para criar interfaces de usuário em aplicações front-end.
- Exemplos de Aplicações que usam React: Notion, Figma
- Com duas aplicações, é possível distribuir as responsabilidades: 

#### Aplicação 1: Servidor (back-end)
- Tecnologias: Node.js, python, ...
- Vai lidar com as regras de negócio, autenticação, banco de dados - parte funcional da aplicação

#### Aplicação 2: Browser (front-end)
- Tecnologias: React, Angular, Vue
- Contém todo o HTML, CSS e JS
- Vai interagir com o servidor, buscar dados - transformar a estrutura de dados em visualização

### SPA (Single Page Application)

- Na versão tradicional, voce precisava retornar todo o HTML com os dados dos contatos, por exemplo (50 KB)

- Na SPA, voce consegue retornar apenas o arquivo com os dados dos contatos (JSON) (10 KB)
- Para transacionar dados entre o front-end e o back-end, usa-se o formato JSON (JavaScript Object Notation)
```
[{ nome: 'Lucas Lima', idade: 28, cidade: 'São Paulo'}]
```

#### A SPA é o index.html
- É a pagina que recebe todas as informações.
- A interface da aplicação vai ser construída no Javascript.
- 
### Iniciando no React
- Ferramenta: creat-react-app
- Comando: sudo yarn create react-app talktome --template typescript



## <a name="firebase"></a>Firebase
### Backend as a Service do Google
Fornecer funcionalidades como: autenticação, sistema de gerenciamento de banco de dados

## <a name="typescript"></a>TypeScript
- TypeScript é uma linguagem de programação fortemente tipada que se baseia em JavaScript, oferecendo melhores ferramentas em qualquer escala.
- Ele já te indica possíveis caminhos, facilita o desenvolvimento e reduz os erros 
- Ex: sugere que 'user.city' não existe.
```
type User = { 
name: string;
address: {
  city: string;
  state: string;
  }
}  

function showWelcomeMessage(user: User) {
  return `Welcome ${user.name} - ${user.address.city}.`
}
```
-  Se voce passar a informacao em um formato que ele nao reconhece, ele já te mostra o erro de tipo (ex: troca de number por string)
```
showWelcomeMessage({
  name: Lucas
}) 
```
-  Mostra que está faltando informação (ex: falta da informação Estado)
```
showWelcomeMessage({
  name: 'Lucas',
  address: {
  city: 'São Paulo';
  }
}) 
```
## <a name="projeto"></a>Projeto
- O arquivo package.json indica quais são as dependências do projeto. São os códigos de terceiros que acoplamos ao nosso código.
- 
- 
