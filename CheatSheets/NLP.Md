# Cheat Sheet AI102 - NLP

## Escala BLEU

- 0 a 19: Tradução inintiligível ou muito ruim
- 20 a 39: Tradução com alguns significados compreensíveis, mas com muitos erros.
- 40 a 59: Tradução de qualidade razoável, com alguns erros, mas geralmente compreensível.
- 60 a 79: Tradução de alta qualidade, próxima à fluência humana.
- 80 a 100: Tradução quase perfeita ou indistinguível de uma tradução humana

## Perguntas de QNA/Chatbot para perguntas frequentes

- Cenários adequados:
  - Informações estáticas na base de conhecimento
  - Conversas de bot com respostas pré-definidas
  - Fornecer a mesma resposta para a mesma pergunta
- Tips:
  - Foque em "respostas estáticas"
  - Descartar "Dinâmicos" e "em tempo real"
  - Cuidado com perguntas genéricas: Exemplo: "Responder qualquer pergunta" → inviável sem contexto pré-definido.

## Importação de dados no Azure Question Answering

- Palavras chaves:
  - Texto formatado
  - Listas
  - URL's
- Armadilhas:
  - Dados não estruturados -> Errado
  - Imagens/Tabelas complexas -> Não aceito
- Fluxo de decisão:
  - O documento tem formatação ou listas? -> Sim(Compatível)
  - Contém apenas texto bruto e sem organização -> Não (Não é ideal)
  - Inclui imagens ou gráficos? Ignorado na extração