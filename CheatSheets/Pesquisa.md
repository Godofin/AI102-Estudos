# Cheat Sheet AI102 - Pesquisa de IA

## Tipos de Dados para Projeções no Azure AI Search

- Tipos:
  - Arquivos: Binários, PDF, imagens, Json complexo
  - Objetos: Json Hierarquico
  - Tabelas: Dados tabulares
- Palavras chaves:
  - PDF, imagem, documento binário e normalização de arquivos -> Arquivos
  - Saída JSON, dados aninhados, estrutura complexa -> Objetos
  - Dados tabulares, metadados, csv, excel, armazenamento estruturado -> Tabelas

## Tipos de Odata para pesquisa

- Azure Machine Learning: AmlSkill
- Pesquisa web ou de uma API Web: WebApiSkill
- Busca de termos em text: CustomEntityLookupSkill
- Extrair conteúdo de arquivo/Documento: DocumentExtractionSkill
- Busca de entidades em um documento: EntityRecognitionSkill
- Extração de palavras chave em um documento: KeyPhraseExtractionSkill
- Dividi conteúdos do documento: SplitSkill
- Gerar links para entidades: EntityLinkingSkill

## Formatos Suportados pelo Modelo de Leitura Pré-treinado do Azure AI Document Intelligence

- PDF
- XLSX
- DOCX