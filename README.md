# 🍽️ Aplicativo Coma Bem

## 📖 Sobre o Projeto

O **Coma Bem** é um aplicativo mobile desenvolvido para conectar amantes da culinária a bons restaurantes locais. O projeto foi desenvolvido como parte da disciplina de **Banco de Dados Mobile**, utilizando Flutter e SQLite para proporcionar uma aplicação organizada, segura e eficiente.

O sistema permite o gerenciamento de usuários, restaurantes e informações cadastradas, aplicando conceitos de Programação Orientada a Objetos e persistência de dados em banco de dados local.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Dart
- **Framework:** Flutter
- **Banco de Dados:** SQLite (sqflite)
- **Gerenciamento de Caminhos:** path
- **Padrões de Projeto:** Orientação a Objetos, DAO (Data Access Object)

---

## 🗄️ Modelagem do Banco de Dados

O banco de dados relacional foi construído respeitando as regras de normalização (1FN, 2FN e 3FN), evitando redundâncias e garantindo integridade das informações.

As principais tabelas do sistema são:

1. **Usuários**
2. **Clientes**
3. **Administradores**
4. **Donos de Restaurante**

---

## 🧩 Arquitetura e Orientação a Objetos

O sistema foi desenvolvido utilizando os principais pilares da Programação Orientada a Objetos.

### 🔒 Encapsulamento

Todos os atributos das classes são privados (`_atributo`), sendo acessados através de métodos *getters* e *setters*, garantindo segurança e validação dos dados.

### 🧬 Herança

As classes **Cliente**, **Administrador** e **DonoRestaurante** herdam características da classe base **Usuário**, reutilizando atributos e comportamentos comuns.

### 🔄 Polimorfismo

Cada tipo de usuário possui sua própria implementação do método `exibirMenu()`, permitindo que o sistema apresente menus diferentes conforme o perfil autenticado.

---

## 💾 Transações e Regras de Negócio

A classe `DatabaseHelper` centraliza toda a comunicação com o banco SQLite.

As operações implementadas seguem o padrão CRUD:

- **Create:** Cadastro de usuários e restaurantes.
- **Read:** Consulta e listagem das informações armazenadas.
- **Update:** Atualização dos dados cadastrados.
- **Delete:** Exclusão de registros do banco de dados.

As consultas utilizam parâmetros para evitar problemas como SQL Injection.

---

## 🚀 Como Executar o Projeto

1. Clone este repositório.

```bash
git clone https://github.com/ArthurFelis/Coma_Bem.git
```

2. Acesse a pasta do projeto.

```bash
cd Coma_Bem
```

3. Instale as dependências.

```bash
flutter pub get
```

4. Certifique-se de possuir um emulador Android ou um dispositivo físico conectado.

5. Execute o projeto.

```bash
flutter run
```

---

## 📂 Estrutura do Projeto

```
lib/
├── database/
│   ├── database_helper.dart
│   └── dao/
├── models/
│   ├── usuario.dart
│   ├── cliente.dart
│   ├── administrador.dart
│   └── dono_restaurante.dart
├── screens/
├── widgets/
└── main.dart
```

---

## ✨ Funcionalidades

- Cadastro de usuários
- Login de usuários
- Cadastro de restaurantes
- Persistência de dados utilizando SQLite
- Operações CRUD
- Menus específicos para cada perfil de usuário
- Aplicação dos conceitos de Herança, Encapsulamento e Polimorfismo

---

## 👨‍💻 Desenvolvido por

**Arthur Felis Silva Ferreira**

Disciplina de Banco de Dados Mobile.