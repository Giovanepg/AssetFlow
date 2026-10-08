<a id="topo"></a>

# 📦 AssetFlow

### Sistema de Gestão e Empréstimo de Equipamentos

O **AssetFlow** é uma aplicação desktop desenvolvida para gerenciar usuários, categorias, equipamentos, empréstimos e devoluções de forma simples, organizada e centralizada.

O sistema foi desenvolvido utilizando **Python, PySide6 e PostgreSQL**, com integração direta entre a aplicação e recursos do banco de dados como **View, Function e Procedure**.



---

<p align="center">
  <a href="#sobre">Sobre</a> •
  <a href="#funcionalidades">Funcionalidades</a> •
  <a href="#video">Vídeo</a> •
  <a href="#banco">Banco de Dados</a> •
  <a href="#executar">Como executar</a> •
  <a href="#autor">Autor</a>
</p>

---

<a id="sumario"></a>

## 📑 Sumário

- [🎥 Vídeo de demonstração](#video)
- [📌 Sobre o projeto](#sobre)
- [🎯 Objetivo](#objetivo)
- [🛠 Tecnologias utilizadas](#tecnologias)
- [✨ Principais funcionalidades](#funcionalidades)
  - [📊 Dashboard](#dashboard)
  - [👤 Usuários](#usuarios)
  - [🗂 Categorias](#categorias)
  - [💻 Equipamentos](#equipamentos)
  - [📤 Novo empréstimo](#novo-emprestimo)
  - [📋 Empréstimos ativos](#emprestimos-ativos)
  - [📥 Devolução](#devolucao)
  - [🕒 Histórico](#historico)
- [🗄 Banco de Dados](#banco)
- [👁 View](#view)
- [⚙ Function](#function)
- [🔄 Procedure](#procedure)
- [🔗 Integração aplicação + banco](#integracao)
- [📁 Estrutura do projeto](#estrutura)
- [🚀 Como executar](#executar)
- [📚 Conceitos aplicados](#conceitos)
- [🎓 Contexto acadêmico](#academico)
- [👨‍💻 Autor](#autor)
- [✅ Status do projeto](#status)

---

<a id="video"></a>

# 🎥 Vídeo de demonstração

Confira abaixo uma demonstração completa do **AssetFlow**, mostrando o funcionamento da aplicação e sua integração com o PostgreSQL.


No vídeo são demonstrados:

- Dashboard;
- gerenciamento de usuários;
- gerenciamento de categorias;
- gerenciamento de equipamentos;
- realização de empréstimos;
- verificação de disponibilidade;
- empréstimos ativos;
- devolução de equipamentos;
- histórico de empréstimos;
- utilização da View;
- utilização da Function;
- utilização da Procedure;
- integração entre Python e PostgreSQL.

[⬆ Voltar ao topo](#topo)

---

<a id="sobre"></a>

# 📌 Sobre o projeto

O **AssetFlow** foi desenvolvido para facilitar o gerenciamento de equipamentos que podem ser disponibilizados para empréstimo.

A aplicação centraliza as principais informações do patrimônio e permite acompanhar todo o ciclo de utilização de um equipamento:

```text
Cadastro
   ↓
Disponível
   ↓
Empréstimo
   ↓
Equipamento em uso
   ↓
Devolução
   ↓
Disponível novamente
```

O sistema possui controle de:

- usuários;
- categorias;
- equipamentos;
- disponibilidade;
- empréstimos;
- devoluções;
- histórico de movimentações.

Além das operações CRUD tradicionais, o projeto utiliza recursos do PostgreSQL para executar consultas e regras de negócio diretamente no banco de dados.


---

<a id="objetivo"></a>

# 🎯 Objetivo

O objetivo do AssetFlow é oferecer uma solução simples para o controle de equipamentos destinados a empréstimos.

Além disso, o projeto demonstra na prática a integração entre uma aplicação desktop e recursos de Banco de Dados.

A arquitetura básica pode ser representada por:

```text
AssetFlow
   ↓
PySide6
   ↓
Python
   ↓
psycopg
   ↓
PostgreSQL
   ↓
View / Function / Procedure
```

[⬆ Voltar ao topo](#topo)

---

<a id="tecnologias"></a>

# 🛠 Tecnologias utilizadas

| Tecnologia | Utilização |
|---|---|
| **Python** | Desenvolvimento da aplicação |
| **PySide6** | Interface gráfica desktop |
| **PostgreSQL** | Banco de dados |
| **psycopg** | Conexão entre Python e PostgreSQL |
| **SQL** | Consultas e manipulação dos dados |
| **PL/pgSQL** | Function e Procedure |
| **Git** | Controle de versão |
| **GitHub** | Hospedagem e documentação do projeto |


---

<a id="funcionalidades"></a>

# ✨ Principais funcionalidades

O AssetFlow possui as seguintes áreas principais:

```text
01. Dashboard

02. Usuários

03. Categorias

04. Equipamentos

05. Novo Empréstimo

06. Empréstimos Ativos

07. Devolução

08. Histórico
```

---

<a id="dashboard"></a>

## 📊 Dashboard

O Dashboard apresenta uma visão geral das principais informações do sistema.

São exibidos dados como:

- quantidade de usuários cadastrados;
- total de equipamentos;
- equipamentos disponíveis;
- equipamentos emprestados;
- equipamentos em manutenção;
- empréstimos ativos.

Também é apresentada uma visualização dos empréstimos atualmente em andamento.

<img width="1911" height="993" alt="AssetFlow-img1" src="https://github.com/user-attachments/assets/4a7dd793-f2e6-4db6-a868-217b4dfd7e5d" />


---

<a id="usuarios"></a>

## 👤 Gerenciamento de usuários

A tela de usuários permite cadastrar e gerenciar as pessoas que podem realizar empréstimos no sistema.

Cada usuário possui:

- código;
- nome;
- e-mail;
- telefone;
- tipo;
- status.

Os tipos disponíveis são:

```text
ALUNO

PROFESSOR

FUNCIONARIO
```

Os possíveis status são:

```text
ATIVO

INATIVO
```

Entre as funcionalidades disponíveis estão:

- cadastrar usuário;
- pesquisar;
- editar;
- excluir;
- atualizar a listagem.

<img width="1917" height="988" alt="AssetFlow-img2" src="https://github.com/user-attachments/assets/09325773-b3af-4c11-a2d3-d2fdb9827c2d" />

---

<a id="categorias"></a>

## 🗂 Categorias

As categorias são utilizadas para organizar os equipamentos cadastrados no AssetFlow.

Algumas categorias utilizadas no sistema são:

```text
Notebook

Projetor

Tablet

Câmera

Kit Arduino
```

A tela permite:

- cadastrar;
- pesquisar;
- editar;
- excluir;
- visualizar informações das categorias.

<img width="1917" height="988" alt="AssetFlow-img3" src="https://github.com/user-attachments/assets/d7705c92-0601-4513-b896-e0b17ffe05a4" />



---

<a id="equipamentos"></a>

## 💻 Equipamentos

A tela de equipamentos concentra o gerenciamento dos itens disponíveis no sistema.

Cada equipamento possui informações como:

- código;
- nome;
- patrimônio;
- categoria;
- descrição;
- status.

Os possíveis status são:

```text
DISPONIVEL

EMPRESTADO

MANUTENCAO

INATIVO
```

O sistema também permite pesquisar equipamentos pelo nome ou patrimônio.

<img width="1917" height="986" alt="AssetFlow-img4" src="https://github.com/user-attachments/assets/3f8ddf8d-c314-4171-8c44-b8312d108759" />


A disponibilidade dos equipamentos também pode ser consultada através de uma **Function criada no PostgreSQL**.


---

<a id="novo-emprestimo"></a>

## 📤 Novo empréstimo

A tela **Novo Empréstimo** permite registrar a retirada de um equipamento.

Para realizar a operação são informados:

- usuário;
- equipamento;
- data prevista para devolução.

Antes da operação ser concluída, o sistema verifica se o equipamento está disponível.

<img width="1917" height="988" alt="AssetFlow-img5" src="https://github.com/user-attachments/assets/1fb22620-e3e5-4abb-8e61-88e0cc4317cf" />


A operação utiliza diretamente a Procedure:

```sql
realizar_emprestimo()
```

Quando o empréstimo é realizado:

```text
Empréstimo registrado
        +
Equipamento alterado para EMPRESTADO
```

---

<a id="emprestimos-ativos"></a>

## 📋 Empréstimos ativos

Essa tela apresenta todos os empréstimos que ainda estão em andamento.

São exibidas informações como:

- código do empréstimo;
- usuário;
- tipo do usuário;
- equipamento;
- patrimônio;
- categoria;
- data do empréstimo;
- data prevista para devolução.

<img width="1916" height="993" alt="AssetFlow-img6" src="https://github.com/user-attachments/assets/9904d7d1-5ad4-4205-b0b7-623e31a7ed73" />


Os dados dessa tela são obtidos diretamente através da View:

```sql
vw_emprestimos_ativos
```

A aplicação executa:

```sql
SELECT *
FROM vw_emprestimos_ativos;
```


---

<a id="devolucao"></a>

## 📥 Devolução

A tela de devolução permite selecionar um empréstimo ativo e registrar o retorno do equipamento.

<img width="1912" height="988" alt="AssetFlow-img7" src="https://github.com/user-attachments/assets/86c9455b-ff7d-480f-baf9-e665f4b57ce6" />


Após registrar a devolução:

```text
EMPRÉSTIMO

ATIVO
  ↓
FINALIZADO
```

e:

```text
EQUIPAMENTO

EMPRESTADO
    ↓
DISPONIVEL
```

A data de devolução também é registrada no banco de dados.


---

<a id="historico"></a>

## 🕒 Histórico

A tela de histórico permite consultar os empréstimos realizados no sistema.

São apresentadas informações como:

- código;
- usuário;
- equipamento;
- patrimônio;
- data do empréstimo;
- previsão de devolução;
- data da devolução;
- status.

<img width="1915" height="987" alt="AssetFlow-img8" src="https://github.com/user-attachments/assets/0f0c4bd9-e1a8-401a-b718-bf3071e50650" />


Dessa forma, é possível acompanhar tanto empréstimos ativos quanto empréstimos já finalizados.


---

<a id="banco"></a>

# 🗄 Banco de Dados

O AssetFlow utiliza o **PostgreSQL** como Sistema Gerenciador de Banco de Dados.

Nome do banco:

```text
assetflow
```

O banco possui quatro tabelas principais:

```text
usuario

categoria

equipamento

emprestimo
```

## Relacionamentos

```text
CATEGORIA
    │
   1:N
    │
    ▼
EQUIPAMENTO
    │
   1:N
    │
    ▼
EMPRESTIMO
    ▲
    │
   N:1
    │
USUARIO
```

As cardinalidades podem ser representadas como:

```text
CATEGORIA   (1) -------- (N) EQUIPAMENTO

EQUIPAMENTO (1) -------- (N) EMPRESTIMO

USUARIO     (1) -------- (N) EMPRESTIMO
```

### Principais regras

- um usuário pode realizar vários empréstimos;
- um equipamento pode aparecer em vários empréstimos ao longo do tempo;
- cada equipamento pertence a uma categoria;
- usuários inativos não podem realizar empréstimos;
- equipamentos indisponíveis não podem ser emprestados;
- o patrimônio de um equipamento deve ser único;
- o e-mail de cada usuário deve ser único.


---

<a id="view"></a>

<a id="view"></a>

# 👁 View

## `vw_emprestimos_ativos`

A View `vw_emprestimos_ativos` foi criada para reunir em uma única consulta os principais dados relacionados aos empréstimos que ainda estão ativos.

Ela utiliza informações das tabelas:

- `emprestimo`;
- `usuario`;
- `equipamento`;
- `categoria`.

### Código da View

```sql
CREATE OR REPLACE VIEW vw_emprestimos_ativos AS
SELECT
    emp.id_emprestimo,
    u.nome AS usuario,
    u.tipo_usuario,
    eq.nome AS equipamento,
    eq.patrimonio,
    c.nome AS categoria,
    emp.data_emprestimo,
    emp.data_prevista_devolucao

FROM emprestimo emp

JOIN usuario u
ON emp.id_usuario = u.id_usuario

JOIN equipamento eq
ON emp.id_equipamento = eq.id_equipamento

JOIN categoria c
ON eq.id_categoria = c.id_categoria

WHERE emp.status = 'ATIVO';
```

### Consulta da View

```sql
SELECT *
FROM vw_emprestimos_ativos;
```

### O que ela retorna?

A View apresenta:

- ID do empréstimo;
- nome do usuário;
- tipo do usuário;
- equipamento;
- patrimônio;
- categoria;
- data do empréstimo;
- data prevista para devolução.

### Onde é utilizada?

Na tela:

**Empréstimos Ativos**

### Fluxo

```text
Tela Empréstimos Ativos
        ↓
SELECT *
FROM vw_emprestimos_ativos
        ↓
PostgreSQL
        ↓
Dados apresentados na aplicação
```

[⬆ Voltar ao topo](#topo)

---

<a id="function"></a>

# ⚙ Function

## `verificar_disponibilidade()`

A Function `verificar_disponibilidade` recebe o ID de um equipamento e consulta o seu status no banco de dados.

Se o equipamento estiver com status `DISPONIVEL`, a Function retorna `TRUE`.

Caso contrário, retorna `FALSE`.

### Código da Function

```sql
CREATE OR REPLACE FUNCTION verificar_disponibilidade(
    p_id_equipamento INTEGER
)
RETURNS BOOLEAN
LANGUAGE plpgsql
AS $$

DECLARE
    v_status VARCHAR(20);

BEGIN

    SELECT status
    INTO v_status
    FROM equipamento
    WHERE id_equipamento = p_id_equipamento;


    IF v_status = 'DISPONIVEL' THEN
        RETURN TRUE;
    ELSE
        RETURN FALSE;
    END IF;

END;

$$;
```

### Exemplo de utilização

```sql
SELECT verificar_disponibilidade(1);
```

Se o equipamento estiver disponível:

```text
TRUE
```

Caso esteja emprestado, em manutenção ou inativo:

```text
FALSE
```

### Onde é utilizada?

A Function é utilizada pela aplicação para verificar se determinado equipamento pode ser emprestado.

### Fluxo

```text
Equipamento selecionado
        ↓
verificar_disponibilidade(id)
        ↓
PostgreSQL
        ↓
TRUE / FALSE
        ↓
Disponível / Indisponível
```

[⬆ Voltar ao topo](#topo)

---

<a id="procedure"></a>

# 🔄 Procedure

## `realizar_emprestimo()`

A Procedure `realizar_emprestimo` é responsável por realizar o processo de empréstimo de um equipamento.

Ela recebe três parâmetros:

- ID do usuário;
- ID do equipamento;
- data prevista para devolução.

Durante sua execução, a Procedure verifica se o usuário está ativo, verifica se o equipamento está disponível, registra o empréstimo e altera o status do equipamento para `EMPRESTADO`.

### Código da Procedure

```sql
CREATE OR REPLACE PROCEDURE realizar_emprestimo(
    p_id_usuario INTEGER,
    p_id_equipamento INTEGER,
    p_data_prevista_devolucao DATE
)

LANGUAGE plpgsql

AS $$

DECLARE
    v_status_usuario VARCHAR(20);
    v_status_equipamento VARCHAR(20);

BEGIN

    -- Consulta o status do usuário

    SELECT status
    INTO v_status_usuario
    FROM usuario
    WHERE id_usuario = p_id_usuario;


    -- Verifica se o usuário está ativo

    IF v_status_usuario <> 'ATIVO' THEN
        RAISE EXCEPTION
        'Usuário não está ativo';
    END IF;


    -- Consulta o status do equipamento

    SELECT status
    INTO v_status_equipamento
    FROM equipamento
    WHERE id_equipamento = p_id_equipamento;


    -- Verifica se o equipamento está disponível

    IF v_status_equipamento <> 'DISPONIVEL' THEN
        RAISE EXCEPTION
        'Equipamento não está disponível';
    END IF;


    -- Registra o empréstimo

    INSERT INTO emprestimo (
        id_usuario,
        id_equipamento,
        data_prevista_devolucao
    )

    VALUES (
        p_id_usuario,
        p_id_equipamento,
        p_data_prevista_devolucao
    );


    -- Altera o status do equipamento

    UPDATE equipamento
    SET status = 'EMPRESTADO'
    WHERE id_equipamento = p_id_equipamento;

END;

$$;
```

### Exemplo de execução

```sql
CALL realizar_emprestimo(
    1,
    1,
    '2026-10-15'
);
```

### Consulta após a execução

```sql
SELECT *
FROM emprestimo;
```

### O que a Procedure faz?

```text
1. Consulta o status do usuário

2. Verifica se o usuário está ATIVO

3. Consulta o status do equipamento

4. Verifica se o equipamento está DISPONIVEL

5. Registra o empréstimo

6. Altera o status do equipamento para EMPRESTADO
```

### Onde é utilizada?

Na tela:

**Novo Empréstimo**

### Fluxo

```text
Tela Novo Empréstimo
        ↓
Usuário + Equipamento + Data
        ↓
CALL realizar_emprestimo(...)
        ↓
PostgreSQL
        ↓
INSERT em emprestimo
        +
UPDATE em equipamento
        ↓
Resultado apresentado na aplicação
```

[⬆ Voltar ao topo](#topo)
---

<a id="integracao"></a>

# 🔗 Integração aplicação + banco

Um dos principais objetivos do AssetFlow é demonstrar que o banco de dados não é utilizado apenas para armazenar registros.

Parte das consultas e regras de negócio são executadas diretamente pelo PostgreSQL.

```text
┌───────────────────────────┐
│         AssetFlow         │
│          PySide6          │
└─────────────┬─────────────┘
              │
              ▼
           Python
              │
              ▼
           psycopg
              │
              ▼
┌───────────────────────────┐
│        PostgreSQL         │
│                           │
│  Tables                   │
│  View                     │
│  Function                 │
│  Procedure                │
└───────────────────────────┘
```

## Recursos utilizados

| Recurso | Implementação | Utilização |
|---|---|---|
| **View** | `vw_emprestimos_ativos` | Tela Empréstimos Ativos |
| **Function** | `verificar_disponibilidade()` | Verificação de equipamentos |
| **Procedure** | `realizar_emprestimo()` | Realização de empréstimos |

[⬆ Voltar ao topo](#topo)

---

<a id="estrutura"></a>

# 📁 Estrutura do projeto

A organização do projeto segue uma estrutura semelhante a:

```text
AssetFlow/
│
├── src/
│   ├── main.py
│   ├── database.py
│   └── ...
│
├── database/
│   │
│   ├── tables/
│   │
│   ├── inserts/
│   │
│   ├── views/
│   │
│   ├── functions/
│   │
│   └── procedures/
│
├── requirements.txt
│
└── README.md
```

> As imagens e o vídeo de demonstração são inseridos diretamente neste README através dos anexos do GitHub.

[⬆ Voltar ao topo](#topo)

---


---

<a id="conceitos"></a>

# 📚 Conceitos aplicados

Durante o desenvolvimento do AssetFlow foram utilizados conceitos como:

- modelagem de Banco de Dados;
- chave primária (`PRIMARY KEY`);
- chave estrangeira (`FOREIGN KEY`);
- cardinalidade;
- `NOT NULL`;
- `UNIQUE`;
- `DEFAULT`;
- `CHECK`;
- `SELECT`;
- `INSERT`;
- `UPDATE`;
- `DELETE`;
- `JOIN`;
- `SELECT INTO`;
- `IF / ELSE`;
- View;
- Function;
- Procedure;
- CRUD;
- regras de negócio;
- integração Python + PostgreSQL.

[⬆ Voltar ao topo](#topo)

---

<a id="academico"></a>

# 🎓 Contexto acadêmico

O **AssetFlow** foi desenvolvido como trabalho avaliativo da disciplina de **Banco de Dados**.

O objetivo acadêmico do projeto é demonstrar a evolução de uma aplicação CRUD através da utilização prática de recursos mais avançados do PostgreSQL.

## Identificação

**Aluno:** Giovane Ferreira Paes Ribeiro
**Curso:** Engenharia de Software  
**Disciplina:** Banco de Dados  
**Professor:** Anderson Soares Costa

[⬆ Voltar ao topo](#topo)

---

<a id="autor"></a>

# 👨‍💻 Autor

Desenvolvido por **Giovane Ferreira Paes Ribeiro**

---

<a id="status"></a>

# ✅ Status do projeto

### AssetFlow 1.0

- [x] Dashboard
- [x] CRUD de usuários
- [x] CRUD de categorias
- [x] CRUD de equipamentos
- [x] Pesquisa de registros
- [x] Controle de disponibilidade
- [x] Realização de empréstimos
- [x] Empréstimos ativos
- [x] Registro de devoluções
- [x] Histórico
- [x] Integração Python + PostgreSQL
- [x] View PostgreSQL
- [x] Function PostgreSQL
- [x] Procedure PostgreSQL

### 🟢 Projeto concluído e funcional

---

<p align="center">
  <strong>AssetFlow</strong><br>
  Desenvolvido com Python, PySide6 e PostgreSQL.
</p>

<p align="center">
  <a href="#topo">⬆ Voltar ao topo</a>
</p>
