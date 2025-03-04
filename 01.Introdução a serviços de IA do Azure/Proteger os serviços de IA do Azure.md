# Proteger os serviços de IA do Azure

## Introdução

- O serviços de IA fornecem várias camadas de segurança que devem ser consideradas ao implementar uma solução;

## Considerar Autenticação

- Por padrão, o acesso aos recursos de serviços de IA é restrito usando chaves de assinatura;

### Regenerar Chaves

- É importante regenerar as chaves regularmente para proteger contra o risco de que elas sejam compartilhadas ou acessadas por indivíduos não autorizados. Essa regeneração pode ocorrer dentro do portal da Azure ou com comando CLI ```az cognitiveservices account keys regenerate```
- Cada serviço é fornecido com 2 chaves, permitindo a geração de novas chaves sem a interrupção do serviço, como:
  1. Se tiver usando as duas chaves em produção, é necessário alterar o código para utilizar somente uma chave
  2. Regenerar a chave 2
  3. Alterne todos os apps para a chave 2
  4. Regenerar a chave 1
  5. Atualizar novamente o código para a chave 1

Para regenerar basta:
  
  1. Portal do Azure -> Painel Chaves e Ponto de Extremidade
  2. Selecionar cada chave para regenerar

## Proteger chaves com Azure Key Vault

- O Azure Key Vault é um serviço do Azure no qual você pode armazenar segredos com segurança (como senhas e chaves).
- O acesso ao cofre de chaves é concedido a *entidades de segurança* as quais pode considerar identidades de usuário autenticados ao Microsoft Entra ID. 

## Autenticação Baseada em Token

- Ao usar interface REST, alguns serviços de IA do azure dão suporte a autenticação baseada em token. Nesses casos, a chave de assinatura é apresentada a uma solicitação inicial para obter o token tem um tempo de expiração de 10 minutos. As novas solicitações devem apresentar o token antigo para validar que o chamador foi autenticado.

## Autenticação Microsfot Entra ID

- Os serviços de IA do Azure dão suporte à autenticação do Microsoft Entra ID, permitindo que você conceda acesso a entidades de serviço específicas ou identidades gerenciadas para aplicativos e serviços em execução no Azure.

- Há diferentes forma de se autenticar utilizando o MS Entra ID, como:
  - Autenticação por meio de entidade de serviço: O processo geral de autenticação em serviços de IA do Azure por meio de entidades de serviço é o seguinte:
    - Cria um subdomínio personalizado
    - Atribuir uma função a uma entidade de serviço
  - Autenticar usando identidades gerenciadas: disponíveis em 2 tipos
    - Identidade gerenciada atribuída ao sistema: criada e vinculada a um recurso específico, como uma máquina virtual. Quando o recurso é excluído, a identidade também é excluída.
    - Identidade gerenciada atribuída pelo usuário: é criada para ser utilizada por vários recursos de uma vez ao invés de ser vincualda a um. Ela existe independentemente de qualquer recurso único;

## Implementar segurança de rede

- A segurança de rede é uma medida importante para garantir que usuários não autorizados não acessem os serviços que você está protegendo.

- Por padrão, os serviços de IA do Azure podem ser acessados de todas as redes. Alguns recursos individuais dos serviços de IA do Azure (como o serviço de Detecção Facial de IA do Azure, Visão de IA do Azure e outros) podem ser configurados para restringir o acesso a endereços de rede específicos - endereços de Internet públicos ou endereços em redes virtuais.

- Com as restrições de rede habilitadas, um cliente tentando se conectar de um endereço IP que não é permitido receberá um erro de Acesso Negado