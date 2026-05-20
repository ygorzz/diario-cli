# diario-cli

![Node.js](https://img.shields.io/badge/node-%3E%3D18-green)
![Commander](https://img.shields.io/badge/commander-CLI-blue)
![ESModules](https://img.shields.io/badge/modules-ESM-yellow)
![License](https://img.shields.io/badge/license-MIT-informational)

## Descrição

CLI simples para registrar anotações de estudo diretamente pelo terminal, salvando automaticamente cada entrada em um arquivo `diario.txt` com data e hora formatadas.

O projeto foi desenvolvido como prática de conceitos fundamentais do ecossistema Node.js moderno, incluindo manipulação de arquivos, programação assíncrona, ES Modules e construção de aplicações de linha de comando utilizando Commander.

A aplicação permite adicionar, listar e limpar anotações através de comandos executados no terminal, funcionando de maneira simples e multiplataforma.

---

## Tecnologias utilizadas

| Tecnologia | Versão | Função |
|---|---|---|
| [Node.js](https://nodejs.org/) | >= 18 | Ambiente de execução JavaScript |
| [Commander](https://github.com/tj/commander.js) | — | Criação e gerenciamento da CLI |
| `fs/promises` | Nativo | Manipulação assíncrona de arquivos |
| `path` | Nativo | Manipulação de caminhos de arquivos |
| ES Modules | Nativo | Sistema moderno de módulos (`import/export`) |

A aplicação utiliza **ES Modules** (`import`/`export`) nativamente.

---

## Estrutura do projeto

```bash
diario-cli/
├── src/
│   ├── comandos/                # Definição dos comandos da CLI
│   ├── services/                # Regras de negócio e manipulação do diário
│   ├── utils/                   # Funções auxiliares
│   └── index.js                 # Ponto de entrada da aplicação
├── diario.txt                   # Arquivo onde as anotações são armazenadas
├── package.json
└── README.md
```

---

## Funcionalidades

| Comando | Descrição |
|---|---|
| `diario add "<texto>"` | Adiciona uma nova anotação ao diário |
| `diario list` | Lista todas as anotações salvas |
| `diario clear` | Remove todas as anotações do diário |

### Adicionar anotação

```bash
diario add "Aprendi sobre async/await"
```

A anotação será registrada automaticamente com data e hora formatadas em `pt-BR`.

### Listar anotações

```bash
diario list
```

Exibe todas as anotações armazenadas no arquivo `diario.txt`.

### Limpar diário

```bash
diario clear
```

Remove todo o conteúdo do diário.

---

## Funcionalidades e diferenciais

- **CLI com Commander** — Estruturação profissional de comandos e argumentos.
- **Persistência em arquivo** — Todas as as anotações são armazenadas automaticamente em `diario.txt`.
- **Datas formatadas** — Registro automático utilizando `toLocaleString('pt-BR')`.
- **Programação assíncrona** — Uso de `async/await` para manipulação de arquivos.
- **Tratamento de erros** — Implementação de `try/catch` e erros personalizados.
- **Criação automática de arquivos** — Arquivos e diretórios podem ser criados dinamicamente quando necessário.
- **Manipulação de caminhos** — Utilização do módulo `path` para compatibilidade multiplataforma.
- **ES Modules** — Uso do sistema moderno de módulos do Node.js.
- **CLI global** — Possibilidade de registrar o comando utilizando `npm link`.
- **Compatibilidade multiplataforma** — Funciona em Windows, Linux e macOS.

---

## Como executar o projeto

### Pré-requisitos

- [Node.js](https://nodejs.org/) v18 ou superior

### Passo a passo

**1. Clone o repositório e acesse a pasta do projeto:**

```bash
git clone <url-do-repositorio>
cd diario-cli
```

---

**2. Instale as dependências:**

```bash
npm install
```

---

**3. Registre a CLI globalmente:**

```bash
npm link
```

Após isso, o comando `diario` estará disponível no terminal.

---

**4. Utilize os comandos da aplicação:**

Adicionar anotação:

```bash
diario add "Minha anotação"
```

Listar anotações:

```bash
diario list
```

Limpar diário:

```bash
diario clear
```

---

## Observações

- O projeto foi desenvolvido com foco em prática de Node.js moderno e construção de CLIs.
- A aplicação utiliza programação assíncrona para manipulação de arquivos.
- O arquivo `diario.txt` é utilizado como persistência simples de dados.
- O projeto utiliza ES Modules nativamente.
- O projeto utiliza o Commander para criação e gerenciamento dos comandos da CLI.

---

## Licença

Este projeto está sob a licença [MIT](https://opensource.org/licenses/MIT).

---
*Desenvolvido por **Ygor Santos** — [LinkedIn](https://www.linkedin.com/in/ygor-santos-869152325/) | [GitHub](https://github.com/ygorzz)*
