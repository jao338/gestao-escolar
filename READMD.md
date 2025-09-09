# Projeto Integrador – Sistema de Gestão Universitária

## 📌 Tema
Modelagem e Prototipação de um Sistema Orientado a Objetos para gestão de dados de uma universidade.  

O projeto segue as orientações de UML (Unified Modeling Language) para auxiliar no entendimento da modelagem, prototipação e futura implementação do sistema.

---

## 📍 Primeira Entrega – Modelagem UML

### 🔹 Diagrama de Caso de Uso
O sistema contempla o cadastro e gerenciamento de diferentes tipos de pessoas vinculadas à universidade.  

![Diagrama de Caso de Uso](1%20-%20CASO%20DE%20USO.jpg)

### 🔹 Cenários dos Casos de Uso

#### 1) Cadastro de Pessoa Física
- **Cenário Principal:** O administrador acessa o sistema, informa os dados da pessoa física e confirma o cadastro.  
- **Cenário Alternativo 1:** Administrador tenta cadastrar um CPF já existente → o sistema bloqueia e informa duplicidade.  
- **Cenário Alternativo 2:** Administrador deixa campos obrigatórios em branco → o sistema alerta e não finaliza.  
- **Pré-condição:** O administrador deve estar autenticado no sistema.  
- **Pós-condição:** Pessoa Física cadastrada com sucesso e disponível para consulta.  

#### 2) Cadastro de Pessoa Jurídica
- **Cenário Principal:** O administrador informa CNPJ e razão social e confirma o cadastro.  
- **Cenário Alternativo 1:** CNPJ já cadastrado → sistema informa duplicidade.  
- **Cenário Alternativo 2:** Falta de dados obrigatórios → sistema alerta e impede cadastro.  
- **Pré-condição:** Administrador autenticado.  
- **Pós-condição:** Pessoa Jurídica cadastrada e disponível no sistema.  

#### 3) Cadastro de Professor
- **Cenário Principal:** O administrador acessa o cadastro de pessoa física e inclui dados de professor (SIAPE, departamento).  
- **Cenário Alternativo 1:** SIAPE já cadastrado → sistema bloqueia.  
- **Cenário Alternativo 2:** Dados obrigatórios faltando → sistema solicita correção.  
- **Pré-condição:** Pessoa Física cadastrada previamente.  
- **Pós-condição:** Professor cadastrado e vinculado à universidade.  

#### 4) Cadastro de Aluno
- **Cenário Principal:** Administrador acessa cadastro de pessoa física e insere matrícula e curso.  
- **Cenário Alternativo 1:** Matrícula já existente → bloqueio do sistema.  
- **Cenário Alternativo 2:** Curso inexistente ou inválido → sistema alerta.  
- **Pré-condição:** Pessoa Física cadastrada previamente.  
- **Pós-condição:** Aluno cadastrado com sucesso.  

#### 5) Cadastro de Fornecedor
- **Cenário Principal:** Administrador cadastra fornecedor a partir de pessoa jurídica, informando tipo de serviço e contato.  
- **Cenário Alternativo 1:** Fornecedor já existente → sistema alerta.  
- **Cenário Alternativo 2:** Tipo de serviço não informado → sistema impede cadastro.  
- **Pré-condição:** Pessoa Jurídica cadastrada previamente.  
- **Pós-condição:** Fornecedor cadastrado com sucesso.  

---

### 🔹 Diagrama de Classes
O sistema foi modelado com as seguintes classes principais:  

![Diagrama de Classes](2%20-%20CLASSES.jpg)

- **Pessoa**: classe base com atributos comuns (nome, telefone, e-mail).  
- **Pessoa Física**: herda de Pessoa, possui CPF e método de validação.  
- **Pessoa Jurídica**: herda de Pessoa, possui CNPJ e razão social.  
- **Aluno**: herda de Pessoa Física, possui matrícula e curso.  
- **Professor**: herda de Pessoa Física, possui SIAPE e departamento.  
- **Fornecedor**: herda de Pessoa Jurídica, possui tipo de serviço e contato.  

---

## 📍 Segunda Entrega – Prototipação

### 🔹 Protótipos
Os protótipos foram criados no [Figma].  

As jornadas contempladas:
- Cadastro de Pessoa Física  
- Cadastro de Pessoa Jurídica  
- Cadastro de Professores  
- Cadastro de Fornecedores  
- Cadastro de Alunos  

### 🔹 Repositório GitHub
O projeto está hospedado no GitHub para versionamento e colaboração da equipe.  

🔗 [Link para o Repositório](https://github.com/jao338/gestao-escolar.git)  

---

## ✅ Conclusão
O sistema foi modelado em UML (diagramas de casos de uso e classes) e prototipado em ferramenta de design. A modelagem reflete os requisitos da universidade para cadastro e gestão de pessoas físicas, jurídicas, professores, alunos e fornecedores.


