🐞 Bugs encontrados

---

BUG-001 — Campos de registro permanecem preenchidos ao reutilizar a tela

**Descrição:**  
Ao acessar a tela de registro novamente, os campos permanecem previamente preenchidos, permitindo a criação de uma nova conta com os mesmos dados.

---

**Passos para reproduzir:**
1. Acessar a tela de registro  
2. Preencher todos os campos obrigatórios  
3. Criar uma conta com sucesso  
4. Retornar à tela de registro  
5. Observar os campos já preenchidos  
6. Submeter novamente o formulário  

---

**Resultado esperado:**  
Os campos devem ser resetados ao acessar a tela de registro novamente, impedindo reutilização automática dos dados.

---

**Resultado atual:**  
Os campos permanecem preenchidos, permitindo o cadastro de múltiplas contas com os mesmos dados.

---

**Prioridade:**  
Média  

---

BUG 002 - Validação inconsistente do campo "Nome" no cadastro

**Descrição:**  
O sistema apresenta comportamentos diferentes na validação do campo "Nome". Inicialmente, não exibe erro para o campo vazio, mas após preencher outros campos, a validação ocorre de forma diferente, exibindo mensagem em formato de modal.

---

**Passos para reproduzir:**
1. Acessar a tela de registro  
2. Clicar no botão "Registrar" sem preencher nenhum campo  
3. Observar que os campos "Email", "Senha" e "Confirmar senha" são marcados como obrigatórios  
4. Preencher os campos "Email", "Senha" e "Confirmar senha", deixando o campo "Nome" vazio  
5. Clicar novamente no botão "Registrar"  

---

**Resultado esperado:**  
O sistema deve validar todos os campos obrigatórios de forma consistente, exibindo mensagem de erro abaixo do campo "Nome" quando estiver vazio.

---

**Resultado atual:**  
O sistema apresenta comportamento inconsistente:
- Inicialmente, não valida o campo "Nome"  
- Após preenchimento dos outros campos, exibe mensagem em modal informando que o campo "Nome" não pode ser vazio  

--- 

**Prioridade:**  
Média  

---

**Impacto:**  
- Inconsistência na validação de formulário  
- Experiência do usuário confusa  
- Falta de padronização nas mensagens de erro  

---
 
