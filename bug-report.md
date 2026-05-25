## 🐞 Bugs Encontrados

---

BUG-001 — Campos de registro permanecem preenchidos ao reutilizar a tela

**Descrição:**  
Ao acessar a tela de registro novamente, os campos permanecem previamente preenchidos, permitindo a criação de uma nova conta com os mesmos dados.

**Passos para reproduzir:**
1. Acessar a tela de registro  
2. Preencher todos os campos obrigatórios  
3. Criar uma conta com sucesso  
4. Retornar à tela de registro  
5. Observar os campos já preenchidos  
6. Submeter novamente o formulário  

**Resultado esperado:**  
Os campos devem ser resetados ao acessar a tela de registro novamente, impedindo reutilização automática dos dados.

**Resultado atual:**  
Os campos permanecem preenchidos, permitindo o cadastro de múltiplas contas com os mesmos dados.

**Prioridade:**  
Média  

---

BUG 002 - Validação inconsistente do campo "Nome" no cadastro

**Descrição:**  
O sistema apresenta comportamentos diferentes na validação do campo "Nome". Inicialmente, não exibe erro para o campo vazio, mas após preencher outros campos, a validação ocorre de forma diferente, exibindo mensagem em formato de modal.

**Passos para reproduzir:**
1. Acessar a tela de registro  
2. Clicar no botão "Registrar" sem preencher nenhum campo  
3. Observar que os campos "Email", "Senha" e "Confirmar senha" são marcados como obrigatórios  
4. Preencher os campos "Email", "Senha" e "Confirmar senha", deixando o campo "Nome" vazio  
5. Clicar novamente no botão "Registrar"  

**Resultado esperado:**  
O sistema deve validar todos os campos obrigatórios de forma consistente, exibindo mensagem de erro abaixo do campo "Nome" quando estiver vazio.

**Resultado atual:**  
O sistema apresenta comportamento inconsistente:
- Inicialmente, não valida o campo "Nome"  
- Após preenchimento dos outros campos, exibe mensagem em modal informando que o campo "Nome" não pode ser vazio  

**Prioridade:**  
Média  

**Impacto:**  
- Inconsistência na validação de formulário  
- Experiência do usuário confusa  
- Falta de padronização nas mensagens de erro  

---
 BUG-003 — Permite cadastro com e-mail já cadastrado

**Descrição:**  
O sistema permite o cadastro de múltiplas contas utilizando o mesmo e-mail, sem apresentar qualquer validação ou bloqueio.

**Passos para reproduzir:**
1. Acessar a tela de registro  
2. Realizar cadastro com um e-mail válido  
3. Retornar à tela de registro  
4. Inserir o mesmo e-mail já cadastrado  
5. Preencher os demais campos corretamente  
6. Clicar em "Cadastrar"  

**Resultado esperado:**  
O sistema deve impedir o cadastro e exibir mensagem informando que o e-mail já está em uso  

**Resultado atual:**  
O sistema permite o cadastro com o mesmo e-mail, sem apresentar validação  

**Prioridade:**  
Alta  

**Impacto:**  
- Duplicidade de contas  
- Inconsistência na base de dados  
- Possível falha de segurança  

---

BUG-004 — Validação incorreta de formato de e-mail no cadastro

**Descrição:**  
O sistema aceita e-mails em formato inválido durante o cadastro, desde que contenham o caractere "@", sem validar corretamente a estrutura completa do e-mail.

**Passos para reproduzir:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir um e-mail inválido (ex: teste@ ou @email.com)  
4. Preencher os demais campos corretamente  
5. Clicar no botão "Cadastrar"  

**Resultado esperado:**  
O sistema deve validar o formato completo do e-mail e impedir o cadastro com dados inválidos, exibindo mensagem de erro  

**Resultado atual:**  
O sistema permite o cadastro com e-mails inválidos, desde que contenham o caractere "@"  

**Prioridade:**  
Média  

**Impacto:**  
- Cadastro de dados inválidos na base  
- Possível falha na comunicação com o usuário (ex: envio de e-mails)  
- Baixa qualidade dos dados cadastrados  

---

BUG-005 — Permite cadastro com campo "Nome" contendo apenas espaços

**Descrição:**  
O sistema permite o cadastro de usuário quando o campo "Nome" é preenchido apenas com espaços em branco, sem validar corretamente o conteúdo inserido.

**Passos para reproduzir:**
1. Acessar a página de login  
2. Clicar no botão "Registrar"  
3. Inserir e-mail válido  
4. Inserir apenas espaços no campo "Nome" (ex: "     ")  
5. Inserir senha válida  
6. Confirmar a senha corretamente  
7. Clicar no botão "Cadastrar"  

**Resultado esperado:**  
O sistema deve impedir o cadastro e exibir mensagem informando que o campo "Nome" é obrigatório e não pode conter apenas espaços  

**Resultado atual:**  
O sistema permite o cadastro mesmo com o campo "Nome" preenchido apenas com espaços em branco  

**Prioridade:**  
Média  

**Impacto:**  
- Cadastro de dados inválidos na base  
- Comprometimento da qualidade das informações  
- Possíveis problemas em funcionalidades que utilizam o nome do usuário  

---


