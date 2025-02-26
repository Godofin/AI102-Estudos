# Monitorar os Serviços de IA do Azure

## Introdução

- Como qualquer serviço de software, deve-se monitorar os serviços de IA do azure, para acompanhar custos, identificar tendências de utilização e detectar possíveis problemas;

## Monitorar o custo

- Um dos principais benefícios de usar serviços de IA de nuvem é que pode-se obter eficiência de custo pagando pelos serviços apenas à medida que os utiliza; Alguns recursos de IA da Azure, oferecem nível gratuito com restrições de uso, e um ou mais níveis cobrados que geram encargos com base nas transações; A taxa de cobrança depende do tipo de recurso

- **Planejar custos para serviço de IA**:
  - É possível planejar os custos utilizando a calculadora de custos da Azure
  - Para usar a calculadora, visando os custos de IA, basta criar uma nova estimativa e selecionar **Serviços de IA do Azure** na categoria *IA + Machine Learning*
  - Em seguida, é necessário selecionar, a API do Serviço específico de IA que será utilizado, a região, tipo de preço de instância e preencher as métricas e opção de suporte. 

- **Exibir custos para serviços de IA**:
  - Em comum com outros recursos do Azure, você pode exibir detalhes de custos acumulados para recursos de serviços de IA no porta do Azure
  - Para exibir os custos, é necessário:
    - Entrar no porta do Azure e selecionar a assinatura
    - Com isso, pode ser exibido os custos gerais da assinatura selecionando a guia **"Análise de custo"**
    - Para exibir os custos dos serviços de IA, é necessário adicionar um filtro que restrinja os dados para refletir os recursos com um nome de serviço de IA do azure
  
## Criar Alertas

- O microsoft azure dá suporte para criação de alertas por meio de criação de *regras de alerta*; Usar alertas são importantes a fim de configurar notificações e alertas para seus recursos com base em eventos ou limites de métricas;
- **Regras de alerta**:
  - Para criar uma regra de alerta para um recurso de IA, é necessário: 
  - Selecionar o recurso no portal do azure -> e na guia alertas, adicionar uma nova regra de alerta, para definir a regra de alerta é preciso:
    - O escopo da regra de alerta: o recurso que deseja monitorar
    - Uma condição no qual o alerta é disparado: O trigger específico para o alerta é baseado em um tipo de sinal que pode ser o log de atividades ou métrica
    - Ações opcionais: como enviar um email a um adm notificando sobre o alerta ou executando o aplicativo lógico do azure para resolver o problema automaticamente
    - Detalhes da regra de alerta: como um nome para a regra de alerta e o grupo de recursos no qual ela deve ser definida

## Métricas de exibição

- O Azure monitor coleta métricas para recursos em intervalos regulares, para que seja possível rastrear indicados de utilização, integridade e desempenho de recursos; As métricas coletadas dependem dos recursos da azure. No caso de IA, o Azure monitor coleta dados de solicitação de pontos de extremidade, dados enviados e retornados, erros e outras medições úteis

- **Exibir métricas no portal**:
  - Você pode exibir métricas para recurso individual no portal do Azure selecionando o recurso e exibindo sua página de *Métricas*. Nessa página é possível adicionar métricas específicas de recursos a gráficos, por padrão um gráfico vazio é criado e pode ser adicionado mais gráficos conforme o necessário;
  - É possível adicionar diversas métricas a um gráfico e escolher agregações e tipos de gráficos apropriados; É possível também exportar o gráfico para o excel ou copiar o link para duplica-lo na página de métricas

- **Adicionar métricas a um painel**:
  - É possível criar paineis no portal do Azure, que consistem em várias visualizações de diferentes recursos no ambiente do Azure
  - Para criar o painel, selecione painel no menu do portal do azure, lá é possível adicionar até 100 painéis nomeados para encapsular exibições em aspectos específicos dos serviços da Azure;

## Gerenciar logs de diagnóstico

- O log de diagnóstico permite que você capture dados operacionais avançados para um recurso de serviços de IA do Azure, que pode ser usado para analisar o uso do serviço e solucionar problemas

- **Criar recursos para o armazenamento de log de diagnóstico**
  - Para capturar o log, para recursos de IA do azure, é necessário de um destino para os dados de log, em determinados casos é pode-se utilizar hubs de eventos do Azure com destino de dados de log; Os hubs de eventos permitem que você encaminhe dados para a solução de telemetria personalizada se conecte diretamente a solução de terceiros, a maioria dos casos um ou ambos tipos de recurso em sua assinatura azure:
    - Azure Log Analytics: serviço que permite consultar e visualizar dados de log no portal do Azure
    - Armazenamento do Azure: armazenamento de dados baseado em nuvem que é usado para armazenar arquivos de log

- **Defina as configurações de diagnóstico**
  - Com os destinos dos logs estabelecidos, é necessário definir as configurações de diagnóstico para o recurso. Tem que definir na página **"Configurações de diagnóstico"** do painel para o seu recursos de serviços de IA, deve especificar:
    - Um nome para as configurações de diagnóstico
    - As categorias de dados de eventos de log que você deseja capturar
    - Detalhes de destinos nos quais você deseja armezanar os dados de log

- **Exibir dados de log no Azure Log Analytics**
  - Pode levar uma hora ou mais antes que os dados de diagnóstico comecem a fluir para os destinos, mas quando os dados tiverem sido capturados, você poderá exibi-los em seu recurso do Azure Log Analytics executando consultas, conforme mostrado neste exemplo.

