# Aula: Tratamento de Dados - 01/04/2025


## Para exibir uma solicitação de algo como nome do usuário ao abrir o site:
    window.prompt()

## Para exibir uma mensagem, como um aviso:
    window.alert()

## É possível juntar isso a uma variável, exemplo:
    var nome = window.prompt('Qual é seu nome?')

<!-- A variável 'nome', recebe 'window.prompt' -->

- Com isso, podemos gerar um alert que exibe uma mensagem, utilizando da variável 'nome'. Assim, o nome exibido, será o nome digitado. Dessa forma:
    window.alert('É um grande prazer te conhecer, ' + nome + '!') <!-- + em JS significa: Contatenação -->

- Após a var, podemos utilizar mais uma contatenação, com uma exclamação entre aspas, para complementar a frase, que ficará assim:
    <!-- É um grande prazer te conhecer, 'nome'! -->

## Convertendo strings para number

- Vamos supor que você queira fazer um cálculo usando as variáveis, exemplo:
    var n1 = window.prompt('Digite um número:')
    var n2 = window.prompt('Digite outro número:')

    var s = n1 + n2
    window.alert('A soma dos dois valores é:' + s) <!-- Concatenação -->

- O problema é que o '+' serve tanto para adição, quanto para concatenação. Isso gera um "conflito", porque o 'window.prompt' retorna para mim, uma string, mesmo que eu digite um número.
<!-- (number + number) para adição; -->
<!-- (string + string) para concatenação -->

- Então precisamos converter de string para número, lá na variável, usando um:
    Number.parseInt <!-- Para número inteiro -->
ou
    Number.parseFloat <!-- Para número real -->

- Ficando dessa forma:
    var n1 = Number.parseFloat(window.prompt('Digite um número:'))
ou
    var n1 = parseFloat(window.prompt('Digite um número:')) <!-- Sem o 'Number' que também é possível -->

### Para encurtar esse processo:

- Podemos utilizar somente:
    Number <!-- Antes do 'window.prompt', funcionando perfeitamente também.-->
Ex: var n1 = Number(window.prompt('Digite um número:'))

## Convertendo number para string