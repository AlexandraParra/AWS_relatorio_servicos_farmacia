# RELATÓRIO DE IMPLEMENTAÇÃO DE SERVIÇOS AWS

Data: 07/06/2025<br>
Empresa: Abstergo Industries<br>
Responsável: Alexandra Parra

## Introdução
Este relatório apresenta o processo de implementação de ferramentas na Abstergo Industries, realizado por Alexandra Parra. O objetivo do projeto foi elencar 3 serviços da AWS (Amazon CloudFront, Amazon EC2 Auto Scaling e Amazon SQS) selecionadas por sua capacidade de otimizar recursos, automatizar processos e aprimorar a experiência dos usuários. Com a finalidade de reduzir custos imediatos, melhorar o desempenho dos sistemas e garantir maior escalabilidade, marcando o primeiro passo da empresa rumo à modernização de sua infraestrutura tecnológica.

## Descrição do Projeto
O projeto de implementação de ferramentas foi dividido em 3 etapas, cada uma com seus objetivos específicos. A seguir, são descritas as etapas do projeto:

<b>Etapa 1:</b>
- Nome da ferramenta: Amazon CloudFront

- Foco da ferramenta: O Amazon CloudFront é uma CDN (Content Delivery Network) que distribui conteúdos com baixa latência e alta velocidade.
Essa ferramenta reduz a carga sobre os servidores de origem, economizando em largura de banda e processamento.
O principal benefício é a melhoria significativa no desempenho e na experiência do usuário, especialmente no acesso ao site e ao catálogo de produtos da empresa.

- Descrição de caso de uso: O site institucional e o catálogo de produtos da empresa farmacêutica serão entregues ao público via CloudFront.
Em vez de os arquivos (imagens, PDFs, vídeos, etc.) serem servidos diretamente do servidor principal, eles serão armazenados e disponibilizados a partir de locais de borda (edge locations) distribuídos geograficamente.
Com isso, o tempo de carregamento é reduzido, a experiência do cliente é otimizada e os custos com tráfego no servidor de origem são consideravelmente menores.


<b>Etapa 2:</b> 
- Nome da ferramenta: Amazon EC2 Auto Scaling

- Foco da ferramenta: O EC2 Auto Scaling permite ajustar automaticamente a quantidade de instâncias EC2 conforme a demanda da aplicação.
Isso evita custos com servidores ociosos, pois as instâncias são ativadas apenas quando necessário.
O principal ganho é a otimização de custos com infraestrutura e a garantia de alta disponibilidade.

- Descrição de caso de uso: A empresa poderá migrar seu sistema ERP ou plataforma de pedidos para uma aplicação hospedada em instâncias EC2.
Será criado um grupo de Auto Scaling com políticas baseadas, por exemplo, na utilização de CPU acima de 70%.
Durante horários de pico, novas instâncias são provisionadas automaticamente. Quando a demanda diminui, elas são encerradas.
Isso garante que o ambiente se ajuste dinamicamente à carga de trabalho, sem intervenção manual e sem custos desnecessários.


<b>Etapa 3:</b>
- Nome da ferramenta: Amazon Simple Queue Service (SQS)

- Foco da ferramenta: O Amazon SQS é um serviço de fila de mensagens que permite o desacoplamento entre componentes do sistema.
Ele reduz os custos operacionais ao evitar o uso constante de recursos síncronos e possibilita o processamento assíncrono de tarefas.
O principal benefício é a eficiência no uso de recursos computacionais, promovendo escalabilidade e resiliência.

- Descrição de caso de uso: Quando um pedido é realizado, em vez de processar todas as ações em tempo real (como envio de e-mails, atualização de estoque e emissão de nota fiscal), essas tarefas são enfileiradas no SQS.
Um serviço consumidor (executado em uma instância EC2, container ou função Lambda) irá processar essas mensagens em segundo plano.
Isso mantém o sistema principal leve e responsivo, além de permitir escalar os processamentos secundários conforme a demanda, pagando apenas pelo uso efetivo.

## Conclusão
A implementação das ferramentas na empresa Abstergo Industries trouxe benefícios como melhoria no desempenho do site, redução de custos com infraestrutura e tráfego, além de maior escalabilidade e eficiência nos processos, o que aumentará a eficiência e a produtividade da organização. Recomenda-se a continuidade da utilização das ferramentas implementadas e a busca por novas tecnologias que possam aprimorar ainda mais os processos da empresa.


## Anexos
- Manual de configuração do Amazon CloudFront.
- Documento com a política de escalonamento do Amazon EC2 Auto Scaling.
- Fluxo de mensagens e configuração da fila Amazon SQS.
<br>
Assinatura do Responsável pelo Projeto:

Alexandra Parra
