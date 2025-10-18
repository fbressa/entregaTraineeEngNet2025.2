## 1. Autenticação e Gestão de Conta

| ID   | Nome do Requisito                        | Descrição                                                                                                                                                                                                 | Prioridade  |
|------|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF1  | Realizar login com e-mail e senha        | O sistema deve permitir que usuários realizem login com e-mail e senha.                                                                                                                                  | Must Have    |
| RF2  | Permitir login via conta Google          | O sistema deve permitir login usando conta do Google.                                                                                                                                                    | Could Have   |
| RF3  | Permitir login via conta Apple           | O sistema deve permitir login usando conta da Apple.                                                                                                                                                     | Could Have   |
| RF4  | Recuperar senha de acesso                | O sistema deve oferecer funcionalidade de recuperação de senha. Este fluxo deve permitir que o usuário insira seu e-mail para receber um link seguro e redefinir sua senha.                              | Must Have    |
| RF5  | Validar conta com confirmação por e-mail | O sistema deve exigir confirmação de e-mail para validação de conta. Após o cadastro, um e-mail com um link de ativação será enviado ao usuário, que deverá ser acessado para validar a conta.           | Should Have  |
| RF6  | Realizar logout do aplicativo            | O sistema deve permitir que o usuário faça logout do aplicativo.                                                                                                                                         | Must Have    |
| RF7  | Apagar conta de usuário                  | O sistema deve permitir que o usuário apague a conta.                                                                                                                                                    | Must Have    |

---

## 2. Gestão de Grupos

| ID   | Nome do Requisito                    | Descrição                                                                                                                                                                               | Prioridade  |
|------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF8  | Criar grupo de competição            | O sistema deve permitir que o usuário crie um grupo de competição.                                                                                                                      | Must Have    |
| RF9  | Entrar em grupo existente via código | O sistema deve permitir que o usuário entre em um grupo existente (via código).                                                                                                        | Must Have    |
| RF10 | Gerar código de convite para o grupo | O sistema deve gerar um código de convite único e compartilhável para que outros usuários possam entrar no grupo.                                                                       | Must Have    |
| RF11 | Visualizar lista de membros do grupo | O sistema deve permitir que o usuário visualize a lista de membros de um grupo.                                                                                                        | Should Have  |
| RF12 | Remover membros do grupo (Admin)     | O sistema deve permitir que um administrador remova membros do grupo.                                                                                                                   | Should Have  |
| RF13 | Sair de um grupo                     | O sistema deve permitir que o usuário saia de um grupo.                                                                                                                                 | Should Have  |
| RF14 | Editar configurações do grupo (Admin)| O sistema deve permitir que o administrador edite configurações do grupo, incluindo nome, descrição e regras de pontuação.                                                              | Should Have  |

---

## 3. Pontuação e Social

| ID   | Nome do Requisito                   | Descrição                                                                                                                                                                                                                             | Prioridade  |
|------|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF15 | Contabilizar pontuação das atividades | O sistema deve contabilizar a pontuação com base em critérios como número de atividades, duração, distância, passos, calorias e dias ativos. A pontuação será personalizável pelo administrador do grupo.                             | Must Have    |
| RF16 | Exibir ranking da competição        | O sistema deve exibir o ranking atualizado da competição.                                                                                                                                                                              | Must Have    |
| RF17 | Realizar posts no grupo             | O sistema deve permitir que o usuário faça posts, que podem conter fotos e vídeos.                                                                                                                                                      | Must Have    |
| RF18 | Comentar em posts                   | O sistema deve permitir que o usuário comente nos posts.                                                                                                                                                                               | Should Have  |

---

## 4. Gestão de Perfil de Usuário

| ID   | Nome do Requisito                  | Descrição                                                                                                                                                                                        | Prioridade  |
|------|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF19 | Editar perfil de usuário           | O sistema deve permitir que o usuário edite suas informações de perfil, incluindo nome de exibição e foto de perfil.                                                                             | Must Have    |
| RF20 | Visualizar perfil de outro usuário | O sistema deve permitir que um usuário visualize o perfil de outros membros dentro de um mesmo grupo, exibindo nome, foto e resumo de atividades recentes.                                       | Should Have  |
| RF21 | Visualizar histórico pessoal de atividades | O sistema deve permitir que o usuário visualize seu próprio histórico de atividades e pontuações acumuladas ao longo do tempo.                                                             | Must Have    |

---

## 5. Registro e Sincronização de Atividades

| ID   | Nome do Requisito                         | Descrição                                                                                                                                                                               | Prioridade  |
|------|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF22 | Registrar atividade manualmente           | O sistema deve permitir que o usuário registre uma atividade manualmente, informando dados necessários para pontuação (ex: tipo de atividade, duração, distância).                        | Must Have    |
| RF23 | Sincronizar atividades com plataformas de saúde | O sistema deve oferecer opção de sincronizar dados automaticamente com plataformas de saúde como Google Fit e Apple Saúde, para registrar treinos de forma automática.              | Could Have   |

---

## 6. Funcionalidades Sociais e de Engajamento

| ID   | Nome do Requisito            | Descrição                                                                                                                                                                                                                   | Prioridade  |
|------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF24 | Enviar notificações          | O sistema deve enviar notificações push sobre eventos como: novo comentário em post, ultrapassagem no ranking ou nova atividade registrada por membros do grupo.                                                            | Should Have  |
| RF25 | Reagir a posts e atividades  | O sistema deve permitir que os usuários reajam a posts e atividades (ex: curtir, parabenizar), de forma semelhante a outras redes sociais.                                            | Should Have  |

---

## 7. Gestão Avançada de Grupos 

| ID   | Nome do Requisito               | Descrição                                                                                                                                                                              | Prioridade  |
|------|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| RF26 | Aprovar solicitações de entrada | O sistema deve permitir que o administrador aprove ou rejeite solicitações de novos membros que desejam entrar através de um código de convite.                                        | Should Have  |
| RF27 | Promover membro a administrador | O sistema deve permitir que o administrador promova outro membro à função de administrador, compartilhando privilégios de gestão.                                                      | Could Have   |
