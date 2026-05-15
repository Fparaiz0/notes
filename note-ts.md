### TYPESCRIPT REQUISITOS

* Node JS 22 ou superior;
* MySql última versão.

<hr>

### TYPESCRIPT ANOTAÇÕES

Criar o package.json:

```bash
npm init
```

Instalar o TypeScript como uma dependência de desenvolvimento:

```bash
npm install --save-dev typescript
```

Criar o arquivo 'tsconfig.json', executar quando o TypeScript foi instalado somente no projeto:

```bash
npx tsc --init
```

Compilar os arquivos TypeScript:

```bash
npx tsc
```

Fazer com que o compilador fique monitorando os arquivos TypeScript e compile-os automaticamente a partir de qualquer alteraçaõ feita:

```bash
npx tsc -watch
```

Executar o arquivo JavaScript compilado:

```bash
node CAMINHO_DO_ARQUIVO
```

Diferença de var, const e let:

```js
var exemplo = "exemplo"; // Pode ter o valor alterado e pode ser usada em qualquer local.
const exemplo = "exemplo"; // Não pode ter o valor alterado e funciona em qualquer local.
let exemplo = "exemplo"; // Pode ter o valor alterado mas funciona somente dentro da função que tiver.
```

Criar objeto:

```js
// Criar variável do tipo objeto
interface Client {
    name: string;
    amount: number;
}

let client: Client {
    name: 'Lucas',
    amount: 20
};
```

<hr>

### PASSOS PARA RODAR O PROJETO TYPESCRIPT (depois de tê-lo clonado)

Instalar o restante das dependencias necessárias (isto instala todas as dependencias que estiverem listadas no arquivo package.json):

```bash
npm install
```

<hr>

### PASSOS PARA ATUALIZAR AS DEPENDENCIAS DO PROJETO

Para atualizar as dependencias de forma interativa, basta dar este comando no terminal:

```bash
npx npm-check-updates -i
```

<hr>

### REACT REQUISITOS

* Node JS 22 ou superior;
* NPX última versão.

<hr>

### PASSOS PARA RODAR O PROJETO REACT (depois de tê-lo clonado)

Instalar o restante das dependencias necessárias:

```bash
npm install
```
