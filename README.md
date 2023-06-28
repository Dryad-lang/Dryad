# Dryad shell

## Comandos

A linguagem possui os seguintes comandos disponíveis:

### Comando `run`

O comando `run` é utilizado para executar um programa Dryad.

#### Descrição

Executa um programa Dryad a partir de um arquivo.

#### Argumentos

- `file` (obrigatório): O arquivo contendo o programa Dryad a ser executado. O arquivo deve ter a extensão ".dyd".

#### Uso

```
dryad run <file>
```

Exemplo:
```
dryad run programa.dyd
```

### Comando `help`

O comando `help` é utilizado para exibir a ajuda.

#### Descrição

Exibe a lista de comandos disponíveis e suas descrições.

#### Uso

```
dryad help
```

# Oak shell

## Comandos

A linguagem possui os seguintes comandos disponíveis:

### Comando `init`

O comando `init` é utilizado para criar um novo projeto.

#### Descrição

Cria um novo projeto com as informações fornecidas.

#### Argumentos

- `name` (obrigatório): O nome do projeto.
- `description` (obrigatório): A descrição do projeto.
- `version` (obrigatório): A versão do projeto.
- `author` (obrigatório): O autor do projeto.
- `license` (obrigatório): A licença do projeto.
- `repository` (obrigatório): O repositório do projeto.

#### Uso

```
oak init
```

### Comando `syncmodules`

O comando `syncmodules` é utilizado para sincronizar os módulos externos.

#### Descrição

Sincroniza os módulos externos do projeto.

#### Uso

```
oak syncmodules
```

### Comando `build`

O comando `build` é utilizado para construir o projeto.

#### Descrição

Constrói o projeto.

#### Uso

```
oak build
```

### Comando `init-extlib-project`

O comando `init-extlib-project` é utilizado para criar um novo projeto externo.

#### Descrição

Cria um novo projeto externo com as informações fornecidas.

#### Argumentos

- `name` (obrigatório): O nome do projeto externo.
- `description` (obrigatório): A descrição do projeto externo.
- `version` (obrigatório): A versão do projeto externo.
- `author` (obrigatório): O autor do projeto externo.
- `license` (obrigatório): A licença do projeto externo.
- `repository` (obrigatório): O repositório do projeto externo.

#### Uso

```
oak init-extlib-project
```

Exemplo:
```
oak init-extlib-project
```


# Documentação da Linguagem

## Expressões Matemáticas

A linguagem oferece suporte a expressões matemáticas básicas, como adição, subtração, multiplicação, divisão, módulo e exponenciação.

Exemplos:
- Operador de adição: `1 + 1;`
- Operador de subtração: `10 - 1;`
- Operador de multiplicação: `3 * 5;`
- Operador de divisão: `15 / 3;`
- Operador de módulo: `15 % 3;`
- Operador de exponenciação: `3 ** 2;`

## Blocos e Funções

A linguagem suporta o uso de blocos de código e a definição de funções.

Exemplos:
- Blocos: `{1 + 2; 2 * 3;}`
- Escopos: `{ {a = 5;} a;}` (retorna o valor de `a`)
- Funções: `{ square = function(x) { x*x; }; square(5); }` (retorna 25)

## Atribuição de Variáveis

A linguagem permite a atribuição de valores a variáveis.

Exemplos:
- Atribuição: `{a = 5 + 2; a;}`
- Incremento: `{a = 5; --a;}`
- Decremento: `{a = 5; ++a;}`
- Atribuição com adição: `{a = 5 + 2; a += 2;}`
- Atribuição com subtração: `{a = 5 + 2; a -= 2;}`
- Atribuição com multiplicação: `{a = 5 + 2; a *= 2;}`
- Atribuição com divisão: `{a = 5 + 2; a /= 2;}`
- Atribuição com módulo: `{a = 5 + 2; a %= 2;}`
- Atribuição com operação bitwise AND: `{a = 5 + 2; a &= 2;}`
- Atribuição com operação bitwise OR: `{a = 5 + 2; a |= 2;}`
- Atribuição com operação bitwise XOR: `{a = 5 + 2; a ^= 2;}`
- Atribuição com operação de deslocamento para a esquerda: `{a = 5 + 2; a <<= 2;}`
- Atribuição com operação de deslocamento para a direita: `{a = 5 + 5; a >>= 2;}`

## Condições

A linguagem oferece suporte a estruturas condicionais, como `if` e `if-else`, para controlar o fluxo do programa.

Exemplos:
- `if` de sucesso: `{a = 5; if(a == 5) a = 6; a;}`
- `if` de falha: `{a = 5; if(a != 5) a = 6; a;}`
- `if-else` de sucesso: `{a = 5; if(a == 5) a = 6; else a = 7; a;}`
- `if-else` de falha: `{a = 5; if(a != 5

) a = 6; else a = 7; a;}`

## Loops

A linguagem suporta loops `while` e `for` para repetição de código.

Exemplos:
- `while`: `{a = 10; while (a < 20) ++a; a;}`
- `for`: `{a = -10; for (a = 0; a < 10; ++a) 0; a;}`
- `do-while`: `{a = 5; do ++a; while (a < 10);}`

## Operadores Lógicos

A linguagem possui operadores lógicos, como `&&` (E lógico), `||` (OU lógico) e `!` (NÃO lógico).

Exemplos:
- `&&` lógico: `0 && 5;`
- `||` lógico: `5 || 0;`
- `!` lógico: `!5;`

## Operadores Bit a Bit

A linguagem suporta operações bit a bit, como `&` (AND bit a bit), `|` (OR bit a bit), `^` (XOR bit a bit) e `~` (NÃO bit a bit).

Exemplos:
- `&` bit a bit: `65421 & 255;`
- `|` bit a bit: `65421 | 255;`
- `^` bit a bit: `65421 ^ 255;`
- `~` bit a bit: `~65421;`

## Operadores de Comparação

A linguagem oferece operadores de comparação para avaliar igualdade, desigualdade e relação de ordem entre valores.

Exemplos:
- Igualdade: `1 == 1;`
- Desigualdade: `1 != 5;`
- Inferioridade: `1 < 5;`
- Superioridade: `1 > 5;`
- Inferior ou igual: `1 <= 5;`
- Superior ou igual: `1 >= 5;`

## Expressões Mistas

A linguagem suporta expressões complexas envolvendo diferentes operadores e prioridades.

Exemplos:
- Expressões complexas: `1+4/5*4+51+(4*(945+94/748)+44+2)+56;`
- Expressões lógicas complexas: `0 || 45-54/9 && 564 + 485 * 4 || 45 / 6;`

## Manipulação de Strings

A linguagem suporta manipulação de strings, permitindo a atribuição de valores a variáveis do tipo string e a utilização de funções para operações específicas.

Exemplo de atribuição de variáveis:
- Atribuição de string: `{str = "Hello, world!";}`

Funções disponíveis:
- `ConsoleWrite(string)`: Imprime uma string no console sem quebra de linha.
- `ConsoleWriteLine(string)`: Imprime uma string no console com quebra de linha.
- `ConsoleRead()`: Lê uma linha de texto do console e retorna como uma string.
- `ConsoleReadLine()`: Lê uma linha de texto do console e retorna como uma string, removendo a quebra de linha.
- `ConsoleReadKey()`: Lê um caractere do console e retorna como uma string.
- `ConsoleError(string)`: Imprime uma string de erro no console.

Exemplo de uso das funções de console:
```
ConsoleWrite("Hello, ");
ConsoleWriteLine("world!");
var input = ConsoleRead();
ConsoleWriteLine("You entered: " + input);
```

Esta é apenas uma documentação inicial como a linguagem se encontra em beta varias coisas poderão ser mudadas no futuro.
