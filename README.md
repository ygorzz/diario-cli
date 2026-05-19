# diario-cli

CLI simples para registrar anotações de estudo diretamente pelo terminal, salvando automaticamente cada entrada em um arquivo `diario.txt` com data e hora formatadas.

![Node.js](https://img.shields.io/badge/node-%3E%3D18-green)
![CLI](https://img.shields.io/badge/type-CLI-blue)
![License](https://img.shields.io/badge/license-MIT-informational)

---

## Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Available Commands](#available-commands)
- [Concepts Practiced](#concepts-practiced)
- [Example Output](#example-output)
- [Contributing](#contributing)
- [License](#license)

---

## About

`diario-cli` é uma aplicação de linha de comando desenvolvida em Node.js para registrar rapidamente anotações de estudo pelo terminal.

O projeto foi criado com foco em prática de conceitos fundamentais do ecossistema Node.js moderno, incluindo manipulação de arquivos, programação assíncrona, ES Modules e construção de CLIs utilizando Commander.

Cada anotação é salva automaticamente em um arquivo `diario.txt`, incluindo data e hora formatadas em português (`pt-BR`).

---

## Features

- Adicionar anotações pelo terminal
- Registrar automaticamente data e hora
- Listar todas as anotações salvas
- Limpar completamente o diário
- Criação automática de arquivos e diretórios
- Tratamento de erros com `try/catch`
- Compatível com múltiplos sistemas operacionais

---

## Tech Stack

| Categoria | Tecnologias |
|---|---|
| Runtime | Node.js |
| CLI | Commander |
| File System | fs/promises |
| Path Handling | path |
| Module System | ES Modules |

---

## Project Structure

```bash
diario-cli/
├── src/
│   ├── comandos/
│   ├── services/
│   ├── utils/
│   └── index.js
├── diario.txt
├── package.json
└── README.md
```

---

# Getting Started

## Prerequisites

- Node.js 18+

---

## Installation

```bash
# Clone the repository
git clone <repository-url>

# Access the project folder
cd diario-cli

# Install dependencies
npm install

# Register CLI globally
npm link
```

---

## Usage

### Adicionar anotação

```bash
diario add "Aprendi sobre async/await"
```

### Listar anotações

```bash
diario list
```

### Limpar diário

```bash
diario clear
```

---

## Available Commands

| Comando | Descrição |
|---|---|
| `diario add "<texto>"` | Adiciona uma nova anotação |
| `diario list` | Lista todas as anotações salvas |
| `diario clear` | Remove todas as anotações do diário |

---

## Concepts Practiced

### ES Modules

- `import`
- `export`
- `export default`

### Programação Assíncrona

- `async`
- `await`

### Tratamento de Erros

- `try/catch`
- `throw`
- `new Error()`

### Sistema de Arquivos (`fs`)

- `fs.promises.mkdir`
- `fs.promises.appendFile`
- `fs.promises.readFile`
- `fs.promises.writeFile`

### Manipulação de Caminhos

- `path.resolve`

### Datas

```js
new Date().toLocaleString('pt-BR')
```

### Commander

- `.command()`
- `.argument()`
- `.action()`
- `.parseAsync()`

### CLI com Node.js

- `npm link`
- `"bin"` no `package.json`
- Shebang:

```bash
#!/usr/bin/env node
```

### Tratamento do erro `ENOENT`

Tratamento de erros relacionados a arquivos ou caminhos inexistentes.

---

## Example Output

```txt
[18/05/2026, 21:30:12]
Aprendi sobre async/await

[18/05/2026, 21:45:03]
Estudei Commander.js
```

---

## Contributing

Contribuições são bem-vindas.

```bash
# Create a new branch
git checkout -b feature/new-feature

# Commit changes
git commit -m "feat: add new feature"

# Push branch
git push origin feature/new-feature
```

---

## License

This project is licensed under the MIT License.
