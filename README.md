# format-masks
Este é um componente Angular que serve para formatar máscaras de CPF, CNPJ, CEP e Telefones brasileiros.

As máscaras só funcionam em inputs HTML. Esse componente serve para formatar strings que vêm de uma API e printar no HTML de forma correta.

## Instalação

Rode o comando npm install para executar a instalação do pacote:

```
npm install format-masks
```

Feito isso o componente ficará instalado no diretório node_modules/

## Configuração

Agora você precisa colocar o JS responsável por chamar o componente:

```html
<script src="/node_modules/format-masks/dist/faq.component.js"></script>
```

Agora adicione o componente no módulo Angular do seu projeto:

```javascript
angular.module('application', ['format.masks']);
```

## Aplicando no template

Agora é adicionar a tag na sua view:

```html
<format-masks></format-masks>
```

### Opções de máscaras

Você pode adicionar as seguintes máscaras:

* CPF
* CNPJ
* CEP
* Telefone

O componente possui um atributo **OBRIGATÓRIO** chamado mask-type, que você passa o tipo de máscara que você quer que o componente transforme:

```html
<format-masks maskt-type="cpf"></format-masks>
```

Os tipos são:

* cpf
* cnpj
* cep
* brazilian-phone

### Valores

Depois do tipo você precisa passar o valor da máscara:

```html
<format-masks maskt-type="cpf" mask-value="11111111111"></format-masks>
```

Os valores só aceitam números e com seus respectivos valores máximos:

* cpf - 11 caracteres
* cnpj - 14 caracteres
* cep - 8 caracteres
* brazilian-phone - 8 ou 9 caracteres

Feito isso, sua string será formata com a máscara:

```html
111.111.111-11
```

## Finalizando

Qualquer dúvida, melhoria, sugestão, é só entrar em contato.
