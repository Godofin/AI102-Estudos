# Cheat Sheet AI102 - Fala

## Azure Speech Service (Modelos para ambiente ruidosos)

- Quando usar cada modelo?
  - Ambiente Silencioso -> Padrão
  - Ambiente barulhento -> Conversão de fala em texto Personalizado
  - Precisão média com baixo custo -> Enhanced
- Palavras chave:
  - Ambiente barulhento -> Conversão de fala em texto Personalizado
  - Vocabulário técnico ou sotaques -> Conversão de fala em texto Personalizado
- Armadilhas:
  - Base ou standard -> Só cenários ideais
  - Enhanced -> Não é melhor para ruídos extremos

## Tipos de erros

- Erros de substituição
  - Resolve com nome personalizado de produtos e pessoas
- Erros de exclusão
  - Resolve com falantes em sobreposição
- Erro de inserção
  - As pessoas falam em segundo plano

## Identificação de locutores

- Identificação de locutor
  - Ajuda a indentificar um locutor desconhecido em um grupo de locutores registrado
- Verificação dependente do texto
  - locutores precisam escolher a mesma frase secreta para uso durante as fases de registro e verificação
- Verificação independente do texto
  - Os locutores podem falar frases casuais durante as fases de registro e verificação