# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS
 DATA : [22/07/2025]
 EMPRESA:[ABSTERGO INDUSTRIES]
 RESPONSÁVEL:[EDUARDO MIGUEL BOTELHO]

 ## INTRODUÇÃO
  Este relatório apresenta o processo de implementação de ferramentas na empresa [Abstergo Industries], realizado por [Eduardo Miguel Botelho].
  O objetivo foi elencar 3 serviços AWS, com a finalidade de realizar uma
  diminuição de custos imediatos.

  ## DESCRIÇÃO DO PROJETO
  O Projeto de implementação de ferramentas foi realizado em 3 etapas, cada uma com seus objetivos específicos. A seguir, serão descritas as etapas do projeto:
  
  ETAPA 1:
  -[AWS Direct Connect e Amazon RDS]
  -[Conectividade Segura On-Premises a partir da infraestrutura local, utilize o AWS Direct Connect para uma conexão de rede dedicada. Amazon RDS:Oferece alta disponibilidade e gerenciamento simplificado.

]
  -[ AWS Direct Connect :
  A empresa contrata um parceiro da AWS para instalar uma conexão de fibra óptica dedicada que vai do seu data center local até um Ponto de Presença (PoP) do Direct Connect. Este é um local físico onde a AWS tem sua infraestrutura de rede.
  Conexão Privada: Essa fibra estabelece um link direto e privado entre a rede da empresa e a rede global da AWS, contornando completamente a internet pública.
Interface Virtual (VIF): Sobre essa conexão física, eles criam uma Interface Virtual Privada (Private VIF) para se conectar diretamente à sua Amazon VPC (Virtual Private Cloud), onde estão seus recursos de computação e análise. 
    Amazon RDS:
    Implantações Multi-AZ: Configure o RDS com implantações Multi-AZ (Múltiplas Zonas de Disponibilidade). O RDS manterá uma réplica síncrona em outra Zona de Disponibilidade e realizará o failover automaticamente em caso de falha, garantindo a continuidade dos negócios.]

ETAPA 2:
  -[Amazon VPC]
  -[Proporcionar isolamento lógico de cada um dos ambientes como: desenvolvimento, testes e produção.]
  -[Caso de Uso: Para hospedar um Sistema de Gerenciamento de Dados de Ensaios Clínicos (CTMS - Clinical Trial Management System), a empresa cria uma VPC. O banco de dados do CTMS, contendo informações sensíveis de pacientes, é colocado em uma sub-rede privada, sem acesso direto à internet. Apenas o servidor de aplicação do CTMS, localizado em outra sub-rede privada, pode se comunicar com o banco de dados. O acesso dos usuários ao sistema é feito através de um Application Load Balancer seguro, localizado na sub-rede pública, garantindo o isolamento completo dos dados críticos.
  Sub-redes Públicas e Privadas: Recursos que não precisam de acesso direto à internet, como bancos de dados e servidores de aplicação, devem ser colocados em sub-redes privadas. Apenas recursos que necessitam de exposição, como Application Load Balancers, devem ficar em sub-redes públicas.]

ETAPA 3:
  -[AWS Compute Optimizer e AWS Cost Explorer]
  -[Utilize o  e o  para analisar e dimensionar corretamente as instâncias EC2 e os bancos de dados RDS, evitando o superprovisionamento.
Spot e Savings Plans: Para cargas de trabalho não críticas ou ambientes de desenvolvimento e teste, o uso de Instâncias Spot pode gerar uma economia de até 90%. Para cargas de trabalho previsíveis, os Savings Plans oferecem um desconto significativo em troca de um compromisso de uso.
]
  -[A equipe de finanças utiliza o AWS Cost Explorer para visualizar os gastos mensais e percebe que a maior parte do custo vem de instâncias EC2. Usando o AWS Compute Optimizer, eles analisam as métricas de uso (CPU, memória, rede) das instâncias que rodam o software de simulação molecular.]

#CONCLUSÃO
A implementação de ferramentas na empresa [ABSTERGO INDUSTRIES] tem como esperado [Redução de custos utilizando as ferramentas AWS] , o que aumentará a eficiência e a produtividade da empresa. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam melhorar ainda mais os processos da empresa.

#Anexos
[(https://aws.amazon.com/pt/products/compute/?trk=2ee11bb2-bc40-4546-9852-2c4ad8e8f646&sc_channel=ps&ef_id=CjwKCAjw7fzDBhA7EiwAOqJkhzleoqiRTtYihdyyibVIZxkCSdcB19HM4a48xcidjVDVpXfE1Q5hYRoChtEQAvD_BwE:G:s&s_kwcid=AL!4422!3!696214219377!e!!g!!aws!15278604629!130587771740&gad_campaignid=15278604629&gbraid=0AAAAADjHtp_lI36qSqLFKEQzyJpueFeZV&gclid=CjwKCAjw7fzDBhA7EiwAOqJkhzleoqiRTtYihdyyibVIZxkCSdcB19HM4a48xcidjVDVpXfE1Q5hYRoChtEQAvD_BwE)]
Assinatura do Responsável pelo Projeto:
[Eduardo Miguel Botelho]







