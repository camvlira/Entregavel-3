# Entregável 3 - Calculadora com Express

API simples feita com **Node.js** e **Express** que realiza as quatro operações matemáticas básicas (soma, subtração, divisão e multiplicação) através de requisições **POST**.

O objetivo do projeto é praticar a criação de rotas POST, a leitura de dados enviados no corpo da requisição (`req.body`) e o teste da API com o **Postman**.

## Tecnologias

- [Node.js](https://nodejs.org/)
- [Express](https://expressjs.com/)
- [body-parser](https://www.npmjs.com/package/body-parser)
- [Postman](https://www.postman.com/) (para testar as requisições)

## Pré-requisitos

1. **Node.js** instalado. Baixe a versão LTS em [nodejs.org](https://nodejs.org/) e instale normalmente.
   Para conferir se deu certo, rode no terminal:
   ```bash
   node -v
   npm -v
   ```
2. **Postman** para testar a API. Você pode instalar a extensão **Postman** direto no VS Code (aba de extensões) ou usar o aplicativo.

## Instalação

1. Clone o repositório (ou baixe o ZIP e extraia):
   ```bash
   git clone <URL-DO-SEU-REPOSITORIO>
   ```
2. Entre na pasta do projeto:
   ```bash
   cd <NOME-DA-PASTA>
   ```
3. Instale as dependências:
   ```bash
   npm install express
   npm install body-parser
   ```

> Se o repositório já tiver o `package.json`, basta rodar `npm install`.

## Como executar

No terminal, dentro da pasta do projeto:

```bash
node app.js
```

Se tudo deu certo, aparecerá a mensagem:

```
App de Exemplo escutando na porta http://localhost:3000/
```

Deixe o terminal aberto: o servidor precisa continuar rodando para receber as requisições.

> Se você alterar o código, pare o servidor com `Ctrl + C` e rode `node app.js` novamente.

## Testando no navegador

Abra [http://localhost:3000](http://localhost:3000). Deve aparecer:

```
Oi, mundo.
```

Essa é a rota `GET /`, só para confirmar que o servidor está funcionando.

## Testando no Postman

As operações são rotas **POST**, então não funcionam digitando a URL no navegador. Use o Postman:

1. Crie uma nova requisição (**New HTTP Request**).
2. Escolha o método **POST**.
3. Digite a URL da operação desejada, por exemplo `http://localhost:3000/soma`.
4. Abra a aba **Body**, marque **raw** e, no menu ao lado, escolha **JSON** (não deixe em *Text*).
5. Cole o JSON abaixo:
   ```json
   { "a": 7, "b": 3 }
   ```
6. Clique em **Send**.

## Rotas disponíveis

| Método | Rota             | Descrição     | Resposta para `{ "a": 7, "b": 3 }`                     |
| ------ | ---------------- | ------------- | ------------------------------------------------------ |
| GET    | `/`              | Teste do site | `Oi, mundo.`                                           |
| POST   | `/soma`          | Soma          | `O resultado da soma de 7 e 3 é 10`                     |
| POST   | `/subtracao`     | Subtração     | `O resultado da subtração de 7 e 3 é 4`               |
| POST   | `/divisao`       | Divisão       | `O resultado da divisão de 7 e 3 é 2.333333333333333` |
| POST   | `/multiplicacao` | Multiplicação | `O resultado da multiplicação de 7 e 3 é 21`            |

### Formato do corpo (body)

Todas as rotas POST esperam um JSON com dois números:

```json
{
  "a": 7,
  "b": 3
}
```

## Estrutura do projeto

```
.
├── app.js          # servidor e rotas
├── package.json
└── README.md
```

## GET
<img width="261" height="106" alt="image" src="https://github.com/user-attachments/assets/b8d6fb95-3b68-4727-96f9-0736bba1dcab" />

## POSTS
# Soma
<img width="999" height="470" alt="image" src="https://github.com/user-attachments/assets/7447e319-ad15-4510-887c-2e11912488a0" />
# Subtração
<img width="1015" height="489" alt="image" src="https://github.com/user-attachments/assets/665c1e65-47fa-4c1b-9c55-6277bea0aa84" />
# Multiplicação
<img width="1012" height="465" alt="image" src="https://github.com/user-attachments/assets/83123fd1-2199-4550-858f-ecec1caef108" />
# Divisão
<img width="998" height="466" alt="image" src="https://github.com/user-attachments/assets/3d27e996-2e17-4955-9bea-aca8df578b75" />
