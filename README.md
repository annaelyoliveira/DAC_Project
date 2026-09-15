# ✈️ Sistema de Gerenciamento de Viagens Acadêmicas e Eventos

Plataforma web voltada para a centralização, organização e controle de inscrições em viagens acadêmicas e eventos institucionais. O sistema busca otimizar a relação entre alunos e organizadores, automatizando o controle de vagas, a coleta segura de dados pessoais/bancários e a gestão do fluxo de aprovação dos editais.

---

## 📌 Sumário
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades e Regras de Negócio](#-funcionalidades-e-regras-de-negócio)
- [Perfis de Acesso (Roles)](#-perfis-de-acesso-roles)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)

---

## 📖 Sobre o Projeto

O projeto resolve a descentralização de informações no processo de candidatura a viagens acadêmicas. Através da plataforma:
- **Monitores** submetem propostas de editais com detalhes do evento, orçamentos e horários.
- **Coordenadores** realizam a curadoria e aprovação dos editais submetidos.
- **Estudantes** consultam vagas abertas, realizam inscrições e acompanham o status de aprovação administrativa e financeira (com potencial integração via SUAP).

---

## ⚡ Funcionalidades e Regras de Negócio

- **Submissão de Editais:** Cadastro com detalhamento de vagas, custo por pessoa, datas, projeto/disciplina associado e organizadores.
- **Aprovação em Duas Etapas:** O edital nasce como `PENDENTE` e só fica visível publicamente após a aprovação do Coordenador (`APROVADO`).
- **Inscrição e Ajuda de Custo:** Formulário adaptativo que coleta dados bancários (PIX, banco, agência, conta) apenas se o estudante solicitar auxílio financeiro.
- **Auto-cadastro de Monitores:** Estudantes podem se cadastrar diretamente como Monitores no sistema, definindo suas credenciais de acesso.
- **Controle de Acesso Fino:** Monitores consultam inscritos e relatórios **apenas** dos editais sob sua autoria. Coordenadores possuem acesso irrestrito.
- **Validação de Vaga:** Cancelamento automático por estouro de prazo limite caso o estudante não confirme a participação.

---

## 👥 Perfis de Acesso (Roles)

| Perfil | Descrição | Permissões |
| :--- | :--- | :--- |
| **`ESTUDANTE`** | Acesso público / Alunos | Visualiza editais aprovados, se inscreve em viagens e cadastra-se como Monitor. |
| **`MONITOR`** | Aluno organizador autenticado | Submete editais, consulta inscritos e gera relatórios dos seus próprios editais. |
| **`COORDENADOR`** | Gestor responsável autenticado | Aprova/Rejeita editais submetidos, gerencia qualquer edital e lista de inscritos. |

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem:** Java 21+
- **Framework:** Spring Boot (Spring Data JPA, Spring Security, Spring Web)
- **Banco de Dados:** PostgreSQL
- **Documentação da API:** Swagger
- **Modelagem UML:** Astah Professional
- **Gerenciador de Dependências:** Maven

---
