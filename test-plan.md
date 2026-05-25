# 📋 Test Plan

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

TC - 02 — Registro com dados já utilizados

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

TC - 03 — Validação do campo "Nome" obrigatório

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

---

TC-04 — Registro com senha diferente da confirmação

**Pré-condição:**
Usuário não cadastrado no sistema

**Passos:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir e-mail válido  
4. Inserir nome válido  
5. Inserir senha válida  
6. Inserir uma senha diferente no campo de confirmação  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**
Sistema deve impedir o cadastro e exibir mensagem informando que as senhas não coincidem

**Resultado atual:**
Sistema bloqueia o cadastro e exibe mensagem informando divergência entre as senhas

**Status:**
Aprovado

---

TC-05 — Registro com e-mail já cadastrado

**Pré-condição:**
Usuário já cadastrado no sistema

**Passos:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir um e-mail já cadastrado  
4. Inserir nome válido  
5. Inserir senha válida  
6. Confirmar a senha corretamente  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**
Sistema deve impedir o cadastro e exibir mensagem informando que o e-mail já está em uso

**Resultado atual:**
Sistema permitiu o cadastro de um novo usuário utilizando um e-mail já cadastrado, sem exibir mensagem de erro ou bloqueio

**Status:**
Reprovado (Bug 003)

---

TC-06 — Registro com formato de e-mail inválido

**Pré-condição:**
Nenhuma

**Passos:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir um e-mail em formato inválido (ex: teste@ ou teste.com)  
4. Inserir nome válido  
5. Inserir senha válida  
6. Confirmar a senha corretamente  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**
Sistema deve impedir o cadastro e exibir mensagem informando que o e-mail é inválido  

**Resultado atual:**
Sistema permitiu o cadastro com e-mail em formato inválido, desde que contenha o caractere "@"

**Status:**
Reprovado (BUG-004)

---

TC-07 — Registro com espaços em branco nos campos

**Pré-condição:**
Nenhuma

**Passos:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir e-mail com espaços antes e depois (ex: "   teste@email.com   ")  
4. Inserir nome com espaços (ex: "   Andressa   ")  
5. Inserir senha válida  
6. Confirmar a senha corretamente  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**
Sistema deve remover os espaços automaticamente ou impedir o cadastro com dados inválidos  

**Resultado atual:**
Sistema permitiu o cadastro com o campo "Nome" preenchido apenas com espaços

**Status:**
Reprovado (BUG-005)

---

TC-08 — Registro com senha contendo apenas espaços

**Pré-condição:**
Nenhuma

**Passos:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir e-mail válido  
4. Inserir nome válido  
5. Inserir apenas espaços no campo "Senha" (ex: "     ")  
6. Inserir apenas espaços no campo "Confirmar senha"  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**
Sistema deve impedir o cadastro e exibir mensagem informando que a senha é inválida ou não pode conter apenas espaços  

**Resultado atual:**
Sistema permitiu o cadastro com senha composta apenas por espaços, desde que os campos coincidam

**Status:**
Reprovado (BUG-006)
