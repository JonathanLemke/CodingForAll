# Identação e Blocos de Código

A identação é uma prática de adicionar espaços ou tabulações no início das linhas de código para torná-lo mais legível e organizado. Ela ajuda a visualizar a estrutura do código e a relação entre diferentes blocos de código.

Um bloco de código é um conjunto de instruções que são agrupadas. Em muitas linguagens de programação, os blocos de código são definidos por chaves `{}` ou palavras-chave específicas.

## Exemplos em Portugol Studio e PHP

Abaixo estão exemplos de código não indentado e indentado em Portugol Studio e PHP, com e sem a estrutura de controle `se`.

### Portugol Studio

#### Sem Identação

```plaintext
programa
{
funcao inicio()
{
inteiro numero = 5
inteiro fatorial = 1
se (numero > 0)
{
para(inteiro i = 1; i <= numero; i++)
{
fatorial = fatorial * i
}
escreva("O fatorial de ", numero, " é ", fatorial)
}
senao
{
escreva("O número deve ser maior que zero")
}
}
}
```

Neste exemplo, temos três blocos de código:

1. O bloco de código da função `inicio()`, que inclui todo o código dentro da função.
2. O bloco de código da condição `se (numero > 0)`, que inclui o loop `para` e a instrução `escreva`.
3. O bloco de código da condição `senao`, que inclui a instrução `escreva`.

#### Com Identação

```plaintext
programa
{
    funcao inicio()
    {
        inteiro numero = 5
        inteiro fatorial = 1

        se (numero > 0)
        {
            para(inteiro i = 1; i <= numero; i++)
            {
                fatorial = fatorial * i
            }

            escreva("O fatorial de ", numero, " é ", fatorial)
        }
        senao
        {
            escreva("O número deve ser maior que zero")
        }
    }
}
```

No primeiro exemplo, é difícil ver à primeira vista que o `fatorial = fatorial * i` está dentro do `para(inteiro i = 1; i <= numero; i++)`. No segundo exemplo, a identação torna isso muito mais claro.

### PHP

#### Sem Identação

```php
<?php
$numero = 5;
$fatorial = 1;
if ($numero > 0) {
for($i = 1; $i <= $numero; $i++){
$fatorial = $fatorial * $i;
}
echo "O fatorial de " . $numero . " é " . $fatorial;
} else {
echo "O número deve ser maior que zero";
}
?>
```

#### Com Identação

```php
<?php
    $numero = 5;
    $fatorial = 1;

    if ($numero > 0) {
        for($i = 1; $i <= $numero; $i++){
            $fatorial = $fatorial * $i;
        }

        echo "O fatorial de " . $numero . " é " . $fatorial;
    } else {
        echo "O número deve ser maior que zero";
    }
?>
```

Novamente, no primeiro exemplo, é difícil ver à primeira vista que o `$fatorial = $fatorial * $i;` está dentro do `for($i = 1; $i <= $numero; $i++)`. No segundo exemplo, a identação torna isso muito mais claro.

## Explicação no código
```plaintext
programa
{
    funcao inicio() // Início do bloco da função 'inicio'
    {
        inteiro numero = 5
        inteiro fatorial = 1

        // A identação aqui (espaços antes do 'se') indica que estamos dentro do bloco da função 'inicio'
        se (numero > 0) // Início do bloco 'se'
        {
            // A identação aqui (espaços antes do 'para') indica que estamos dentro do bloco 'se'
            para(inteiro i = 1; i <= numero; i++) // Início do bloco 'para'
            {
                // A identação aqui (espaços antes do 'fatorial') indica que estamos dentro do bloco 'para', que está dentro do bloco 'se'
                fatorial = fatorial * i
            } // Fim do bloco 'para'

            // A identação aqui (espaços antes do 'escreva') indica que ainda estamos dentro do bloco 'se', mas fora do bloco 'para'
            escreva("O fatorial de ", numero, " é ", fatorial)
        } // Fim do bloco 'se'
        senao // Início do bloco 'senao'
        {
            // A identação aqui (espaços antes do 'escreva') indica que estamos dentro do bloco 'senao'
            escreva("O número deve ser maior que zero")
        } // Fim do bloco 'senao'
    } // Fim do bloco da função 'inicio'
} // Fim do programa
```
A identação ajuda a ver claramente a estrutura do código e quais partes do código estão dentro de quais blocos. Sem a identação, seria mais difícil ver essa relação à primeira vista.
