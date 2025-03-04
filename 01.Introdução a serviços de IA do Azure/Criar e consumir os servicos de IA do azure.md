# Criar e Consumir os Serviços de IA

## Introdução

Os serviços de IA do Azure podem ser pensados como um conjunto de serviços individuais que funcionam como componentes básicos para a criação de soluções inteligentes. Alguns exemplos de serviços de IA do Azure incluem:

- **Visão de IA do Azure**: Análise de conteúdo em imagens.
- **Linguagem de IA do Azure**: Criação de aplicativos com recursos de compreensão de linguagem natural.
- **Fala de IA do Azure**: Conversão de fala em texto, texto em fala, tradução e reconhecimento de locutor.
- **IA do Azure para Informação de Documentos**: OCR (Reconhecimento Óptico de Caracteres) para extrair significado semântico de formulários, faturas, recibos e outros documentos.
- **Pesquisa de IA do Azure**: Extrai insights de dados e documentos usando IA.
- **OpenAI do Azure**: Fornece acesso a modelos avançados como o GPT-4.

---

## Provisionar um Recurso dos Serviços de IA do Azure

Para usar qualquer serviço de IA do Azure, é necessário criar **recursos** apropriados em uma **assinatura do Azure**. Isso permite:

- Definir um **ponto de extremidade** para consumir o serviço.
- Fornecer **chaves de acesso autenticado**.
- Gerenciar a **cobrança** pelo uso do aplicativo.

### Opções para Recursos do Azure

Para muitos serviços de IA do Azure, você pode escolher entre as seguintes opções de provisionamento:

1. **Recursos de Múltiplos Serviços**:
   - Um único recurso que suporta vários serviços de IA (por exemplo, Linguagem de IA, Visão de IA, Fala de IA, etc.).
   - Vantagens:
     - Gerenciamento de um único conjunto de credenciais de acesso.
     - Ponto de extremidade único.
     - Cobrança consolidada.

2. **Recurso de Serviço Único**:
   - Cada serviço de IA é provisionado individualmente.
   - Vantagens:
     - Pontos de extremidade separados para cada serviço.
     - Gerenciamento independente de credenciais e cobrança.
     - Geralmente oferecem camadas gratuitas (com restrições de uso), permitindo experimentação.

3. **Recursos de Treinamento e Previsão**:
   - Alguns serviços oferecem recursos separados para **treinamento** e **previsão** de modelos.
   - Vantagens:
     - Cobrança separada para treinamento e consumo.
     - Uso de recursos dedicados para treinamento e inferência.

---

## Identificar Pontos de Extremidade e Chaves

Ao provisionar um recurso de serviços de IA, você define:

1. **URI do Ponto de Extremidade**:
   - Endereço HTTP onde a interface REST do serviço pode ser acessada.
   - Usado pela maioria dos SDKs para iniciar conexões.

2. **Chave de Assinatura**:
   - Chave de acesso restrita para autenticação.
   - Dois tipos de chaves são criadas no provisionamento, e qualquer uma pode ser usada.

3. **Localização do Recurso**:
   - Determina o data center do Azure onde o recurso está hospedado.
   - Alguns SDKs exigem a localização explicitamente.

---

## Usar a API REST

Os serviços de IA do Azure fornecem **APIs REST** que permitem que aplicativos clientes consumam funcionalidades de IA. Características principais:

- **Formato de Dados**: JSON.
- **Métodos HTTP**: POST, PUT, GET, etc.
- **Respostas**: Retornam resultados em JSON.
- **Flexibilidade**: Qualquer linguagem ou ferramenta que suporte HTTP e JSON pode ser usada (exemplos: C#, Python, JavaScript, Postman, cURL).

---

### Exemplo de Uso

1. **Envio de Solicitação**:
   - Um aplicativo envia uma solicitação HTTP (por exemplo, uma imagem para análise) para o ponto de extremidade do serviço.

2. **Resposta do Serviço**:
   - O serviço processa a solicitação e retorna os resultados em formato JSON.

3. **Integração**:
   - Ferramentas como Postman ou bibliotecas em Python podem ser usadas para testar e integrar os serviços.