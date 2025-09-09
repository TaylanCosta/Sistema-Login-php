# Sistema de Login e Cadastro em PHP

Este é um projeto simples de sistema de login e cadastro desenvolvido para fins de aprendizado, utilizando as tecnologias:

- **HTML**  para a interface.
- **PHP** para a lógica de back-end.
- **MySQL** para o banco de dados.

## Funcionalidades

- **Cadastro de Usuário:** Permite que novos usuários se registrem com nome de usuário, e-mail e senha.
- **Login de Usuário:** Autentica usuários existentes e inicia uma sessão.
- **Proteção de Rota:** Redireciona usuários não logados que tentam acessar páginas restritas.
- **Logout:** Encerra a sessão do usuário.
- **Segurança:** Utiliza `password_hash()` e `password_verify()` para armazenar senhas de forma segura.

## Estrutura do Projeto

O projeto é composto pelos seguintes arquivos:

- `cadastro.php`: Página com o formulário de cadastro e a lógica de registro.
- `login.php`: Página com o formulário de login e a lógica de autenticação.
- `dashboard.php`: Página restrita, acessível apenas após o login.
- `logout.php`: Encerra a sessão e redireciona para a página de login.
- `conexao.php`: Arquivo de configuração para a conexão com o banco de dados.

## Como Usar

### Pré-requisitos

- Servidor local (como XAMPP, WAMP ou MAMP) com PHP e MySQL instalados e rodando.

### Configuração

1.  **Clone o repositório** ou baixe os arquivos para a pasta `htdocs` (ou `www`) do seu servidor local.
2.  **Crie um banco de dados** com o nome `sistema_login` no phpMyAdmin.
3.  **Crie a tabela `usuarios`** executando o seguinte código SQL:

    ```sql
    CREATE TABLE usuarios (
        id INT AUTO_INCREMENT PRIMARY KEY,
        nome_de_usuario VARCHAR(50) NOT NULL UNIQUE,
        email VARCHAR(100) NOT NULL UNIQUE,
        senha VARCHAR(255) NOT NULL,
        data_de_criacao TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```
4.  **Ajuste o arquivo `conexao.php`** com as suas credenciais do banco de dados (usuário, senha e porta, se necessário).

### Acessando as Páginas

Após a configuração, você pode acessar as páginas no seu navegador:

- **Cadastro:** `http://localhost/seu-projeto/cadastro.php`
- **Login:** `http://localhost/seu-projeto/login.php`

---

## Contribuição

Sinta-se à vontade para fazer um "fork" do projeto, sugerir melhorias ou reportar problemas.

---
