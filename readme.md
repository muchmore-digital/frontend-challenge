# *Muchmore.digital | Teste front-end*
## *Sobre o teste*

Olá, este é o desafio para a desenvolvedores Front-End da Muchmore.digital. Neste repositório nós temos duas paginas que estão em PSD e JPG e  o objetivo é codificar essas páginas em HTML. Você irá notar que temos apenas o design para desktop, mas você ficará responsável por transformar esse layout em uma página “responsivo”.

### *Home*

Nesta página temos uma contagem regressiva para o lançamento do site, o objetivo aqui é fazer esse contador funcionar e contar repressivamente dia, hora, minuto e segundos até 06/06/2020.

### *Contact Us*

Nesta página o principal desafio é integrar o formulário de contato com a API disponibilizada mais abaixo.

A ideia é que quando os usuários preencherem o formulário este faça uma requisição para a API e caso sucesso exiba uma mensagem de sucesso, caso retorne algum erro, essa mensagem deve ser tratada e uma mensagem de erro deve ser mostrada para o usuário.

- - - -

### *Entrega do teste*

Para entregar o teste você deve criar um repositório no GitHub, hospedar todo seu código de forma pública e compartilhar com a gente apenas o link.

É importante que você coloque no _readme_  um passo a passo de como executar seu código, desde como compilar o código caso necessário, ou até mesmo as dependências necessárias, caso haja alguma.

O teste deve ser executado sem utilizar nenhuma linguagem back-end, seria interessante que você utiliza-se algum framework para front-end como por exemplo o vue.js, react e angular. Porém fique livre para desenvolver o desafio da maneira que acredite ser a melhor.

### *Critérios de avaliação*

Para este teste iremos levar em consideração os seguintes critérios de avaliação:
	1.	Resolução do desafio proposto;
	2.	Qualidade do código desenvolvido;
	3.	Responsividade do site;

## *Requisição a API*
Para solicitar o envio do formulário é preciso realizar uma chamada do tipo POST (https://sendmail.muchomas.xyz/) com o seguinte código de autorização no Header:

```
Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJNdWNoTW9yZSIsImlhdCI6MTU4MzQzMTEyOCwiZXhwIjoxNjE0OTY3MTI4LCJhdWQiOiJ3d3cubXVjaG1vcmUuY29tIiwic3ViIjoibXVjaG1vcmUtdGVzdC1kZXYiLCJHaXZlbk5hbWUiOiJKb2hubnkiLCJTdXJuYW1lIjoiUm9ja2V0IiwiRW1haWwiOiJqcm9ja2V0QGV4YW1wbGUuY29tIiwiUm9sZSI6WyJNYW5hZ2VyIiwiUHJvamVjdCBBZG1pbmlzdHJhdG9yIl19.x5i2ldiTazjY1ANxdoURBiQ-TXqam_K1KJfdo3puYEQ
```

Os dados do formulário devem ser enviados com a seguinte formatação:

```
{
    "email": "seu@email.com",
    "subject": "Titulo do email",
    "name": "Nome",
    "comment": "Comentário"
}
```

Os campos de nome, email e comentário são obrigatórios.

Caso a requisição ocorra sem erros, a API retornará o json abaixo, com código 200 :

```
{
    "message": "Email enviado com sucesso"
}
```

Caso contrário, a API retornará uma mensagem de erro e o código correspondente.
