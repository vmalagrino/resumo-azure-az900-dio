# Resumo Azure - Certificação AZ900 - DIO
Resumo sobre o Microsoft Azure - Certificação AZ900 - DIO

## Introdução
Este repositório contém um resumo dos conceitos aprendidos durante o estudo da certificação AZ900 da Microsoft, cobrindo aspectos básicos do Azure.

## O que é a computação em nuvem?
- É o fornecimento de serviços de computação pela internet, habilitando inovações mais rápidas, recursos flexíveis e economia de escala.
- É a virtualização de uma empresa, de modo IaaS, pagando apenas pelo uso.

## Modelos
### PRIVADA
- A empresa cria a sua nuvem, um ambiente interno em seu data center, sem os grandes players, este modelo também se chama on-premise.
- A empresa é responsável por operrar os serviços e não gera acessos a usuários de fora da organização.
### PÚBLICA
- Entrega de serviços e recursos para diversas organizações e usuários, através de um provedor de hosting.
- Acesso via conexão de rede segura.
-  Empresas deste segmento, Microsoft (Azure), Amazon (AWS), Google (GCP), Oracle (Oracle Cloud).
### HÍBRIDA
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

### Como criar uma máquina virtual com Azure



## COmo utilizei o GitHub
- Documentar o estudo e versionar o conteúdo.
- O arquivo **README.md** contém o resumo dos conceitos abordados, e todos os arquivos estão versionados para facilitar a consulta e o compartilhamento.

## Links úteis
- [Documentação oficial do Azure](https://learn.microsoft.com/azure/)
- [Certificação AZ900 - Microsoft](https://learn.microsoft.com/certifications/exams/az-900/)
- [Criar uma máquina virtual do Windows no Portal do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
