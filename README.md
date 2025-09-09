# 🧪 Teste de Login

Este documento descreve os cenários de teste para a funcionalidade de **login** do sistema.

---

## 📌 Objetivo
Validar se o processo de autenticação permite que usuários válidos acessem o sistema e que usuários inválidos sejam corretamente bloqueados, garantindo segurança e usabilidade.

---

## ⚙️ Pré-requisitos
- Ambiente de testes configurado.
- Usuário válido cadastrado:
  - **E-mail:** usuario@teste.com  
  - **Senha:** Senha123
- Navegador atualizado / Emulador de dispositivo (se mobile).
- Ferramenta de automação (opcional): Cypress, Selenium, Playwright, etc.

---

## 🔍 Cenários de Teste

### ✅ Cenário 1: Login com credenciais válidas
- **Dado** que o usuário está na tela de login  
- **Quando** ele informa e-mail e senha válidos  
- **Então** deve acessar o sistema e visualizar o dashboard inicial  

### ❌ Cenário 2: Login com senha inválida
- **Dado** que o usuário está na tela de login  
- **Quando** ele informa e-mail válido e senha incorreta  
- **Então** deve visualizar a mensagem: *"Usuário ou senha inválidos"*  

### ❌ Cenário 3: Login com e-mail inválido
- **Dado** que o usuário está na tela de login  
- **Quando** ele informa um e-mail inexistente e qualquer senha  
- **Então** deve visualizar a mensagem: *"Usuário ou senha inválidos"*  

### ⚠️ Cenário 4: Campos obrigatórios em branco
- **Dado** que o usuário está na tela de login  
- **Quando** ele tenta logar sem preencher os campos  
- **Então** deve visualizar a mensagem: *"Preencha os campos obrigatórios"*  

### 🔄 Cenário 5: Lembrar senha (opcional)
- **Dado** que o usuário esqueceu a senha  
- **Quando** ele clica em *“Esqueci minha senha”*  
- **Então** deve ser redirecionado para o fluxo de recuperação de senha  

---

## 🛠️ Ferramentas Sugeridas
- **Cypress** para automação web
- **Appium** para automação mobile
- **Postman** para validação de API de login

---

## 📊 Critérios de Aceite
- Usuário válido deve conseguir logar sem erros.
- Usuário inválido deve ser bloqueado com mensagens claras.
- Mensagens de erro devem ser exibidas de forma consistente.
- A tela de login deve manter acessibilidade e usabilidade.

---

## 📌 Observações
- Garantir que o login esteja protegido contra ataques de força bruta.  
- Testar diferentes navegadores/dispositivos.  
- Validar regras de complexidade de senha, caso aplicável.  

---

✍️ **Autor:** [Seu Nome]  
📅 **Data:** 08/09/2025
