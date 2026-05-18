### REACT ANOTAÇÕES

Criar o projeto com React e Next JS:

```bash
npx create-next-app@latest .
```

Rodar o projeto (acessá-lo em: http://localhost:3000/):

```bash
npm run dev
```

Síntaxe básica para criar uma arrow function:

```js
const Home = () => {
  return (
    <main>
      <h2>Bem-vindo!</h2>
    </main>
  );
};
export default Home;
```

Passar parâmetro para uma função (props) e utilizando children, ou seja, escrever algo dentro do objeto na view.
Criando-a no componente:

```js
import { ReactNode } from "react"; // se for utilizar children precisa importá-lo.

interface UserProps{ // interface remete a objeto em TypeScript.
    name: string;
    children?: ReactNode; // O "?" informa que o elemento do objeto não é obrigatório.
}

const User = ({name, children}: UserProps) => { // em TypeScript tudo precisa ser tipado, igualmente desta forma os parâmetros para esta função; como os parâmetros aqui estão dentro de um objeto o retorno também precisa ser um objeto, onde cada parâmetro é um item deste objeto.
    return (
        <div>
            <p>Usuário: {name}</p>
            {children && <div>{children}</div>}
        </div>
    )
}
export default User;
```

Depois, imprimindo-os na view:

```ts
import User from "../components/User";

const Home = () => {
  const userName = "Lucas";

  return (
    <main>
      <User name={userName}> /* o "name" aqui, ou seja, o nome do parâmetro, precisa ser igual ao que está na funcão chamada. */
        <p>Utilizando Children</p>
      </User>
      <h2>Bem-vindo!</h2>
    </main>
  );
};

export default Home;
```

Utilizando o useState, precisa informar o 'use client' para importá-lo:

```js
"use client"; // com use client o código roda no navegador.
import { useState } from "react";

const Home = () => {
  const [nameUser, setNameUser] = useState("Lucas"); // o valor padrão começa com "Lucas" e o tipo da variável "nameUser" depende do valor que for informado no useState, como foi informado "Lucas" é uma string.

  return (
    <main>
      <p>Nome: {nameUser}</p>
      <button onClick={() => setNameUser("Messi")}>Alterar</button> // sempre
      que for alterá-lo usa-se o setNameUser passando no parâmetro o novo valor
      que irá receber.
      <h2>Bem-vindo!</h2>
    </main>
  );
};

export default Home;
```

Utilizando o useEffect, ele realiza os comportamentos passados para ele caso o seu segundo parâmetro sofra quaisquer alterações:

```js
"use client";

import { useEffect, useState } from "react";

const Home = () => {
  const [productId, setProductId] = useState(1);
  const [nameId, setNameId] = useState("Notebook");
  const [priceId, setPriceId] = useState(1000);
  const [userId, setUser] = useState({
    id: 0,
    name: "Indefinido",
  });

  function searchProduct() {
    setNameId("Notebook atualizado");
    setPriceId(5000);
    setProductId(10);
    setUser({
      id: 10,
      name: "Lucas",
    });
  }

  useEffect(() => {
    searchProduct();
  }, [productId]); // Quando a página recarregar o useEffect será executado, após isto ele será chamado somente se productId sofrer alteração. Caso queira que ele rode somente quando a página carregar usa-se [].

  return (
    <main>
      <p>ID do produto: {productId}</p>
      <p>Nome do produto: {nameId}</p>
      <p>Preço do produto: {priceId}</p>
      <hr />

      <p>ID do usuário: {userId.id}</p>
      <p>Nome do produto: {userId.name}</p>
    </main>
  );
};

export default Home;
```

URL amigável (somente anotação, funcionalidade do Next JS, não do React):

```
 - O nome da pasta define a url (ex.: Dashboard/page.tsx => URL: /dashboard);
 - O nome do arquivo precisa ser um destes para funcionar:
 | - page.tsx => página;
 | - layout.tsx => layout;
 | - loading.tsx => loading;
 | - error.tsx => error.
 - O nome da constante do arquivo NÃO define a URL.

Resumo: o nome do diretório define a URL, contanto que o nome do arquivo seja um dos 4 citados acima, lembrando que eles precisam estar dentro do diretório src/app.
```

Formulário em React (para validá-lo):

```js
Para receber o evento:

const Exemplo = (e) => {
    e.preventDefault();
}

// Utilizar e: any => vulnerável, isto desliga o ts e ele não valida a tipagem deixando o método menos seguro.
// Utilizando e: React.FormEvent<HTMLFormEvent> => seguro, usa o ts e valida a tipagem, deixando o método seguro.
```

Mais anotações formulário em React e TypeScript:

```js
const Home = () => {

  interface formData {
    nameUser: string,
    emailUser: string
  };

  const [data, setData] = useState<formData>({
    nameUser: '',
    emailUser: ''
  });

  /* Recebe os dados dos campos do formulário: */
  /* Obs: "React.ChangeEvent<HTMLInputElement>" espera alguma alteração no evento (React.ChangeEvent) e essa alteração vem de um input de um formulário (<HTMLInputElement>). */
  const valueInput = (e: React.ChangeEvent<HTMLInputElement>) => setData({
    ...data, // isso copia tudo o que há em data, ou seja, é como se valueInput agora possuísse:
    // nameUser: '',
    // emailUser: '',
    // demais campos...

    // E aqui, e.target.name recebe o nome do campo do formulário, se o nome bater com o nome do objeto (de setData) ele o substitui, se não apenas adiciona mais um campo no objeto.
    [e.target.name]: e.target.value
  });


  /* "React.SubmitEvent<HTMLFormElement>" é uma tipagem ts que refere à um evento de um formulário (por estar usando TypeScript não é recomendado usar any.).*/
  const addUser = (e: React.SubmitEvent<HTMLFormElement>) => {

    e.preventDefault();

    // Manipular os dados recebidos:
    console.log("Nome" + data.nameUser);
    console.log("E-mail" + data.emailUser);
  }

  return(
    <main>
        <form onSubmit={addUser}>

          <label htmlFor="name">Nome:</label>
          <input type="text" name="nameUser" placeholder="Ex.: Lucas Vinicius" onChange={valueInput} /><br /><br />

          <label htmlFor="email">E-mail:</label>
          <input type="email" name="emailUser" placeholder="Ex.: exemplo@dominio.com" onChange={valueInput} /><br /><br />

          <input type="submit" value="Cadastrar" />

        </form>
    </main>
  )
}

export default Home;
```

Ligar o servidor em TS usando Express:

```bash
import express, {Request, Response} from "express";

// Utilizando o express como funcão pode-se usar a constante app para gerenciar rotas e ligar o servidor.
const app = express();

// Inicia o servidor na porta 8080.
app.listen(8080, () => {
    console.log("Servidor iniciado na porta 8080.");
});
```
