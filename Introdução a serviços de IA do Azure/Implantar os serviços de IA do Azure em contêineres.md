# Implantar os serviços de IA do Azure em contêineres

## Introdução

- Os conteineres, possibilitam hospedar serviços de IA do Azure localmente ou no Azure.
- Por exemplo: Se o app usa dados confidenciais em SQL Server local, é possível implantar os serviços de IA do Azure em conteineres na mesma rede. Agora os dados podem permanecer em sua rede local, sem que sejam transmitidos para nuvem.
- A implantação de forma local, também diminuirá latência entre serviço de dados e os locais.

## Entender Contêineres

- O que é contêiner?
  - O contêiner consiste em um aplicativo ou serviço nos componentes de runtime necessários para executa-lo ao mesmo tempo que abstrai do sistema operacional subjacente e o hardware. Na prática a abstração resulta em dois benefícios significativos:
    - Os contêiners são portáveis entre hosts, que podem executar em sistemas operacionais diferentes ou usar hardware diferete; Facilita mover um app e suas dependências;
    - Um único host de contêiner pode dar suporte a vários contêineres isolados, cada um com sua própria configuração de runtime específica; Facilitando a consolidação de vários apps com diferentes requisitos de configuração
  - Um contêiner é encapsulado em uma *imagem de contêiner* que define o software e a configuração que ele deve dar suporte.

- Implantação de um Contêiner
  - Para usar um contêiner, normalmente é necessário extrair a imagem de contêiner de um registro e implanta em um host de contêiner. O host de contêiner pode estar na nuvem, em uma rede privada, ou computador local, por exemplo:
    - Um servidor docker
    - Uma ACI(Istância de contêiner do Azure)
    - Um cluster do AKS (Serviço de kubernets do azure)
  
## Usar contêineres dos serviços de IA do Azure

-  Para implantar um serviço de contêiner de serviços de IA do Azure, as três atividades a seguir devem ocorrer:
   -  A imagem de contêiner para API dos serviços de IA do Azure específica que você deseja usar é baixada e implantada em um host de contêiner, como Docker, Aci ou AKS;
   -  Os apps de cliente enviam dados para o ponto de extremidade fornecido pelo serviço e recuperam os resultados da mesma forma que fariam e um recurso em nuvem;
   -  Periodicamente as métricas de serviço de contêiner são enviadas para um recurso dos serviços de IA do Azure no Azure para calcular a cobrança do serviço;
-  