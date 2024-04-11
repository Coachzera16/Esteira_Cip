# Sistema de Portabilidade de Crédito Consignado - Documentação

## Objetivo

O Sistema de Portabilidade de Crédito Consignado tem como objetivo simplificar e automatizar o processo de solicitação de portabilidade de crédito consignado de outros bancos para o Itaú Unibanco. Esta documentação fornece uma visão geral do sistema, incluindo sua arquitetura, funcionalidades e instruções de uso.

## Tecnologias Utilizadas

- **Frontend em Angular:** Interface do usuário desenvolvida em Angular para facilitar a interação dos usuários.
- **Backend AWS Lambda:** Funções Lambda na AWS para processar as solicitações de portabilidade.
- **AWS CIP (Centralizadora de Serviços da CIP):** Serviço externo responsável pela validação e processamento da portabilidade de crédito consignado.

## Funcionalidades

O Sistema de Portabilidade de Crédito Consignado oferece as seguintes funcionalidades:

1. **Solicitação de Portabilidade:** Os usuários podem solicitar a portabilidade de crédito consignado fornecendo as informações necessárias, como dados pessoais e detalhes do contrato atual.
2. **Processamento da Solicitação:** O sistema processa a solicitação, incluindo validação dos dados, comunicação com a CIP e processamento da resposta.
3. **Feedback ao Usuário:** Os usuários recebem feedback sobre o status da solicitação, incluindo confirmação de envio, aprovação da portabilidade ou retenção pelo banco detentor do contrato.

## Configuração e Implantação

Para configurar e implantar o Sistema de Portabilidade de Crédito Consignado, siga estas etapas:

### Frontend Angular:

1. Clone este repositório e navegue até o diretório do frontend.
2. Instale as dependências utilizando o comando `npm install`.
3. Execute o aplicativo localmente usando o comando `ng serve`.
4. Para implantação em produção, compile o aplicativo usando o comando `ng build --prod` e hospede os arquivos estáticos em um serviço de hospedagem, como AWS S3 ou AWS Amplify.

### Backend AWS Lambda:

1. As funções Lambda estão localizadas no diretório `lambda_functions`.
2. Cada função deve ser implantada individualmente na AWS Lambda usando o console da AWS ou ferramentas de automação como AWS SAM (Serverless Application Model).

## Contribuição

Se você deseja contribuir para este projeto, siga estas etapas:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature (`git checkout -b feature/MinhaFeature`).
3. Faça commit das suas alterações (`git commit -am 'Adicionando uma nova feature'`).
4. Faça push para a branch (`git push origin feature/MinhaFeature`).
5. Crie um novo Pull Request.
