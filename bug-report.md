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

**Impacto:**  
- Possibilidade de criação de contas duplicadas  
- Inconsistência na base de dados  
- Experiência de usuário inadequada  
