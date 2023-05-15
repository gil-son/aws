CloudWatch
<div align="center">
  <img src="https://assets.zabbix.com/img/brands/cloudwatch.svg" width="30%">
</div>

O Amazon CloudWatch é um serviço de monitoramento que fornece métricas e logs em tempo real de vários recursos da AWS. Ele permite que você tenha visibilidade de suas aplicações, infraestrutura e serviços, e tome ações com base nos dados recebidos. O CloudWatch pode ser usado para monitorar recursos como instâncias EC2, bancos de dados RDS, buckets S3 e outros, e pode acionar alertas com base nas métricas que você define.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Monitoramento em tempo real:</b> O CloudWatch fornece métricas e logs em tempo real de vários recursos da AWS, permitindo que você tenha visibilidade de suas aplicações, infraestrutura e serviços.</li>
    <li><b>Alertas:</b> O CloudWatch permite que você defina alarmes com base em métricas e acione ações com base nos dados recebidos.</li>
    <li><b>Gestão de logs:</b> O CloudWatch permite que você colete e analise dados de logs, e pode ser integrado com serviços da AWS, como EC2, Lambda e Elastic Beanstalk.</li>
    <li><b>Painéis:</b> O CloudWatch fornece painéis personalizáveis que permitem que você visualize e monitore seus recursos em tempo real.</li>
    <li><b>API e CLI:</b> O CloudWatch pode ser acessado por meio do Console de Gerenciamento da AWS, APIs e CLI, permitindo que você o integre com suas ferramentas e fluxos de trabalho existentes.</li>
</ul> 
</details>
<details><summary> <h3>Termos e Conceitos</h3></summary>
<ul>
<li><b>Métricas:</b> Uma métrica é um conjunto de pontos de dados ordenados no tempo que representam os valores de uma variável ao longo do tempo.</li>
<li><b>Namespaces:</b> Um namespace é um contêiner para métricas do CloudWatch e é usado para agrupar métricas relacionadas.</li>
<li><b>Logs:</b> O CloudWatch Logs é um serviço que permite monitorar, armazenar e acessar arquivos de log de instâncias da Amazon EC2, AWS CloudTrail e outros recursos em nuvem.</li>
<li><b>Grupos de Log:</b> Um grupo de log é uma coleção de fluxos de log que compartilham as mesmas configurações de retenção, monitoramento e controle de acesso.</li>
<li><b>Fluxos de Log:</b> Um fluxo de log é uma sequência de eventos de log que compartilham a mesma origem, como uma instância EC2 ou uma função Lambda.</li>
<li><b>Alarmes:</b> Um alarme é uma maneira de monitorar uma métrica ao longo do tempo e disparar ações com base nos dados que você recebe. Você pode criar alarmes que automaticamente param, terminam ou reiniciam instâncias EC2, ou enviam notificações para tópicos Amazon SNS.</li>
<li><b>Painel:</b> Um painel é uma coleção de widgets que permitem visualizar e monitorar seus recursos em tempo real.</li>
</ul> 
</details>
<details><summary><h3>Melhores Práticas</h3></summary>
<ul>
  <li>Configure alarmes do CloudWatch para notificá-lo quando determinados limites forem ultrapassados, como uso de CPU ou tráfego de rede</li>
  <li>Use CloudWatch Logs para armazenar e monitorar dados de log gerados por suas instâncias e aplicativos, e para solucionar problemas</li>
  <li>Habilite o monitoramento detalhado para coletar métricas em intervalos de um minuto em vez do intervalo padrão de cinco minutos, para ter dados mais granulares para análise e solução de problemas</li>
  <li>Use o CloudWatch Dashboards para visualizar e monitorar métricas e tendências importantes para seus recursos em uma única exibição, e compartilhe com as partes interessadas</li>
  <li>Implemente políticas do AWS Identity and Access Management (IAM) para restringir o acesso aos recursos do CloudWatch com base no princípio do menor privilégio</li>
  <li>Use os Eventos do CloudWatch para automatizar respostas a eventos em seu ambiente da AWS, como iniciar ou parar instâncias EC2 ou acionar funções do Lambda</li>
  <li>Configure o CloudWatch Synthetics para criar canários que monitoram seus pontos de extremidade e APIs, e alertá-lo quando eles apresentam erros ou problemas de latência</li>
  <li>Use o CloudWatch Container Insights para monitorar e solucionar problemas em aplicativos containerizados em execução no Amazon Elastic Container Service (ECS) ou Kubernetes</li>
</ul>
</details>
