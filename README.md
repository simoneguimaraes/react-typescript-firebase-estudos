## React, TypeScript & Firebase

Índice
- [ReactJs](#react)
- [Conceitos do ReactJs](#conceitos-react)
- [TypeScript](#typescript)
- [Firebase](#firebase)

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

## <a name="conceitos-react"></a>Conceitos do ReactJs
### Componentes
- Um componente é uma função que devolve um HTML
- No React, tudo é componente
- Deixa a aplicação mais simples e fácil do usuário utilizar
- A Aplicação React (App) também é um compontene

### Named Export (ao invés de Export Default)
```
export function Button() {
  return (
    <button>Clique Aqui</button>
  )
}
```
Caso voce altere o nome do componente de 'Button' para 'OutlineButton', a importação no App vai dar erro, o que ajuda a prevenir bugs. 
```
import { OutlineButton } from './components/OutlineButton'
```

### Propriedade
- A propriedade no JSX funciona como o atributo no HTML.
- O texto do botão será inserido por meio da propriedade 'text' no componente:
```
function App() {
  return (
    <div>
      <Button text="Compre Já"/>
      <Button text="Clique Aqui"/>
      <Button text="Saiba Mais"/>
    </div>
  )
}
```

- Caso tenha vários botões com textos diferentes, voce precisará criar uma tipagem ('type') no componente por causa do TypeScript:
- As chaves {} executam o código da variável
```
type ButtonProps = {
  text: string 
}
export function Button(props: ButtonProps) {
  return (
    <button>{props.text}</button>
  )
}
```
#### As propriedades (diferentemente dos atributos do HTML) podem receber qualquer tipo de informação do Javascript.
- Number:
```
function App() {
  return (
    <div>
      <Button text={1} />
    </div>
  )
}
```
```
type ButtonProps = {
  text: number 
}
```
- Array:
```
function App() {
  return (
    <div>
      <Button text={['1', '2']}/>
    </div>
  )
}
```
```
type ButtonProps = {
  text: Array<string> 
}
```
#### Children
```
function App() {
  return (
    <div>
      <Button>Clique Aqui<Button/>
    </div>
  )
}
```
```
type ButtonProps = {
  children: string
}
export function Button(props: ButtonProps) {
  return (
    <button>{props.children}</button>
  )
}
```
### Estado
- Serve para dar vida para a interface, ser manipulável pelo usuário
- Estado é uma informação mantida por um componente do React
- Quando a informação nao permenece com o mesmo valor durante todo o uso da aplicação, essa informação é mantida no Estado
- Essa informação vai ter o seu valor alterado pelo uso do usuário na aplicação 
- No React, as palavras são usadas em camelCase `<button onClick={}></button>`
- As chaves {} indicam que voce está colocando uma variável que foi definida em cima, como uma propriedade ou como um conteúdo.

#### Exemplo: Contador
Clicar no botão e a informaçao vai aumentar o valor (contador). Essa informação será mantida no Estado
```
export function Button() {
  let counter = 0;
  function increment(){
    counter += 1
  }
  
  return (
    <button onClick={increment}>{counter}</button>
  )
}
```
- O React consegue perceber que uma informação mudou para, então, ele mostrar essa nova informação em tela. Essa informação precisa ser um Estado.



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

## <a name="firebase"></a>Firebase
### Backend as a Service do Google
Fornecer funcionalidades como: autenticação, sistema de gerenciamento de banco de dados

## <a name="projeto"></a>Projeto
- O arquivo package.json indica quais são as dependências do projeto. São os códigos de terceiros que acoplamos ao nosso código.

```
let - let it change
const - constante
```

## Referências: 
- [Fonte](https://app.rocketseat.com.br/node/mission-react-js?fbclid=IwAR0QJRwQOXh3XIs9qYirdp_2SW5pn8SKyEpb823zl3h__3h85DmsuNpy6qQ)
- [Whimsical](https://whimsical.com/): aplicação web para criação de Flowchart
