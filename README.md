# ✅ Todo List - Reatividade com Vue.js

![Status](https://img.shields.io/badge/Status-Finalizado-green)
![Vue.js](https://img.shields.io/badge/Framework-Vue.js-4FC08D?logo=vue.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/Code-JavaScript-F7DF1E?logo=javascript&logoColor=black)

> Uma Single Page Application (SPA) para gerenciamento de tarefas, demonstrando o poder da renderização reativa e a arquitetura de componentes do Vue.js.

## 🎯 Motivação e Propósito

Após dominar a manipulação imperativa do DOM (JavaScript Vanilla/jQuery), é necessário evoluir para abordagens declarativas. O propósito deste projeto é aplicar os conceitos fundamentais do **Vue.js**.

Este repositório resolve o problema de complexidade na atualização de interfaces. Ao invés de selecionar elementos e alterar o HTML manualmente, o projeto utiliza o **Virtual DOM** do Vue para atualizar a tela automaticamente sempre que o estado dos dados (lista de tarefas) muda.

## 🖼️ Demonstração Visual



## 🛠️ Tecnologias Utilizadas

A stack foca na simplicidade e performance do framework progressivo:

* **[Vue.js](https://vuejs.org/):** Framework principal utilizado para:
    * **Diretivas:** Uso de `v-for` (listagem), `v-if` (condicional) e `v-model` (ligação bidirecional de dados).
    * **Eventos:** Manipulação de interação do usuário (`@click`, `@submit`).
    * **SFC (Single File Components):** Estrutura de arquivos `.vue` que encapsulam HTML, CSS e JS.
* **[JavaScript (ES6+)](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript):** Lógica de manipulação de arrays e objetos.
* **[CSS3](https://developer.mozilla.org/pt-BR/docs/Web/CSS):** Estilização escopada (Scoped CSS) para isolar o design dos componentes.

## ✨ Funcionalidades

A aplicação implementa um CRUD básico de memória:

1.  **Adicionar Tarefa:** Input controlado que captura o texto e atualiza a lista reativa.
2.  **Listagem Dinâmica:** Renderização automática de itens baseada no array de dados.
3.  **Remover Tarefa:** Interação para excluir itens da lista, demonstrando a reatividade instantânea da interface.
4.  **Estado da Tarefa:** (Se aplicável no código) Checkbox para marcar itens como concluídos.

## 📦 Instalação e Configuração

O projeto requer um ambiente Node.js para gerenciar as dependências e o servidor de desenvolvimento.

### Pré-requisitos
* **Node.js** e **NPM** instalados.
* **Git** instalado.

### Passo a Passo

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/DouglassenG/todo-vue.git](https://github.com/DouglassenG/todo-vue.git)
    ```

2.  **Acesse o diretório:**
    ```bash
    cd todo-vue
    ```

3.  **Instale as dependências:**
    ```bash
    npm install
    ```

4.  **Execute o Servidor Local:**
    Para iniciar a aplicação em modo de desenvolvimento (Hot Reload):
    ```bash
    npm run serve
    # Ou, dependendo da configuração do projeto (Vite):
    npm run dev
    ```

## 💻 Uso e Exemplos

O código destaca a sintaxe limpa do Vue para loops e eventos.

**Exemplo de Template (Vue):**

```html
<template>
  <div class="container">
    <input v-model="novaTarefa" placeholder="Digite uma tarefa" />
    <button @click="adicionarTarefa">Adicionar</button>

    <ul>
      <li v-for="(tarefa, index) in tarefas" :key="index">
        {{ tarefa }}
        <button @click="removerTarefa(index)">Excluir</button>
      </li>
    </ul>
  </div>
</template>
