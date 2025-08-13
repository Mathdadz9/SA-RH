# 🧾 Sistema de Recrutamento Online

Este projeto é uma aplicação web simples voltada para recrutamento e seleção de candidatos. Ele permite que **usuários comuns** se cadastrem, criem currículos e visualizem vagas disponíveis, enquanto **administradores** podem gerenciar as vagas e visualizar currículos recebidos.

---

## 📌 Etapa 2: Levantamento do Escopo

### 🎯 Objetivo

Criar um sistema que permita a interação entre candidatos e equipe de RH por meio de funcionalidades básicas de cadastro, login, visualização e gerenciamento de informações.

---

## 👤 Tipos de Usuário

### Usuário Comum

- Cadastro de conta
- Login no sistema
- Cadastro de currículo
- Visualização de vagas

### Administrador

- Login com credenciais específicas
- Cadastro, edição e exclusão de vagas
- Visualização de currículos recebidos

---

## ✅ Funcionalidades Requeridas

### Usuário Comum

- **Cadastro de Conta**
  - Campos: nome, e-mail, senha
  - E-mail deve ser único
- **Login**
  - Autenticação por e-mail e senha
- **Cadastro de Currículo**
  - Informações: formação, experiência, habilidades etc.
- **Visualização de Vagas**
  - Listagem com título, descrição, requisitos e outros detalhes

---

### Administrador

- **Login**
  - Acesso via e-mail e senha definidos no banco de dados (`db.json`)
- **Gerenciamento de Vagas**
  - Criar, editar e excluir vagas
  - Campos: título, descrição, requisitos, salário, localidade
- **Visualização de Currículos**
  - Lista de currículos cadastrados pelos usuários

---

## 🗃️ Estrutura dos Dados (`db.json`)

```json
{
  "usuarios": [
    {
      "id": 1,
      "email": "admin@rh.com",
      "senha": "admin123",
      "tipo": "admin"
    }
  ],
  "curriculos": [],
  "vagas": []
}
Tabelas
usuarios

id: número

email: string

senha: string

tipo: "admin" ou "usuario"

curriculos

id, usuarioId, formacao, experiencia, habilidades, etc.

vagas

id, titulo, descricao, requisitos, salario, localidade

🔐 Regras de Acesso
Apenas usuários com "tipo": "admin" acessam a área administrativa

Usuários comuns visualizam apenas suas informações e as vagas

🧪 Testes Esperados
✅ Login com dados válidos e inválidos

✅ Cadastro de novos usuários com validação de e-mail

✅ Criação e edição de currículos

✅ Ações de CRUD em vagas (admin)

✅ Restrições de acesso entre usuários e administradores

