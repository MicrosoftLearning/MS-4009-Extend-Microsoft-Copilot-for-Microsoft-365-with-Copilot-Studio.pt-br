# Exercício: criar um plug-in de prompt

Neste exercício, você aprenderá a:

- Como escrever um bom prompt
- Criar a ação de prompt no Copilot Studio
- Testar o prompt no construtor de prompts
- Usar o plug-in de prompt no Microsoft 365 Copilot

## Como escrever um bom prompt

Anteriormente neste módulo, você já aprendeu alguns conceitos básicos de engenharia de prompt. Um ótimo recurso para saber mais sobre engenharia rápida é ler o guia de engenharia de prompt da equipe do AI Builder. Você encontra o guia de engenharia de prompt [aqui](https://aka.ms/learn-ai-builder-prompting-guide).

## Elementos de um bom prompt

O guia de engenharia de prompt da equipe do AI Builder tem um ótimo conjunto de elementos que devem fazer parte do seu prompt.

Como você pode ver, ele possui os seguintes elementos:

- **Tarefa**: uma **instrução** que informa ao modelo GPT (transformador pré-treinado generativo) a tarefa a ser executada
- **Contexto**: descreve os **dados** com base nos quais age, além de quaisquer **variáveis** de entrada
- **Expectativas**: transmita ao GPT **metas** e **expectativas** sobre a resposta
- **Saída**: ajude o GPT a formatar a **saída** da maneira que você quer

![Uma captura de tela da página de ingredientes de prompt do guia de engenharia de prompt do AI Builder. As tarefas, o contexto, as expectativas e o resultado são destacados como ingredientes de prompt.](../Media/4-prompt-engineering-guide.png)

## Tarefa 1: criar um prompt

Nesta tarefa, você criará um prompt que ajuda a criar um plano de desenvolvimento profissional com base em marcos de carreira.

> [!IMPORTANT]
> Ao criar um prompt, você não precisa começar do zero. Embora seja muito útil saber como escrever um bom prompt, pode ser útil começar com algo que resolva uma boa parte.
> Já há exemplos de prompt disponíveis na [Galeria de Soluções de Exemplo de Adoção da Microsoft](https://aka.ms/power-prompts). Neste exercício, usaremos o [exemplo de Prompt do Plano de Desenvolvimento Profissional](https://adoption.microsoft.com/sample-solution-gallery/sample/pnp-powerplatform-prompts-professional-development/).

Vamos adicionar todos os ingredientes do prompt:

- **Tarefa** – Elaborar um plano de desenvolvimento profissional.
- **Contexto** – Para alguém que pretende alcançar os seguintes [marcos] de carreira.
- **Expectativas** – O plano deve incluir metas e objetivos, recursos e ferramentas e um cronograma para as atividades.
- **Saída** – Formate o plano para ser conciso e acionável e apresente as informações de maneira clara e fácil de seguir, adequada para um funcionário de nível júnior.

Tudo isso resultaria no seguinte prompt:

*Crie um plano de desenvolvimento profissional para alguém com o objetivo de alcançar os seguintes [marcos] de carreira. O plano deve incluir metas e objetivos, recursos e ferramentas e um cronograma para as atividades. Formate o plano para ser conciso e acionável e apresente as informações de maneira clara e fácil de seguir, adequada para um funcionário de nível júnior.*

## Tarefa 2: criar uma ação de prompt no Copilot Studio

Agora que você terminou de escrever o prompt, é hora de inseri-lo no Copilot Studio.

1. No navegador da Web, navegue até o [Copilot Studio](https://copilotstudio.microsoft.com) e entre com sua conta corporativa ou de estudante, se solicitado.  Selecione **ignorar** para ignorar as mensagens de boas-vindas.

    **Observação:** na primeira vez que você abrir o Copilot Studio, poderá aparecer uma interface de bate-papo para criar seu primeiro copiloto. Se isso acontecer, clique no menu **...** no canto superior direito (ao lado do botão **Criar**), selecione **Cancelar criação do copiloto** e depois em **sair** para sair da interface de bate-papo e exibir a home page do Copilot Studio.
1. Selecione **Biblioteca** na navegação à esquerda. Aqui, você pode exibir uma lista de ações e conectores existentes e criar um novo.
1. Selecione **Adicionar um item** na parte superior.  Um menu lista duas opções para estender o Copilot para Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="A janela lista duas opções para estender o Copilot: criar um copiloto ou criar uma ação.":::
1. Selecione **Nova ação**.
1. Na tela *Nova ação*, selecione **Prompt**. Isso abrirá o construtor de prompts do AI Builder.
1. Na página **Detalhes da ação**, insira "Plano de Desenvolvimento Profissional" como o **nome da ação**.
1. Insira a seguinte **descrição**: "Cria um plano de desenvolvimento profissional acionável com base nos marcos de carreira desejados."
1. Selecione **Avançar**.
1. Na seção **prompt** da página **Adicionar uma ação de prompt**, digite "Criar um plano de desenvolvimento profissional para alguém com o objetivo de alcançar os seguintes [marcos] de carreira. O plano deve incluir metas e objetivos, recursos e ferramentas e um cronograma para as atividades. Formate o plano para ser conciso e acionável e apresente as informações de maneira clara e fácil de seguir, adequada para um funcionário de nível júnior." como o **prompt**.

    > [!NOTE]
    > Observe que há uma barra de informações na parte superior que indica que o prompt deve ter pelo menos um valor dinâmico

1. Em **Configurações do prompt** na barra lateral direita, abra a seção **Entrada**.
1. Clique no botão **Adicionar entrada** para adicionar uma entrada.
1. Insira `milestones` como o nome da entrada.
1. Adicione o seguinte texto como os dados de exemplo:

      ```text
      * Become medior in 3 years
      * Have 3 top reviews in a row
      * Become a manager in 10 years
      ```

1. Selecione **[marcos]** na seção de prompt com o cursor.
1. Selecione **Inserir**.
1. Selecione **marcos**.

      Isso fará **[marcos]** virar um valor dinâmico.

1. Em seguida, podemos testar o prompt.

## Tarefa 3: testar o prompt no construtor de prompts

1. Selecione **Testar prompt** abaixo da seção de prompt. O prompt será testado com os dados de exemplo que você adicionou anteriormente.

    > [!NOTE]
    > O prompt será enviado para o modelo de IA e mostrará a resposta na seção de resposta de IA. Isso permite que você veja como o LLM responde e se você está contente com os resultados.

1. Quando gostar da resposta de IA, clique em **Salvar prompt personalizado** para salvar o prompt.

    Na próxima janela - você pode revisar a descrição do plug-in e a descrição das entradas.

1. Na página **Selecionar parâmetros da ação**, altere a descrição de entrada dos **marcos** para:

      ```text
      The career milestones that the user wants to achieve
      ```

1. Selecione **Avançar**.

1. Clique em **Publicar** para publicar a ação no Microsoft 365 Copilot.  Isso pode levar alguns minutos.

## Tarefa 4: usar o plug-in de prompt no Microsoft 365 Copilot

Agora que você criou sua ação de prompt e a testou, passe para a próxima tarefa para acessá-la no Microsoft 365 Copilot.  Pode levar cinco minutos ou mais para que o plug-in apareça no Microsoft 365 Copilot.

1. Abra o [Microsoft Teams](https://teams.microsoft.com).
1. Na barra de navegação à esquerda, clique no botão **Copilot**.
1. Clique no ícone **Gerenciar resposta do Copilot** na parte inferior da tela (ao lado de onde você pode enviar mensagens para o Copilot).
1. Procure **Copilot Studio** no menu suspenso que apareceu e confirme se ele está ativado para ser ativado.  
1. Clique no **ícone do cursor** para expandir a lista de ações em Copilot Studio.

    > [!NOTE]
    > Pode ser que o Copilot Studio não esteja visível. Pode haver duas razões para isso: ou seu administrador não implantou o aplicativo integrado do Copilot Studio ou o plug-in ainda não foi indexado. Isso pode significar que você deve esperar um pouco mais.

2. Procure a ação com o nome **Plano de Desenvolvimento Profissional** na lista de ações na seção Copilot Studio e selecione a alternância ao lado dela para ativá-la.

    > [!NOTE]
    > Se você não vir Plano de Desenvolvimento Profissional na lista de plug-ins do Copilot Studio, pode demorar um pouco mais para aparecer. Pode demorar um pouco mais para aparecer no Microsoft 365 Copilot.

3. Depois de ativar a ação Plano de Desenvolvimento Profissional, agora você pode usá-la no Copilot. **Faça um teste** enviando a seguinte mensagem para o Copilot no Teams: "Quero gerar um Plano de Desenvolvimento Profissional para atingir os seguintes marcos de carreira: 1 – melhorar no meu trabalho como profissional de marketing e 2 – ter uma chance melhor de promoção à função de profissional de marketing sênior."

**Dica:** para ativar o modo de desenvolvedor no Copilot, insira `-developer on` no bate-papo.  Isso permite que você observe quando o Copilot usou um plug-in para responder no bate-papo.
