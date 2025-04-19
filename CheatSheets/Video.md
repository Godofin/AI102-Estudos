# Cheat Sheet AI102 - Video Indexer

## Treinamento de Modelo de Linguagem Personalizado no Azure Video Indexer

- Palavras Chave:
  - Vários exemplos de frase -> Diversidade de dados
  - Uma frase por linha -> Formatação correta
  - Variações de adaptação ou múltiplas formas de dizer a mesma coisa -> Sinônimos, contextos diferentes
  - Domínio específico -> Modelos personalizados exigem dados focados
- Respostas erradas:
  - Quantidades enormes de dados
  - Caracteres especiais
  - Modelo genérico

## Extração de miniaturas em vídeos

- Palavras chaves:
  - Obter o índice do vídeo
  - Miniatura de cada quadro-chave
- Sempre que tiver quadro-chave na pergunta:
  - Necessário carregar o vídeo
  - índice contém os metadados
  - Miniaturas são obtidas uma a uma via API