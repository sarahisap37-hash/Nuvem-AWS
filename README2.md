Aqui está a documentação do seu laboratório organizada em **Markdown**, pronta para usar no README 👇

---

# 📘 Laboratório 1: Introdução ao AWS IAM

## 📌 O que é o AWS IAM

O **AWS Identity and Access Management (IAM)** é um serviço da AWS que permite gerenciar usuários, credenciais de segurança e permissões de acesso aos recursos da nuvem de forma centralizada.

Com o IAM, é possível:

* Criar usuários e grupos
* Definir permissões
* Controlar acessos a serviços da AWS

---

## 🎯 Objetivos do Laboratório

Este laboratório tem como objetivo:

* Explorar usuários e grupos IAM pré-criados
* Analisar políticas de acesso
* Simular um cenário real de permissões
* Utilizar o URL de login do IAM
* Testar permissões de acesso aos serviços

---

## ⏱️ Duração

Tempo estimado: **40 minutos**

---
---

## 🔐 Conceitos Importantes do IAM

###  Usuários

* Representam pessoas ou aplicações
* Possuem credenciais (senha, chave de acesso, MFA)

###  Grupos

* Conjunto de usuários
* Permissões atribuídas ao grupo são herdadas pelos usuários

###  Funções (Roles)

* Identidades assumidas temporariamente
* Usadas por serviços ou usuários

###  Políticas

Definem permissões através de:

* **Effect** → Allow ou Deny
* **Action** → ações permitidas (ex: `ec2:DescribeInstances`)
* **Resource** → recursos afetados

---

##  Acesso ao Console AWS

1. Clique em **Iniciar Laboratório**
2. Aguarde o ambiente iniciar
3. Clique no link da AWS
4. Permita pop-ups se necessário
5. Abra o console em uma nova aba

---

## 🧪 Tarefa 1: Explorar Usuários e Grupos

###  Usuários criados:

* user-1
* user-2
* user-3

###  Observações:

* user-1 não possui permissões
* user-1 não pertence a grupos
* possui apenas senha de acesso

---

### 👥 Grupos disponíveis:

* EC2-Admin
* EC2-Support
* S3-Support

---

### 📜 Políticas dos grupos:

#### EC2-Support

* Política: `AmazonEC2ReadOnlyAccess`
* Permite:

  * Visualizar recursos EC2
  * Sem permissão de alteração

#### S3-Support

* Política: `AmazonS3ReadOnlyAccess`
* Permite:

  * Listar e visualizar buckets S3

#### EC2-Admin

* Política Inline
* Permite:

  * Visualizar instâncias
  * Iniciar e parar instâncias EC2

---

## 💼 Cenário de Negócio

| Usuário | Grupo       | Permissão      |
| ------- | ----------- | -------------- |
| user-1  | S3-Support  | Leitura no S3  |
| user-2  | EC2-Support | Leitura no EC2 |
| user-3  | EC2-Admin   | Gerenciar EC2  |

---

##  Tarefa 2: Adicionar Usuários aos Grupos

###  user-1 → S3-Support

* Ganha acesso de leitura ao S3

###  user-2 → EC2-Support

* Ganha acesso de leitura ao EC2

###  user-3 → EC2-Admin

* Ganha permissões administrativas no EC2

 Ao final:
* Cada grupo deve conter **1 usuário**

---

## 🧪 Tarefa 3: Testar Usuários

###  Login IAM

* Copiar URL de login
* Abrir janela anônima
* Testar acessos

---

###  user-1

*  Acessa S3 (somente leitura)
*  Não acessa EC2

---

###  user-2

*  Visualiza EC2
*  Não pode alterar instâncias
*  Não acessa S3

---

###  user-3

*  Visualiza EC2
*  Pode parar instâncias
*  Possui permissões administrativas

---

## 📤 Submissão

1. Clique em **Enviar**
2. Aguarde o processamento
3. Verifique a nota
4. Consulte o relatório se necessário

⚠️ Pode ser necessário aguardar alguns minutos para pontuação completa

---

## ✅ Conclusão

Neste laboratório você:

* Explorou usuários e grupos IAM
* Analisou políticas de acesso
* Aplicou permissões em um cenário real
* Testou diferentes níveis de acesso
* Entendeu o funcionamento do controle de acesso na AWS

---

## 🏁 Finalização

* Clique em **Finalizar Laboratório**
* Confirme a ação
* Encerre o ambiente

---


