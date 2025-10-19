# Casos de Uso – Gym Rats

## Descrição
A elaboração de casos de uso **visa** descrever as funcionalidades do sistema sob a perspectiva dos usuários, permitindo uma visão geral dos serviços oferecidos e da interação entre os atores.

---

## Índice
- [UC-01: Cadastrar Novo Usuário](#uc-01-cadastrar-novo-usuário)
- [UC-02: Realizar Login com E-mail e Senha](#uc-02-realizar-login-com-e-mail-e-senha)
- [UC-03: Recuperar Senha de Acesso](#uc-03-recuperar-senha-de-acesso)
- [UC-04: Realizar Logout](#uc-04-realizar-logout)
- [UC-05: Apagar Conta](#uc-05-apagar-conta)
- [UC-06: Criar Grupo de Competição](#uc-06-criar-grupo-de-competição)
- [UC-07: Entrar em Grupo via Código](#uc-07-entrar-em-grupo-via-código)
- [UC-08: Registrar Atividade Manualmente](#uc-08-registrar-atividade-manualmente)
- [UC-09: Interagir no Feed do Grupo](#uc-09-interagir-no-feed-do-grupo)
- [UC-10: Gerenciar Grupo (Admin)](#uc-10-gerenciar-grupo-admin)

---

## UC-01: Cadastrar Novo Usuário
**Ator Principal:** Novo Usuário  
**Objetivo:** Criar uma nova conta no aplicativo para poder participar das competições.

**Pré-condições**
- O usuário não possui uma conta existente com o e-mail fornecido.

**Pós-condições**
- Conta de usuário criada com status **“não validado”**.
- E-mail de validação enviado ao endereço informado.

**Fluxo Principal (Caminho Feliz)**
1. O usuário seleciona **“Criar Conta”**.  
2. O sistema exibe formulário solicitando **nome**, **e-mail** e **senha**.  
3. O usuário preenche os dados e confirma.  
4. O sistema valida os dados e cria a conta.  
5. O sistema exibe instrução para verificar o e-mail e validar a conta.

**Fluxos Alternativos**
- **A1 — E-mail já em uso**  
  4.1. O sistema exibe: *“Este e-mail já está em uso.”*  
  4.2. Retorna ao passo **3**.

---

## UC-02: Realizar Login com E-mail e Senha
**Ator Principal:** Usuário  
**Objetivo:** Acessar funcionalidades restritas de forma segura.

**Pré-condições**
- Conta cadastrada e **validada**.  
- Usuário na tela de autenticação.

**Pós-condições**
- Usuário autenticado e visualizando a **tela principal**.

**Fluxo Principal (Caminho Feliz)**
1. O usuário insere **e-mail** e **senha**.  
2. Clica em **“Entrar”**.  
3. O sistema verifica as credenciais.  
4. O sistema autentica e exibe a tela principal.

**Fluxos Alternativos**
- **A1 — Credenciais inválidas**  
  3.1. O sistema exibe: *“E-mail ou senha inválidos.”*  
  3.2. Retorna ao passo **1**.
- **A2 — Login via Google/Apple**  
  1. O usuário seleciona **login social**.  
  2. Redirecionamento para o provedor.  
  3. Após autorização, o sistema autentica o usuário.

---

## UC-03: Recuperar Senha de Acesso
**Ator Principal:** Usuário  
**Objetivo:** Redefinir a senha para recuperar o acesso.

**Pré-condições**
- Usuário na tela de **login**.

**Pós-condições**
- Senha do usuário **atualizada**.

**Fluxo Principal (Caminho Feliz)**
1. O usuário clica em **“Esqueci minha senha”**.  
2. O sistema solicita o **e-mail** da conta.  
3. O usuário informa o e-mail e confirma.  
4. O sistema envia **link seguro** por e-mail.  
5. O usuário acessa o link e cadastra **nova senha**.

**Fluxos Alternativos**
- **A1 — E-mail não encontrado**  
  4.1. Mensagem genérica por segurança: *“Se o e-mail estiver correto, você receberá um link.”*

---

## UC-04: Realizar Logout
**Ator Principal:** Usuário  
**Objetivo:** Encerrar a sessão com segurança.

**Pré-condições**
- Usuário **autenticado**.

**Pós-condições**
- Sessão encerrada; exibição da tela de **login**.

**Fluxo Principal (Caminho Feliz)**
1. Usuário acessa **menu** ou **perfil**.  
2. Clica em **“Sair (Logout)”**.  
3. Sistema encerra a sessão e redireciona para **login**.

**Fluxos Alternativos**
- *Não aplicável.*

---

## UC-05: Apagar Conta
**Ator Principal:** Usuário  
**Objetivo:** Remover permanentemente sua conta e dados.

**Pré-condições**
- Usuário **autenticado**.

**Pós-condições**
- Conta e dados do usuário **removidos** do sistema.

**Fluxo Principal (Caminho Feliz)**
1. Usuário abre **Configurações do perfil**.  
2. Clica em **“Apagar Conta”**.  
3. Sistema exibe **aviso** e solicita **confirmação**.  
4. Usuário **confirma**.  
5. Sistema remove a conta.

**Fluxos Alternativos**
- **A1 — Usuário cancela**  
  4.1. Sem confirmação, o fluxo é encerrado e o usuário permanece em **Configurações**.

---

## UC-06: Criar Grupo de Competição
**Ator Principal:** Usuário  
**Objetivo:** Criar novo espaço privado para competição.

**Pré-condições**
- Usuário **autenticado**.

**Pós-condições**
- **Grupo criado**.  
- Criador torna-se **administrador**.

**Fluxo Principal (Caminho Feliz)**
1. Usuário seleciona **“Criar Grupo”**.  
2. Sistema exibe formulário (**nome**, **descrição**, **regras**).  
3. Usuário preenche e confirma.  
4. Sistema cria o grupo e exibe a tela do grupo.

**Fluxos Alternativos**
- **A1 — Campos obrigatórios vazios**  
  4.1. Sistema exibe erros de validação.  
  4.2. Retorna ao passo **3**.

---

## UC-07: Entrar em Grupo via Código
**Ator Principal:** Usuário  
**Objetivo:** Participar de uma competição existente.

**Pré-condições**
- Usuário **autenticado**.  
- Possui **código de convite** válido.

**Pós-condições**
- Usuário adicionado como **membro** do grupo.

**Fluxo Principal (Caminho Feliz)**
1. Usuário seleciona **“Entrar em Grupo”**.  
2. Informa o **código** e confirma.  
3. Sistema valida e adiciona o usuário ao grupo.

**Fluxos Alternativos**
- **A1 — Código inválido**  
  3.1. Sistema exibe mensagem de erro.  
  3.2. Retorna ao passo **2**.

---

## UC-08: Registrar Atividade Manualmente
**Ator Principal:** Usuário  
**Objetivo:** Adicionar atividade física e contabilizar pontos.

**Pré-condições**
- Usuário é membro de **ao menos um** grupo.

**Pós-condições**
- Atividade **registrada**.  
- Pontos **calculados** e **somados** ao ranking.

**Fluxo Principal (Caminho Feliz)**
1. Usuário seleciona **“Registrar Atividade”**.  
2. Sistema exibe formulário (ex.: **duração**, **distância**, etc.).  
3. Usuário preenche e **salva**.  
4. Sistema registra, **calcula pontos** e **atualiza o ranking**.

**Fluxos Alternativos**
- **A1 — Dados inválidos**  
  4.1. Sistema destaca campos com erro (ex.: **duração = 0**).  
  4.2. Retorna ao passo **3**.

---

## UC-09: Interagir no Feed do Grupo
**Ator Principal:** Usuário  
**Objetivo:** Engajar com membros via posts e comentários.

**Pré-condições**
- Usuário é **membro** do grupo.

**Pós-condições**
- Feed do grupo **atualizado** com a interação.

**Fluxo Principal (Caminho Feliz)**
- **Fluxo A — Realizar Post**  
  1. Acessa o **feed**.  
  2. Cria novo post (texto e/ou mídia).  
  3. Publica o post.  
- **Fluxo B — Comentar/Reagir**  
  1. Visualiza um post.  
  2. Escreve **comentário** ou registra **reação**.

**Fluxos Alternativos**
- *Não aplicável.*

---

## UC-10: Gerenciar Grupo (Admin)
**Ator Principal:** **Administrador**  
**Objetivo:** Gerenciar configurações e membros do grupo.

**Pré-condições**
- Usuário possui papel de **administrador** do grupo.

**Pós-condições**
- Configurações e/ou lista de membros **atualizadas**.

**Fluxo Principal (Caminho Feliz)**
- **Fluxo A — Editar Configurações**  
  1. Admin edita **nome**, **descrição** ou **regras**.  
  2. Admin **salva** alterações.  
- **Fluxo B — Remover Membro**  
  1. Admin seleciona um **membro**.  
  2. Admin **confirma** a remoção.

**Fluxos Alternativos**
- **A1 — Tentativa de remover o último admin**  
  2.1. Sistema bloqueia a ação e informa: **promova outro membro** antes de remover o último admin.

---
