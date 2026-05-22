# 📋 Test Cases

## 🧪 Funcionalidade: Login

---

TC-01 — Novo registro com campos válidos

**Pré-condição:**
Usuário não cadastrado no sistema

**Passos:**
1. Acessar a página de login
2. Clicar no botão "Registrar"
3. Inserir e-mail válido
4. Inserir nome válido
5. Inserir senha válida
6. Inserir senha válida para confirmação
7. Clicar no botão "Cadastrar"

**Resultado esperado:**
Usuário deve ser cadastrado corretamente 

**Resultado atual:**
Usuário foi cadastrado corretamente na plataforma

**Status:**
Aprovado

---

TC-02 — Novo registro com campos válidos

**Pré-condição:**
Usuário não cadastrado no sistema

**Passos:**
1. Acessar a página de login
2. Clicar no botão "Registrar"
3. Inserir e-mail válido
4. Inserir nome válido
5. Inserir senha válida
6. Inserir senha válida para confirmação
7. Clicar no botão "Cadastrar"

**Resultado esperado:**
Usuário deve ser cadastrado corretamente 

**Resultado atual:**
Usuário foi cadastrado corretamente na plataforma

**Status:**
Aprovado

TC - 03 — Registro com dados já utilizados

**Pré-condição:**
Usuário já cadastrado no sistema

**Passos:**
1. Acessar a tela de registro  
2. Preencher todos os campos obrigatórios  
3. Realizar cadastro com sucesso  
4. Retornar à tela de registro  
5. Submeter novamente os mesmos dados  

**Resultado esperado:**
Sistema não deve permitir cadastro duplicado ou deve exigir novos dados

**Resultado atual:**
Sistema permite novo cadastro com os mesmos dados

**Status:**
Reprovado (BUG-001)

---

TC - 04 — Validação do campo "Nome" obrigatório

**Pré-condição:**
Nenhuma

**Passos:**
1. Acessar a tela de registro  
2. Clicar em "Registrar" sem preencher os campos  
3. Preencher "Email", "Senha" e "Confirmar senha"  
4. Deixar o campo "Nome" vazio  
5. Clicar em "Registrar"  

**Resultado esperado:**
Sistema deve exibir mensagem de erro abaixo do campo "Nome"

**Resultado atual:**
Sistema não valida inicialmente e depois exibe erro em formato de modal

**Status:**
Reprovado (BUG-002)
