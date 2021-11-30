## React & Firebase

- [ReactJs](#react)
- [Firebase](#firebase)


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
[{ nome: 'Diego Lima', idade: 26, cidade: 'São Paulo'}]
```
## <a name="firebase"></a>Firebase
### Backend as a Service do Google
Fornecer funcionalidades como: autenticação, banco de dados



