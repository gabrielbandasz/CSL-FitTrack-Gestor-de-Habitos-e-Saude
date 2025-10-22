# 🏋️ FitTrack - Sistema de Gestão de Treinos

Este projeto é um sistema de gerenciamento de usuários e treinos desenvolvido em Java utilizando a biblioteca Swing. O FitTrack permite cadastrar usuários, registrar treinos e acessar o sistema através de login seguro, com uma interface gráfica intuitiva.
---

## 📌 Funcionalidades

- [x] Tela de Login para autenticação de usuários 
- [x] Tela de Cadastro de Usuário
- [x] Tela de Cadastro de Treino  
- [x] Tela Inicial (Menu) para navegação entre funcionalidades
- [x] Controle de treinos por usuário  
- [x] Interface gráfica amigável e intuitiva  

---

## 🎯 Tecnologias Utilizadas
- 💻 Java SE
- 🧱 Java Swing (para a interface gráfica)
- 🧰 IDE: Recomendado NetBeans ou IntelliJ IDEA
- 🗄️ Banco de Dados: MySQL
---

## 🛠️ Como Usar

1. Clone o repositório:
   ```bash
   git clone https://github.com/Gabrielsande/FitTrack.git
 - Abra o projeto no NetBeans (ou sua IDE favorita)
 - Compile e execute a classe CalculadoraJFrame

---

---

## 📁 Estrutura do ProjetoFitTrack/
```
FitTrack
├── src/
│   └── br/ulbra/controller/         
│   ├── br/ulbra/model/        # Classes modelo (Usuário, Treino)
│   ├── br/ulbra/view/         # Telas (Login, Cadastro, Menu)
│   └── br/ulbra/dao/          # DAO para manipulação do banco
│   └── br/ulbra/view/          # DAO para manipulação do banco
├── lib/                       # Bibliotecas externas (se houver)
```
## 🖥️ Telas do Sistema

O sistema **FitTrack** foi desenvolvido com **Java Swing**, possuindo uma interface intuitiva e amigável, organizada em múltiplas telas que facilitam o uso e a navegação.

### 🔐 Tela de Login
- Permite que o usuário acesse o sistema com **usuário** e **senha**.
- Valida os dados no banco de dados.
- Exibe mensagens de erro caso o login seja inválido.

**Funcionalidades:**
- Login seguro
- Validação de credenciais
- Acesso direto à tela inicial após autenticação

---

### 🧍‍♂️ Tela de Cadastro de Usuário
- Responsável por registrar novos usuários no sistema.
- Inclui campos como: **Nome**, **E-mail**, **Senha**, e **Tipo de Usuário** (Administrador ou Comum).
- Os dados são armazenados diretamente no banco de dados MySQL.

**Funcionalidades:**
- Inserção de novos usuários
- Edição e exclusão de usuários cadastrados
- Visualização dos dados em tabela

---

### 💪 Tela de Cadastro de Treino
- Nesta tela, o usuário pode cadastrar seus treinos diários.
- Campos: **Nome do Treino**, **Tipo de Treino**, **Duração**, **Calorias Queimadas** e **Data do Treino**.
- Exibe uma tabela com todos os treinos registrados.

**Funcionalidades:**
- Adicionar novos treinos
- Editar informações
- Excluir registros
- Listagem geral de treinos cadastrados

---

### 🏠 Tela Inicial (Menu)
- Tela principal do sistema após o login.
- Permite navegar entre as telas de **Cadastro de Usuário**, **Cadastro de Treino** e **Logout**.

**Funcionalidades:**
- Navegação intuitiva
- Acesso rápido às principais áreas do sistema
- Interface simples e responsiva (para desktop)

---

## 🧠 Metodologia Utilizada

O projeto foi desenvolvido utilizando a **metodologia ágil Scrum**, com sprints curtos e reuniões de acompanhamento semanais.

### 🧩 Papéis no Time:
- **Scrum Master:** Gabriel Bandasz  
- **Product Owner (PO):** Gabriel Sandes  
- **Desenvolvedores:** Pedro Flores, Lucas Matheus, Joaquim Guedes e Leonardo Schimmit  

---

## Mockup 
<img width="1280" height="800" alt="1" src="https://github.com/user-attachments/assets/b3ce7101-01df-446c-8293-0399dd567aa7" />
<img width="1280" height="800" alt="2" src="https://github.com/user-attachments/assets/76314818-95b8-4c0f-a9de-1f68090d04fa" />
<img width="1280" height="800" alt="3" src="https://github.com/user-attachments/assets/44318cdb-efc1-4444-b3bc-a0f51a9a9c92" />
<img width="1280" height="800" alt="4" src="https://github.com/user-attachments/assets/7795d9c0-131e-428a-9150-949e11461b40" />
<img width="1280" height="800" alt="5" src="https://github.com/user-attachments/assets/aba6c268-4066-4297-9f8a-fe6e7730b9f4" />

---

## 🗄️ Banco de dados

O **FitTrack** utiliza o **MySQL/MariaDB** para armazenar os dados de usuários e treinos. O banco de dados é chamado `academia` e possui duas tabelas principais: `usuario` e `treino`.

### Criação do schema e tabelas

```sql
CREATE DATABASE IF NOT EXISTS academia;
USE academia;

CREATE TABLE usuario (
  id_usuario INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(80) NOT NULL,
  idade INT,
  peso DECIMAL(5,2),
  altura DECIMAL(4,2),
  senha VARCHAR(200) NOT NULL
);

CREATE TABLE treino (
  id_treino INT AUTO_INCREMENT PRIMARY KEY,
  tipo VARCHAR(50),
  duracao INT,
  calorias INT,
  data_treino VARCHAR(15),
  id_usuario INT,
  FOREIGN KEY (id_usuario) REFERENCES usuario(id_usuario)
);
```
## 🏫 Contexto Acadêmico

Este projeto foi desenvolvido como parte do **Curso Técnico em Informática** do  
**Colégio São Lucas**, com o objetivo de aplicar conceitos de **Programação Orientada a Objetos**, **Banco de Dados** e **Desenvolvimento de Interfaces Gráficas**.

---


## 👨‍💻 Autores

- Scrum Master: Gabriel Bandasz
- Product Owner (PO): Gabriel Sandes
- Desenvolvedores (DEVs):
- Pedro Flores
- Lucas Matheus
- Joaquim Guedes
- Leonardo Schimmit
