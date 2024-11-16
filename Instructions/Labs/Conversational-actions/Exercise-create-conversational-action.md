# Exercício: criar uma ação de conversa

Neste exercício, você criará uma ação de conversa que fornece informações sobre um projeto organizacional fictício intitulado "Projeto ABC".

Tarefas de exercício:

- Criar uma ação de conversa no Copilot Studio
- Publicar uma ação de conversa no Microsoft Copilot
- Testar a ação de conversa no Microsoft Copilot

## Tarefa 1: (Opcional) testar a experiência padrão

Para começar, faça uma pergunta sobre o projeto ABC no Microsoft 365 Copilot.

1. Abra o **Microsoft Teams** e entre com sua conta corporativa ou de estudante.

1. Selecione **Conversar** na barra lateral.

1. Selecione **Copilot** no menu de conversa.

1. Na caixa de composição da mensagem, insira `Who should I contact for questions about Project ABC?`

1. Observe que o Microsoft 365 Copilot atualmente não tem nenhuma informação sobre o Projeto ABC.

## Tarefa 2: criar uma nova ação de conversa

Primeiro, configure o nome, a solução e o esquema para uma nova ação de conversa no Microsoft Copilot.

1. No navegador da Web, navegue até o [Copilot Studio](https://copilotstudio.microsoft.com) e entre com sua conta corporativa ou de estudante, se solicitado.  Selecione **ignorar** para ignorar as mensagens de boas-vindas.

    **Observação:** na primeira vez que você abrir o Copilot Studio, poderá aparecer uma interface de bate-papo para criar seu primeiro copiloto. Se isso acontecer, clique no menu **...** no canto superior direito (ao lado do botão **Criar**), selecione **Cancelar criação do copiloto** e depois em **sair** para sair da interface de bate-papo e exibir a home page do Copilot Studio.
1. Selecione **Biblioteca** na navegação à esquerda. Aqui, você pode exibir uma lista de ações e conectores existentes e criar um novo.
1. Selecione **Adicionar um item** na parte superior.  Um menu lista duas opções para estender o Copilot para Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="A janela lista duas opções para estender o Copilot: criar um copiloto ou criar uma ação.":::
1. Selecione **Nova ação**.

1. Selecione **Conversa** para criar uma ação de conversa.

1. No campo **nome**, insira `Project ABC` e aceite a solução e o esquema padrão.

1. Selecione **Criar** para continuar. Sua nova ação de conversa será criada. Isso pode levar alguns segundos. Quando terminar, a tela de criação abrirá para você continuar configurando a ação.

## Tarefa 3: configurar o tópico

Em seguida, configure o nome e o gatilho do tópico.

1. No painel de criação de ações da conversa, navegue até a guia **Tópicos**.

1. Selecione a caixa de texto **Nome do tópico** na parte superior do painel, que usa como padrão o nome `"Untitled"` e insira `Project ABC info` para nomear o tópico.

1. No nó **Gatilho** dentro do tópico, selecione a caixa de texto sob o texto "Descrever o que o tópico faz" e insira `Answers questions and provides information about Project ABC, including questions about objectives, points of contact, and rollout timeline.`.

## Tarefa 4: enviar uma mensagem

Em seguida, adicione um nó ao tópico para enviar uma mensagem sobre o Projeto ABC.

1. No nó Gatilho, clique no ícone **+** para adicionar um novo nó.

1. No menu exibido, selecione **Enviar uma mensagem**.  Um nó de mensagem será criado.

1. No nó de mensagem, selecione a caixa de texto e insira `Project ABC is an initiative aimed at improving the culture and engagement within the company.  Objectives of the project include improved morale, increased employee survey results, and improved culture ratings.  For more information about Project ABC, contact Devon Torres.`.

1. Clique em **Salvar** acima da tela de criação para salvar as alterações.

## Tarefa 5: publicar a ação

Em seguida, publique a ação para uso no Microsoft 365.

1. Selecione **Publicar** na parte superior da página.

1. Na página **Publicar plug-in**, selecione **Publicar**.

1. Na página **Publicar conteúdo mais recente?**, confirme se o plug-in Informações do Projeto ABC está ativado e clique em **Publicar**.  A publicação pode demorar alguns minutos.  Uma notificação será exibida na parte superior da janela quando a publicação for concluída.

## Tarefa 6: habilitar e testar a ação

Por fim, teste a ação no Microsoft 365 Copilot.

1. Abra o **Microsoft Teams**.

1. Selecione **Conversar** na barra lateral.

1. Selecione **Copilot** no menu de conversa.

1. Na área de composição da mensagem, clique no botão **Gerenciar resposta do Copilot**.

1. No submenu, pesquise **Copilot Studio** e selecione **Adicionar** para adicionar o Copilot Studio.
 
2. A ação **Informações do Projeto ABC** agora estará listada no submenu.  Confirme se **Informações do Projeto ABC** está habilitada e feche o submenu.

:::image type="content" source="../Media/projectABCInfo-action-enabled.png" alt-text="Captura de tela da ação Informações do Projeto ABC listada no submenu"Manage Copilot response" flyout in Teams.":::

3. Na caixa de composição da mensagem, insira `Who should I contact for questions about Project ABC?`

4. Observe que o Microsoft 365 Copilot retorna informações do Projeto ABC invocando a ação de conversa.

Você pode personalizar ou expandir essa ação de conversa com nós adicionais.  Por exemplo, você pode criar um novo nó **Respostas generativas** e fazer upload de um arquivo, expandindo o conhecimento disponível para a ação.

**Observação:** lembre-se do seguinte ao testar sua ação no Copilot:
- O Copilot sempre regravará suas respostas com sua própria voz. Não é possível nesta versão prévia fazer com que o conteúdo seja transmitido inalterado ao usuário final.
- A descrição da ação de conversa é essencial para a confiabilidade com que ela será invocada. A descrição mostra ao Orquestrador a qualidade da ação e quais respostas ela pode fornecer. Certifique-se de usar uma linguagem clara ao escrever a descrição e experimente alterações para obter o melhor resultado.
- Seguir essas etapas com precisão não garante que o Copilot sempre retornará os resultados esperados.  O Copilot determinará quando invocar seu plug-in e como retornar os resultados.

## (Opcional) Desafio: crie a sua versão!

Aplique o que você aprendeu para criar, publicar e testar uma nova ação de conversa para um cenário de sua escolha.  Revise as etapas deste exercício conforme necessário.