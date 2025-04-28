# Resumo Azure - Certificação AZ900 - DIO

## Introdução
Este repositório contém um resumo dos conceitos aprendidos durante o estudo da certificação AZ900 da Microsoft, cobrindo aspectos básicos do Azure.

## O que é a computação em nuvem?
- É o fornecimento de serviços de computação pela internet, habilitando inovações mais rápidas, recursos flexíveis e economia de escala.
- É a virtualização de uma empresa, de modo IaaS, pagando apenas pelo uso.

## Modelos
### Privada
- A empresa cria a sua nuvem, um ambiente interno em seu data center, sem os grandes players, este modelo também se chama on-premise.
- A empresa é responsável por operrar os serviços e não gera acessos a usuários de fora da organização.
### Pública
- Entrega de serviços e recursos para diversas organizações e usuários, através de um provedor de hosting.
- Acesso via conexão de rede segura.
-  Empresas deste segmento, Microsoft (Azure), Amazon (AWS), Google (GCP), Oracle (Oracle Cloud).
### Híbrida
- A organização opta em utilizar os dois modelos anteriores, por questões como sazonalidade, se em determinado período do ano ela recebe um crescimento de acessos e seu modelo on-premise não consegue dar conta, ela utiliza de máquinas em modelo cloud para suportar aquela operação. Ao passar o período ela encerra as máquinas e volta a utilizar apenas o seu modelo de nuvem privada, pagando apenas pelo que foi utilizado.
- Este modo ajuda as organizações em momentos onde seus serviços são requisitados além das capacidades.

## Vantagens e Desvantagems

|Modelo                   |Vantagens                                                             |Desvantagens                             |
|-------------------------|----------------------------------------------------------------------|-----------------------------------------|
| **Privada (on-premise)**| Maior controle e personalização                                      | Custo alto de manutenção e espaço físico|
| **Pública (cloud)**     | Custo baixo, exacalabilidade e flexibilidade                         | Dependência da internet                 |
| **Híbrida**             | Flexibilidade de escolher o que e onde, de acordo com as necessidades| Complexidade na gestão                  |


## Benefícios da Nuvem Pública (Cloud)
### Alta disponibilidade
- Disponível sempre que necessário. No caso do Azure, é calculada uma taxa de indisponibilidade, e se ultrapassada, a Microsoft oferece créditos como compensação na próxima fatura.
### Escalabilidade
- Refere-se a capacidade de ajustar recursos para atender a demanda.
- Pago somente pelo uso ativo.
- Podendo reduzir recursos e consequentemente os seus custos.
- Escala vertical, quando necessário aumento do poder de processamento.
### Elasticidade
- Devido a sazonalidade da demanda, os recursos implantados poderiam ser expandidos de modo automático ou manual, o mesmo vale para a redução destes recursos devido a baixa demanda.
### Confiabilidade
- Refere-se a resiliência, o sistema se recupera de falhas e continua em funcionamento, devido sua escala global descentralizada.
### Previsibilidade
- Permite que avancemos com confiança, tanto no desempenho quanto no custo.
### Segurança
- São oferecidas diversas formas de segurança, porém muitas delas a implementação fica sob responsabilidade do cliente.
### Governança
- Auditoria baseada em nuvem ajuda a sinalizar qualquer recurso que esteja fora de conformidade com seus padrões corporativos e fornece estratégias para mitigar problemas.
### Gerenciabilidade
- Escalar automaticamente a implantação de recursos com base na necessidade. Podemos utilizar um modelo pré-configurado facilitando a implantação inicial.

## Criar uma máquina virtual do Azure
### Acesse o Portal Azure
- Vá para [Portal Azure](https://portal.azure.com)
- Crie sua conta gratuitamente e preencha com os dados solicitados.
- Vale lembrar que é necessário um cartão de crédito para criar sua conta, será débito um baixo valor e estornado em sequência.
### Criação da Máquina Virtual
- Acesse os recursos na lateral esquerda da tela e clique em "Máquinas Virtuais".
- Clique em "Criar" no centro da tela e depois em "Máquina virtual do Azure".
### Básico
- Grupo de Recursos: Selecione ou crie um novo.
- Nome da máquina virtual: "dio-teste-vm"
- Região: Local onde sua máquina será criada, observação o Brasil é uma região com valor elevado na criação.
- Opções de disponibilidade: "Zona de disponibilidade".
- Zona de disponibilidade: Refere-se aos locais dentro da região e quantos queremos adicionar, podemos colocar até 3 zones, isso faz com que nossos serviços não parem independente do que ocorra.
- Tipo de segurança: "Computadores virtuais de inicialização confiável".
- Imagem: Qual o SO queremos trabalhar, isso influencia o valor final.
- Tamanho: em teoria se trata das configurações da máquina.
- Conta de ADM: Deve ser criado o login e senha para acesso daquela máquina, seguindo os padrões de senha da Microsoft.
- Regras: Devido não possuirmos uma VPN para acesso é necessário liberar a porta RDP (3389) para acesso em máquinas Microsoft, não é aconselhado devido questões de segurança, mas como estamos estudando, podemos manter assim.
### Discos
- Tipo de disco de SO: o conceito aqui é igual a uma máquina física, um SSD Premium, será uma excelente opção.
### Rede
- Rede Virtual e Sub-rede: O Azure irá criar esta infraestrutira de rede para nós, porém em cenários produtivos criar a rede e depois a máquina virtual é a melhor decisão.
- Excluir o IP público e a NIC quando a VM for excluída: Deixe esta opção selecionada, pois se excluir a máquina e o IP público não for excluído, o serviços seram cobrados pois aquele IP estará orfão e gerando encargos.
### Gerenciamento
- Desligamento automático: O ideal é deixar selecionado, pois se esquecer de desligar a máquina ela também continua gerando consumo, configure o fuso-horário igual a região que a máquina será criada.
- Defina a hora de desligamento
- Selecione a opção de notificação por e-mail, assim o Azure enviará ao e-mail cadastrado em sequência um aviso sobre o desligamento da máquina.
### Monitoramento
- Podemos receber um diagnóstico de performance da máquina criada.
### Marcas (Tags)
- Etiquetas sobre os recursos que estamos criando.
### Revisar + Criar 
- O Azure calcula os custos por hora daquela máquina e gera um resumo das configurações que acabamos de fazer.
- Selecionar "Criar".

## O que é o Azure SQL Database (PaaS)?
É um serviço de banco de dados relacional totalmente gerenciado na nuvem da Microsoft. Baseado no SQL Server e permite criar, gerenciar e escalar bancos de dados sem precisar se preocupar com a infraestrutura física (como servidores, manutenção ou atualizações). O Azure SQL Database oferece alta disponibilidade, backups automáticos, escalabilidade sob demanda e recursos de segurança integrados.
### Caracteristicas
- Banco de dados como serviço (PaaS - Platform as a Service).
- A Microsoft gerencia backups, atualizações, alta disponibilidade e segurança.
- Ideal para quem quer focar no desenvolvimento de aplicações sem se preocupar com infraestrutura.
- Suporta escalabilidade automática e balanceamento de carga.

## Criar uma instância de banco de dados SQL do Azure
### Acesse o Portal Azure
- Vá para [Portal Azure](https://portal.azure.com)
- Acesse os recursos na lateral esquerda da tela e clique em "SQl databases".
- Clique em "Criar" no centro da tela.
### Básico
- Grupo de Recursos: Selecione ou crie um novo.
- Nome do banco de dados: Nomeie o seu DB.
- Servidor: Selecione ou crie um novo. (Ao criar um novo servidor, o nome deve ser único, selecione a localização e escolha o método de autenticação).
- Ambiente de carga de trabalho: Selecione "Produção".
- Compute + Storage: Se refere ao poder computacional e ao armazenamento do database, por padrão é selecionado a opção mais cara, mas podemos alterar. Se necessário ou sentir que o banco está sofrendo com gargalos, podemos fazer alterações após criado.
- Redundância do armazenamento de backup: O Azure já cria uma estrutura de backups mas podemos selecionar como isso será distribuído na região.
### Rede
- Método de conectividade: Iremos selecionar a opção "Sem acesso", por estarmos criando para estudo, porém temos opções como "IP público" ou "IP privado", esta opção para empresas é a mais adequada e garante maior confiabilidade e segurança.
### Segurança
- Podemos encriptar os dados: mantendo acesso ao manuseio das tabelas mas sem acesso ao dados brutos.
### Configurações adicionais: 
- Ao selecionar "Amostra" recebemos uma lista ficticia para estudo.
### Rótulos (Tags)
- Etiquetas sobre os recursos que estamos criando.
### Revisar + Criar
- O Azure calcula os custos e gera um resumo das configurações que acabamos de fazer.
- Selecionar "Criar".
  
 ## Como utilizei o GitHub
- Documentar o estudo e versionar o conteúdo.
- O arquivo **README.md** contém o resumo dos conceitos abordados, e todos os arquivos estão versionados para facilitar a consulta e o compartilhamento.
- Documentação ensinando a criar uma máquina virtual.
- Documentação ensinando a criar um banco de dados dentro do Azure

## Links úteis
- [Documentação oficial do Azure](https://learn.microsoft.com/azure/)
- [Certificação AZ900 - Microsoft](https://learn.microsoft.com/certifications/exams/az-900/)
- [Criar uma máquina virtual do Windows no Portal do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
- [Criar um banco de dados individual – Banco de Dados SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/database/single-database-create-quickstart?view=azuresql&tabs=azure-portal)
- [O que é o SQL Azure?](https://learn.microsoft.com/pt-br/azure/azure-sql/azure-sql-iaas-vs-paas-what-is-overview?view=azuresql)
- [Implante o Banco de Dados SQL do Azure gratuitamente](https://learn.microsoft.com/en-us/azure/azure-sql/database/free-offer?view=azuresql)
