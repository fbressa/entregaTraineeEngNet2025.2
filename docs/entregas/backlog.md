# Backlog

No backlog, os itens são frequentemente chamados de *user stories* (histórias de usuário) ou requisitos, que representam funcionalidades, comportamentos ou qualidades esperadas do sistema.  
Esses itens servem como base para o planejamento e priorização das entregas, permitindo que a equipe de desenvolvimento compreenda o que deve ser construído e o motivo por trás de cada funcionalidade.  

Cada *user story* descreve, de forma simples e orientada ao usuário, uma necessidade específica geralmente seguindo o formato:  
> “Como [tipo de usuário], eu quero [funcionalidade] para [benefício esperado].”

Além das *user stories*, o backlog também inclui requisitos não funcionais, que definem as características de qualidade do sistema, como desempenho, confiabilidade, usabilidade e segurança.  
Enquanto as histórias de usuário focam em *o que* o sistema deve fazer, os requisitos não funcionais estabelecem *como* o sistema deve se comportar para garantir uma boa experiência e operação estável.

Manter ambos os tipos de requisitos no backlog garante uma visão completa do produto, equilibrando valor para o usuário e qualidade técnica.


## User Stories

| ID | User Story (Descrição) | Épico (Categoria) |
|----|-------------------------|-------------------|
| **ÉPICO 1** | **Autenticação e Gestão de Conta** |  |
| US:01 | "Como um novo usuário, eu quero poder criar uma conta usando meu e-mail e uma senha para acessar o aplicativo e participar das competições." | Autenticação e Gestão de Conta |
| US:02 | "Como um usuário, eu quero realizar login com meu e-mail e senha para acessar minha conta de forma segura." | Autenticação e Gestão de Conta |
| US:03 | "Como um novo usuário, eu quero me conectar usando minha conta Google ou Apple para um cadastro mais rápido." | Autenticação e Gestão de Conta |
| US:04 | "Como um usuário, eu quero recuperar minha senha caso a esqueça, para não perder o acesso à minha conta." | Autenticação e Gestão de Conta |
| US:05 | "Como um usuário, eu quero poder fazer logout do aplicativo para garantir a privacidade da minha conta." | Autenticação e Gestão de Conta |
| US:06 | "Como um usuário, eu quero poder apagar minha conta e meus dados permanentemente." | Autenticação e Gestão de Conta |
| **ÉPICO 2** | **Gestão de Grupos** |  |
| US:07 | "Como um usuário, eu quero criar um novo grupo de competição para desafiar meus amigos e colegas." | Gestão de Grupos |
| US:08 | "Como um usuário, eu quero entrar em um grupo existente usando um código de convite para participar de uma competição." | Gestão de Grupos |
| US:09 | "Como um administrador de grupo, eu quero gerar um código de convite único para compartilhar e trazer novos membros para o meu grupo." | Gestão de Grupos |
| US:10 | "Como um membro do grupo, eu quero visualizar a lista de todos os participantes para saber quem está na competição." | Gestão de Grupos |
| US:11 | "Como um membro, eu quero poder sair de um grupo que não desejo mais participar." | Gestão de Grupos |
| **ÉPICO 3** | **Competição e Interação Social** |  |
| US:12 | "Como um membro do grupo, eu quero que minhas atividades sejam convertidas em pontos automaticamente para competir de forma justa." | Competição e Interação Social |
| US:13 | "Como um membro do grupo, eu quero visualizar um ranking atualizado para acompanhar minha posição e a dos meus concorrentes." | Competição e Interação Social |
| US:14 | "Como um membro do grupo, eu quero poder fazer posts com fotos e vídeos para compartilhar meu progresso e interagir com os outros." | Competição e Interação Social |
| US:15 | "Como um membro do grupo, eu quero comentar nos posts de outros usuários para incentivar e interagir com eles." | Competição e Interação Social |
| **ÉPICO 4** | **Perfil e Atividades do Usuário** |  |
| US:16 | "Como um usuário, eu quero editar meu nome de exibição e foto para personalizar meu perfil." | Perfil e Atividades do Usuário |
| US:17 | "Como um usuário, eu quero visualizar meu histórico de atividades e pontuações para acompanhar minha evolução ao longo do tempo." | Perfil e Atividades do Usuário |
| US:18 | "Como um usuário, eu quero registrar uma atividade manualmente quando não for possível sincronizar automaticamente, para que ela conte na competição." | Perfil e Atividades do Usuário |
| US:19 | "Como um usuário, eu quero sincronizar minhas atividades do Google Fit ou Apple Saúde para registrar meus treinos de forma automática e prática." | Perfil e Atividades do Usuário |

---

## ⚙️ Requisitos Não Funcionais

| ID | Descrição do Requisito Não Funcional | Categoria |
|----|--------------------------------------|------------|
| RNF01 | A interface deve ser exibida corretamente em dispositivos móveis com resoluções de 5 a 12 polegadas. | Usabilidade |
| RNF02 | Um usuário iniciante deve conseguir criar ou entrar em um desafio e registrar seu primeiro treino em no máximo 5 minutos após o primeiro login. | Usabilidade |
| RNF03 | O aplicativo deve estar disponível e funcional nas versões mais recentes e nas duas versões anteriores de iOS e Android. | Usabilidade |
| RNF04 | A interface do usuário deve seguir um padrão de design consistente (cores, fontes, ícones, botões de ação). | Usabilidade |
| RNF05 | O aplicativo deve fornecer respostas visuais ou táteis imediatas às ações do usuário, confirmando o recebimento do comando. | Usabilidade |
| RNF06 | O aplicativo deve aderir às diretrizes de acessibilidade (redimensionamento de texto e leitores de tela). | Usabilidade |
| RNF07 | As mensagens de erro devem ser claras, informativas e em linguagem simples. | Usabilidade |
| RNF08 | A interface deve ser limpa e sem excesso de informações. | Usabilidade |
| RNF09 | Deve haver uma seção de ajuda ou tutorial acessível para suporte adicional. | Usabilidade |
| RNF10 | O aplicativo e seus serviços devem ter alto tempo de disponibilidade. | Confiabilidade |
| RNF11 | Manutenções que exijam interrupção devem ocorrer em horários de baixo tráfego. | Confiabilidade |
| RNF12 | O app deve lidar bem com conexões instáveis, tentando reconectar automaticamente. | Confiabilidade |
| RNF13 | Em falhas de servidor ou API, o app deve exibir dados em cache e mensagens amigáveis. | Confiabilidade |
| RNF14 | O app deve validar entradas e guiar o usuário em caso de erro de formato. | Confiabilidade |
| RNF15 | Devem existir validações no cliente e no servidor para garantir integridade dos dados. | Confiabilidade |
| RNF16 | O app deve restaurar a sessão do usuário se for interrompido. | Confiabilidade |
| RNF17 | O usuário deve poder recuperar dados após perda do dispositivo ou reinstalação. | Confiabilidade |
| RNF18 | O app deve implementar relatórios automáticos de falhas. | Confiabilidade |
| RNF19 | O app deve carregar e responder rapidamente aos comandos. | Desempenho |
| RNF20 | Ações do usuário devem ser processadas em poucos segundos. | Desempenho |
| RNF21 | O sistema deve suportar muitos usuários simultâneos sem lentidão. | Desempenho |
| RNF22 | O app deve consumir o mínimo de bateria possível. | Desempenho |
| RNF23 | O tamanho do app deve ser o menor possível e permitir limpeza de cache. | Desempenho |
| RNF24 | O número de chamadas de rede deve ser minimizado. | Desempenho |
| RNF25 | O app deve implementar cache inteligente para dados e imagens frequentes. | Desempenho |
| RNF26 | O app deve capturar e enviar relatórios automáticos de falhas. | Suportabilidade |
| RNF27 | O app deve enviar logs de eventos e erros para um serviço centralizado. | Suportabilidade |
| RNF28 | O app deve coletar métricas de desempenho (tempo de carregamento, CPU, memória). | Suportabilidade |
| RNF29 | O código deve seguir arquitetura em camadas (MVVM, MVC, MVI). | Suportabilidade |
| RNF30 | O código deve seguir convenções de estilo, ser comentado e legível. | Suportabilidade |
| RNF31 | O app deve ser configurável para diferentes ambientes (Dev, Teste, Prod). | Suportabilidade |
| RNF32 | O código e as APIs públicas devem ser documentados. | Suportabilidade |
| RNF33 | O processo de build, teste e publicação deve ser documentado. | Suportabilidade |
