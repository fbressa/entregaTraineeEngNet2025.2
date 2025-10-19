# Casos de Uso – Gym Rats

## Descrição
A elaboração de casos de uso isa descrever as funcionalidades do sistema sob a perspectiva dos usuários, permitindo uma visão geral dos serviços oferecidos pelo sistema e da interação entre os atores.

## UC-01: Cadastrar Novo Usuário
**Ator Principal:** Novo Usuário  
**Objetivo:** Criar uma nova conta no aplicativo para poder participar das competições.  
**Pré-condições:** O usuário não possui uma conta existente com o e-mail fornecido.  
**Pós-condições:**  
- Uma nova conta de usuário é criada no sistema com status "não validado".  
- Um e-mail de validação é enviado para o endereço de e-mail fornecido.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário seleciona a opção "Criar Conta".  
2. O sistema exibe um formulário solicitando nome, e-mail e senha.  
3. O usuário preenche os dados e confirma.  
4. O sistema valida os dados e cria a conta.  
5. O sistema exibe uma mensagem instruindo o usuário a verificar seu e-mail para validar a conta.  

**Fluxos Alternativos:**  
- **A1: E-mail já em uso:**  
  - No passo 4, se o e-mail já estiver cadastrado:  
    - O sistema exibe uma mensagem de erro: "Este e-mail já está em uso."  
    - O fluxo retorna ao passo 3.  

---

## UC-02: Realizar Login com E-mail e Senha
**Ator Principal:** Usuário  
**Objetivo:** Acessar as funcionalidades restritas do aplicativo de forma segura.  
**Pré-condições:**  
- O usuário deve ter uma conta cadastrada e validada.  
- O usuário deve estar na tela de autenticação.  
**Pós-condições:** O usuário está autenticado no sistema e visualiza a tela principal.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário insere seu e-mail e senha.  
2. O usuário clica no botão "Entrar".  
3. O sistema verifica se as credenciais são válidas.  
4. O sistema autentica o usuário e exibe a tela principal.  

**Fluxos Alternativos:**  
- **A1: Credenciais Inválidas:**  
  - No passo 3, se as credenciais estiverem incorretas:  
    - O sistema exibe uma mensagem: "E-mail ou senha inválidos".  
    - O fluxo retorna ao passo 1.  
- **A2: Login via conta Google/Apple:**  
  1. O usuário clica na opção de login social.  
  2. O sistema redireciona para a autenticação do provedor.  
  3. Após autorização, o sistema autentica o usuário.  

---

## UC-03: Recuperar Senha de Acesso
**Ator Principal:** Usuário  
**Objetivo:** Redefinir a senha para recuperar o acesso à conta.  
**Pré-condições:** O usuário está na tela de login.  
**Pós-condições:** A senha do usuário é atualizada no sistema.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário clica em "Esqueci minha senha".  
2. O sistema solicita o e-mail da conta.  
3. O usuário insere seu e-mail e confirma.  
4. O sistema envia um link seguro para o e-mail do usuário.  
5. O usuário clica no link e cadastra uma nova senha.  

**Fluxos Alternativos:**  
- **A1: E-mail não encontrado:**  
  - No passo 4, se o e-mail não estiver cadastrado:  
    - O sistema exibe uma mensagem de erro genérica: "Se o e-mail estiver correto, você receberá um link."  

---

## UC-04: Realizar Logout
**Ator Principal:** Usuário  
**Objetivo:** Encerrar a sessão de forma segura.  
**Pré-condições:** O usuário está autenticado no sistema.  
**Pós-condições:** O usuário é deslogado e vê a tela de login.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário navega até o menu ou perfil.  
2. O usuário clica na opção "Sair" (Logout).  
3. O sistema encerra a sessão e redireciona para a tela de login.  

**Fluxos Alternativos:**  
- N/A  

---

## UC-05: Apagar Conta
**Ator Principal:** Usuário  
**Objetivo:** Remover permanentemente sua conta e dados.  
**Pré-condições:** O usuário está autenticado no sistema.  
**Pós-condições:** A conta e os dados do usuário são removidos do sistema.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário navega até as configurações do perfil.  
2. O usuário clica na opção "Apagar Conta".  
3. O sistema exibe um aviso e solicita confirmação.  
4. O usuário confirma a exclusão.  
5. O sistema remove permanentemente a conta.  

**Fluxos Alternativos:**  
- **A1: Usuário cancela a exclusão:**  
  - No passo 4, se o usuário não confirmar:  
    - O fluxo é encerrado e o usuário permanece na tela de configurações.  

---

## UC-06: Criar Grupo de Competição
**Ator Principal:** Usuário  
**Objetivo:** Criar um novo espaço privado para uma competição.  
**Pré-condições:** O usuário está autenticado.  
**Pós-condições:**  
- Um novo grupo é criado.  
- O ator se torna o administrador do novo grupo.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário seleciona "Criar Grupo".  
2. O sistema exibe um formulário (nome, descrição, regras).  
3. O usuário preenche os dados e confirma.  
4. O sistema cria o grupo e exibe sua tela principal.  

**Fluxos Alternativos:**  
- **A1: Campos Obrigatórios Vazios:**  
  - No passo 4, se um campo obrigatório não for preenchido:  
    - O sistema exibe uma mensagem de erro.  
    - O fluxo retorna ao passo 3.  

---

## UC-07: Entrar em Grupo via Código
**Ator Principal:** Usuário  
**Objetivo:** Participar de uma competição existente.  
**Pré-condições:**  
- O usuário está autenticado.  
- O usuário possui um código de convite.  
**Pós-condições:** O usuário é adicionado como membro do grupo.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário seleciona a opção "Entrar em Grupo".  
2. O usuário insere o código de convite e confirma.  
3. O sistema valida o código e adiciona o usuário ao grupo.  

**Fluxos Alternativos:**  
- **A1: Código Inválido:**  
  - No passo 3, se o código for inválido:  
    - O sistema exibe uma mensagem de erro.  
    - O fluxo retorna ao passo 2.  

---

## UC-08: Registrar Atividade Manualmente
**Ator Principal:** Usuário  
**Objetivo:** Adicionar uma nova atividade física para contabilizar pontos.  
**Pré-condições:** O usuário é membro de pelo menos um grupo.  
**Pós-condições:**  
- A atividade é registrada.  
- A pontuação é calculada e somada ao ranking.  

**Fluxo Principal (Caminho Feliz):**
1. O usuário seleciona "Registrar Atividade".  
2. O sistema exibe um formulário para inserção de dados (duração, distância, etc.).  
3. O usuário preenche os dados e salva.  
4. O sistema salva a atividade, calcula os pontos e atualiza o ranking.  

**Fluxos Alternativos:**  
- **A1: Dados Inválidos:**  
  - No passo 4, se os dados forem inválidos (ex: duração igual a zero):  
    - O sistema destaca os campos com erro.  
    - O fluxo retorna ao passo 3.  

---

## UC-09: Interagir no Feed do Grupo
**Ator Principal:** Usuário  
**Objetivo:** Engajar com outros membros através de posts e comentários.  
**Pré-condições:** O usuário é membro do grupo.  
**Pós-condições:** O feed do grupo é atualizado com a nova interação.  

**Fluxo Principal (Caminho Feliz):**
- **Fluxo A: Realizar Post:**  
  1. O usuário acessa o feed do grupo.  
  2. O usuário cria um novo post (texto e/ou mídia).  
  3. O usuário publica o post.  
- **Fluxo B: Comentar/Reagir:**  
  1. O usuário visualiza um post.  
  2. O usuário escreve um comentário ou seleciona uma reação.  

**Fluxos Alternativos:**  
- N/A  

---

## UC-10: Gerenciar Grupo (Admin)
**Ator Principal:** Administrador  
**Objetivo:** Gerenciar as configurações e membros do grupo.  
**Pré-condições:** O ator é administrador do grupo.  
**Pós-condições:** As configurações ou a lista de membros do grupo são atualizadas.  

**Fluxo Principal (Caminho Feliz):**
- **Fluxo A: Editar Configurações:**  
  1. O Admin edita nome, descrição ou regras.  
  2. O Admin salva as alterações.  
- **Fluxo B: Remover Membro:**  
  1. O Admin seleciona um membro.  
  2. O Admin confirma a remoção.  

**Fluxos Alternativos:**  
- **A1: Tentativa de remover o último admin:**  
  - No Fluxo B, se o admin tentar se remover ou remover o último admin:  
    - O sistema exibe um erro, instruindo a promover outro membro primeiro.  
