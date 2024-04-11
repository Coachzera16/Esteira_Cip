    #Documentação do Sistema de Portabilidade de Crédito Consignado
#Visão Geral
Este repositório contém a documentação do sistema de portabilidade de crédito consignado desenvolvido para facilitar a solicitação de portabilidade de crédito de outros bancos para o Itaú Unibanco. O sistema foi construído utilizando Angular para o frontend e AWS Lambda para o backend.

Arquitetura

A arquitetura do sistema é composta por três principais componentes:

Frontend em Angular:

Interface do usuário acessível através de um navegador web.
Permite que os usuários solicitem portabilidade de crédito consignado fornecendo informações necessárias.
Backend AWS Lambda:

Responsável pelo processamento das solicitações de portabilidade.
Composto por várias funções Lambda que realizam etapas específicas do processo, como validação, comunicação com a CIP e processamento de respostas.
AWS CIP (Centralizadora de Serviços da CIP):

Entidade externa responsável pela validação e processamento da portabilidade de crédito consignado.
O backend AWS Lambda se comunica com a CIP enviando e recebendo arquivos XML conforme necessário.
Funcionamento
Solicitação de Portabilidade:

O usuário acessa a interface do sistema através do frontend em Angular.
Ele preenche um formulário com informações necessárias para a solicitação de portabilidade, como dados pessoais e detalhes do contrato atual.
Após enviar o formulário, o frontend envia os dados da solicitação para o backend AWS Lambda por meio de chamadas HTTP.
Processamento da Solicitação:

O backend AWS Lambda recebe a solicitação e realiza uma série de etapas, incluindo validação dos dados, comunicação com a CIP e processamento da resposta.
Cada etapa é realizada por uma função Lambda específica, garantindo uma separação clara de responsabilidades e facilitando a manutenção do sistema.
Comunicação com a CIP:

Durante o processo de portabilidade, o backend AWS Lambda se comunica com a CIP enviando e recebendo arquivos XML conforme necessário para a validação e processamento da portabilidade.
Configuração e Implantação
Frontend Angular:

Clone este repositório e navegue até o diretório do frontend.
Instale as dependências utilizando o comando npm install.
Execute o aplicativo localmente usando o comando ng serve.
Para implantação em produção, compile o aplicativo usando o comando ng build --prod e hospede os arquivos estáticos em um serviço de hospedagem, como AWS S3 ou AWS Amplify.
Backend AWS Lambda:

As funções Lambda estão localizadas no diretório lambda_functions.
Cada função deve ser implantada individualmente na AWS Lambda usando o console da AWS ou ferramentas de automação como AWS SAM (Serverless Application Model).
Contribuição
Se você deseja contribuir para este projeto, siga estas etapas:

Faça um fork do repositório.
Crie uma branch para sua feature (git checkout -b feature/MinhaFeature).
Faça commit das suas alterações (git commit -am 'Adicionando uma nova feature').
Faça push para a branch (git push origin feature/MinhaFeature).
Crie um novo Pull Request.
