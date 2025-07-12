# Dryad Programming Language


Dryad é uma linguagem de programação moderna, interpretada, com sintaxe expressiva e tipagem dinâmica.
=======
![Dryad Logo](https://img.shields.io/badge/Dryad-v0.1.0-green)
![Oak Package Manager](https://img.shields.io/badge/Oak-Modular-blue)
![License](https://img.shields.io/badge/License-MIT-blue)
[![Rust](https://github.com/Dryad-lang/source/actions/workflows/rust.yml/badge.svg)](https://github.com/Dryad-lang/source/actions/workflows/rust.yml)

## 🎯 Pilares de Desenvolvimento

1. **Test-Driven Development (TDD)** - Cada funcionalidade possui testes abrangentes
2. **Sistema de Erros Padronizado** - Códigos de erro categorizados e documentados
3. **CLI Intuitivo** - Interface de linha de comando rica em funcionalidades
4. **Gestor de Pacotes (Oak)** - Ferramenta independente para gerenciamento de projetos
5. **Modularidade** - Componentes desacoplados para máxima testabilidade
6. **Completude sem Complexidade** - Código completo mas sem over-engineering

## 📦 Estrutura do Projeto

## ✨ Principais Características

- 🚀 **Sintaxe Simples**: Fácil de aprender e usar
- 📦 **Sistema Oak**: Package manager modular integrado
- 🔗 **Imports/Exports**: Sistema modular avançado (`using` vs `use`)
- 📚 **Common Libraries**: Bibliotecas nativas organizadas
- ⚡ **Performance**: Interpretador otimizado em Rust
- 🛠️ **CLI Moderna**: Interface de linha de comando completa
- 🔧 **APIs Externas**: Suporte para modificação do oak package manager e cli.

## 🚀 Início Rápido

### 1. Instalação

```bash
# Clone o repositório
git clone https://github.com/dryad-lang/dryad.git
cd dryad

# Compile o projeto
cargo build --release

# Execute um script
./target/release/dryad script.dryad
```

### 2. Primeiro Programa

```dryad
// hello.dryad
print("Hello, Dryad!");

let nome = "Mundo";
print("Olá, " + nome + "!");

// Classes com métodos estáticos
class Math {
    static function square(x) {
        return x * x;
    }
}

let resultado = Math.square(5);
print("5² = " + resultado);
```

### 3. Sistema Oak (Package Manager)

```bash
# Inicializar projeto Oak
dryad oak init

# Listar dependências
dryad oak list

# Adicionar dependência (futuro)
dryad oak add math-utils
```

### 4. Sistema de Imports

```dryad
// Bibliotecas do sistema (using)
using IO.Console;
using Core.Types;

// Arquivos locais (use)
use './utils/helper.dryad';
use '../shared/common.dryad';

// Uso das funcionalidades
Console.println("Hello World!");
let type = Types.typeof(42);
helper.processData();
```

## 📁 Estrutura do Projeto

```
dryad/
├── crates/
│   ├── dryad_errors/       # Sistema de erros e códigos padronizados
│   ├── dryad_lexer/        # Tokenização (análise léxica)
│   ├── dryad_parser/       # Parser e construção de AST
│   ├── dryad_runtime/      # Interpretador principal
│   ├── dryad_cli/          # CLI para rodar código Dryad
│   └── oak/                # Gestor de pacotes
├── Cargo.toml              # Workspace principal
└── README.md
```

## 🚀 Funcionalidades Implementadas

### ✅ Lexer (Análise Léxica)
- [x] Comentários de linha (`//`) e bloco (`/* */`)
- [x] Tratamento de espaços em branco
- [x] Completamente funcional

### ✅ Parser (Análise Sintática)
- [x] Análise recursiva descendente
- [x] Completamente funcional

### ✅ Runtime/Interpretador
- [x] Tratamento robusto de erros de tipo
- [x] Completamente funcional

### ✅ Sistema de Erros
- [x] **Códigos estruturados por categoria**:
  - 1000-1999: Erros do Lexer
  - 2000-2999: Erros do Parser
  - 3000-3999: Erros de Runtime
  - 4000-4999: Erros do Sistema de Tipos
  - 5000-5999: Erros de I/O
  - 6000-6999: Erros do Sistema de Módulos
  - 7000-7999: Erros de Sintaxe
  - 8000-8999: Avisos (Warnings)
  - 9000-9999: Erros de Sistema
- [x] Mensagens de erro informativas
- [x] Rastreamento de linha e coluna

### ✅ CLI (dryad)
- [x] `dryad run <arquivo>` - Executa código Dryad
- [x] `dryad run <arquivo> --verbose` - Mostra tokens e AST
- [x] `dryad check <arquivo>` - Valida sintaxe
- [x] `dryad tokens <arquivo>` - Debug: mostra tokens
- [x] `dryad repl` - Modo interativo
- [x] `dryad version` - Informações da versão

### ✅ Gestor de Pacotes (Oak)
- [x] `oak init <nome>` - Cria novo projeto
- [x] `oak info` - Informações do projeto
- [x] `oak list` - Lista dependências
- [x] `oak install <pacote>` - Adiciona dependência (estrutura pronta)
- [x] `oak remove <pacote>` - Remove dependência
- [x] `oak run <script>` - Executa scripts definidos
- [x] `oak clean` - Limpa cache
- [x] Arquivo `oaklibs.json` com configuração completa
- [ ] Criação do registry (repositorio geral de dependencias)

## 🧪 Cobertura de Testes

**Total: 79 testes passando**
- Lexer: 24 testes
- Parser: 25 testes  
- Runtime: 30 testes
- Sistema de erros integrado em todos os componentes

## ▶️ Exemplos de Uso

### Executando código Dryad
```bash
# Expressão simples
echo "5 + 3 * 2" > exemplo.dryad
cargo run --bin dryad run exemplo.dryad
# Output: 11

# Modo verboso (mostra tokens e AST)
cargo run --bin dryad run exemplo.dryad --verbose

# Validar sintaxe
cargo run --bin dryad check exemplo.dryad
```

### Criando projeto com Oak
```bash
# Criar novo projeto
cargo run --bin oak init meu-projeto

# Navegar e ver informações
cd meu-projeto
cargo run --bin oak info
cargo run --bin oak list
```

### Modo Interativo (REPL)
```bash
cargo run --bin dryad repl
# dryad> 2 + 3
# => 5
# dryad> "Hello" + " World"
# => Hello World
```

## 🏗️ Pipeline de Execução

```
Código Fonte (.dryad)
    ↓
Lexer → Tokens
    ↓  
Parser → AST (Abstract Syntax Tree)
    ↓
Interpreter → Resultado
```

## 🚀 Começando

```bash
# Build do projeto
cargo build

# Executar todos os testes
cargo test

# Executar CLI
cargo run --bin dryad --help

# Executar Oak
cargo run --bin oak --help
```

## 📋 Sintaxe Suportada (v0.1)

### Tipos de Dados
- **Números**: `42`, `3.14`, `-5`
- **Strings**: `"Hello World"`, `"Olá\nMundo"`
- **Booleanos**: `true`, `false`
- **Null**: `null`

### Operadores
- **Aritméticos**: `+`, `-`, `*`, `/`
- **Comparação**: `==`, `!=`, `<`, `>`, `<=`, `>=`
- **Lógicos**: `&&`, `||`, `!`

### Exemplos Válidos
```dryad
// Aritmética
(5 + 3) * 2

// Comparações
10 > 5

// Lógica
true && false || !true

// Strings
"Hello" + " " + "World"

// Expressões complexas
(2 + 3) * 4 == 20 && true
```

## 🔮 Próximas Funcionalidades

- [X] Declarações de variáveis (`let x = 5;`)
- [X] Estruturas de controle (`if`, `while`, `for`)
- [X] Funções definidas pelo usuário
- [X] Arrays e objetos
- [ ] Sistema de módulos e imports
- [ ] Instalação real de pacotes no Oak

## 🤝 Contribuindo

Este projeto segue rigorosamente os princípios de TDD. Para contribuir:

1. Escreva testes para a nova funcionalidade
2. Implemente a funcionalidade para passar nos testes
3. Refatore mantendo todos os testes passando
4. Adicione códigos de erro apropriados quando necessário

## 📄 Licença

MIT License - veja o arquivo LICENSE para detalhes.
