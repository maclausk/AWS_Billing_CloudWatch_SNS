<h1>
    <span><center>Projeto AWS: Monitoramento de Custos com Billing, CloudWatch e SNS</center></span>
</h1>


## Introdução
Neste projeto, vamos configurar um ambiente AWS que utiliza os serviços de Billing, CloudWatch e SNS para monitorar e alertar sobre os custos da AWS. Isso é crucial para garantir que os gastos estejam sempre sob controle e que possamos reagir rapidamente a quaisquer aumentos inesperados.


## Conceitos

### AWS Billing and Cost Management
- Permite visualizar e gerenciar os custos e o uso dos serviços AWS, configurar relatórios de faturamento e definir orçamentos com alertas para monitorar os gastos.

### Amazon CloudWatch
- É um serviço de monitoramento que permite acompanhar os recursos e aplicações da AWS em tempo real, configurar métricas e alarmes para reagir a mudanças nos gastos.

### Amazon Simple Notification Service (SNS)
- É um serviço de mensagens que entrega notificações via e-mail, SMS ou HTTP/HTTPS quando os alarmes do CloudWatch são acionados.

<!-- Verificar os itens que irão compor essa arquitetura ou se de fato não terá arquitetura -->


## Passo a Passo

### 1. Configuração de Alarme de Orçamento no Billing
**Acesse o console de Billing da AWS:**
- Navegue até a seção de Billing no console da AWS.

**Crie um Orçamento:**
- Clique em "Budgets" e depois em "Create budget".
- Escolha "Cost budget" e configure o orçamento com o valor desejado.
- Defina os alertas de orçamento, especificando quando você deseja ser notificado (ex: quando atingir 80% do orçamento).

**Configurar Alarme de Orçamento:**
- Na seção de alertas, configure os detalhes do SNS, como o tópico e os assinantes que receberão as notificações.

### 2. Configuração de Métricas e Alarmes no CloudWatch
**Acesse o console do CloudWatch:**
- Navegue até o console do CloudWatch na AWS.

**Crie uma Regra de Métricas:**
- Na seção de Métricas, selecione as métricas de uso e custo que deseja monitorar.
- Por exemplo, selecione as métricas de "EstimatedCharges".

**Criação de Alarme:**
- Clique em "Create Alarm" e configure o alarme para a métrica selecionada.
- Defina o limite que, ao ser atingido, disparará o alarme (ex: $100).

**Configuração de Notificação do Alarme:**
- Associe o alarme a um tópico SNS para receber notificações quando o limite for atingido.
- Escolha ou crie um tópico SNS e adicione os e-mails ou números de telefone que devem receber as notificações.

### 3. Configuração do SNS para Envio de Notificações
**Acesse o console do SNS:**
- Navegue até o console do SNS na AWS.

**Criação de Tópico:**
- Clique em "Create topic" e escolha um nome para o tópico (ex: "CostAlerts").

**Adicionar Assinantes:**
- No tópico criado, adicione assinantes que receberão as notificações.
- Pode ser e-mail, SMS ou endpoints HTTP/HTTPS.

**Testar a Configuração:**
- Envie uma mensagem de teste para garantir que todos os assinantes estão recebendo as notificações.

## Conclusão
Este projeto demonstra como configurar uma arquitetura para monitoramento de custos na AWS utilizando Billing, CloudWatch e SNS. Essa configuração ajuda a manter os gastos sob controle e a ser alertado em tempo real sobre qualquer anomalia, permitindo ações rápidas e eficientes para gerenciar os custos.

---

### 12. Referências

- [AWS Billing and Cost Management - Documentation](https://docs.aws.amazon.com/account-billing/)
- [AWS CloudWatch - Documentation](https://aws.amazon.com/pt/cloudwatch/)
- [AWS SNS - Documentation](https://aws.amazon.com/pt/sns/)
---

### 13. Contato
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maclausk/)
[![E-mail](https://img.shields.io/badge/-Email-000?style=for-the-badge&logo=microsoft-outlook&logoColor=007BFF)](mailto:maclausk@yahoo.com.br)

