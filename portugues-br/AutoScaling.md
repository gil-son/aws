Auto Scaling
<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1200/1*Xd6ZqCDKUo5Cb79c2jdUxg.png" width="50%">
</div>

O Amazon Auto Scaling é um serviço versátil que oferece ajustes automáticos de capacidade não apenas para instâncias da Amazon EC2, mas também para outros recursos da AWS. Ao dimensionar recursos de forma dinâmica com base em métricas predefinidas, como utilização de CPU ou tráfego de rede, o Auto Scaling permite otimizar o desempenho e a eficiência de custos. Além disso, ele se integra perfeitamente a vários serviços da AWS, permitindo dimensionamento dinâmico em uma ampla variedade de recursos.

<details><summary><h3>Recursos</h3></summary>
<ul>
  <li><b>Dimensionamento dinâmico:</b> O Auto Scaling ajusta automaticamente o número de instâncias da EC2, serviços Docker em execução no ECS, clusters Kubernetes no EKS, capacidade de leitura/gravação no DynamoDB, instâncias de banco de dados Aurora e outros recursos, em resposta às mudanças na demanda, garantindo que suas aplicações tenham a quantidade adequada de recursos a todo momento.</li>
  <li><b>Políticas de dimensionamento:</b> Você pode definir políticas de dimensionamento que determinam quando e como dimensionar suas instâncias EC2, serviços Docker, capacidade de leitura/gravação no DynamoDB, entre outros, com base em métricas como utilização de CPU, tráfego de rede ou métricas personalizadas.</li>
  <li><b>Integração com serviços da AWS:</b> O Auto Scaling pode ser integrado a outros serviços da AWS, como o Amazon CloudWatch, Elastic Load Balancing, AWS Identity and Access Management (IAM), para obter um dimensionamento mais eficiente e dinâmico em uma variedade de recursos.</li>
  <li><b>Monitoramento da saúde das instâncias:</b> O Auto Scaling monitora continuamente a saúde de suas instâncias EC2, contêineres, bancos de dados, etc., e substitui as instâncias não saudáveis para manter a capacidade e disponibilidade desejadas.</li>
  <li><b>Dimensionamento agendado:</b> É possível definir ações de dimensionamento agendadas para ajustar automaticamente a capacidade de suas instâncias, contêineres, bancos de dados, etc., com base em padrões previsíveis, como aumentar durante horários de pico e reduzir durante horários de menor demanda.</li>
  <li><b>Integração com o AWS Elastic Beanstalk:</b> O Auto Scaling pode ser usado com o AWS Elastic Beanstalk para dimensionar automaticamente suas aplicações web com base em padrões de tráfego.</li>
</ul>
</details>

<details><summary><h3>Termos e Conceitos</h3></summary>
<ul>
  <li><b>Grupo de Dimensionamento Automático (ASG):</b> Um grupo de dimensionamento automático é uma coleção de instâncias EC2, serviços Docker, instâncias de banco de dados, etc., que são tratadas como uma unidade lógica para dimensionamento e gerenciamento. Os grupos de dimensionamento automático definem o número mínimo, máximo e desejado de instâncias.</li>
  <li><b>Configuração de Lançamento:</b> Uma configuração de lançamento é um modelo que define as configurações de configuração para as instâncias lançadas por um grupo de dimensionamento automático.</li>
  <li><b>Política de Dimensionamento:</b> Uma política de dimensionamento é um conjunto de instruções que define como o dimensionamento automático deve dimensionar as instâncias EC2, serviços Docker, instâncias de banco de dados, etc., em resposta às mudanças na demanda.</li>
  <li><b>Plano de Dimensionamento:</b> Um plano de dimensionamento é uma configuração que permite criar e gerenciar políticas de dimensionamento usando estratégias de dimensionamento predefinidas.</li>
  <li><b>Período de Espera:</b> Um período de espera é um período de tempo configurável que impede que o dimensionamento automático inicie ou termine instâncias adicionais imediatamente após uma atividade de dimensionamento.</li>
</ul>
</details>

<details><summary><h3>Boas Práticas</h3></summary>
<ul>
  <li><b>Defina políticas de dimensionamento adequadas:</b> Analise as métricas de desempenho da sua aplicação e a demanda esperada para definir políticas de dimensionamento que garantam uma alocação ótima de recursos, seja para instâncias EC2, serviços Docker, instâncias de banco de dados, etc.</li>
  <li><b>Utilize dimensionamento dinâmico:</b> Habilite o dimensionamento dinâmico com base em métricas em tempo real para ajustar automaticamente o número de instâncias, contêineres, capacidade de leitura/gravação no DynamoDB, etc., em resposta às mudanças na demanda, garantindo um desempenho e eficiência de custo ótimos.</li>
  <li><b>Monitore e otimize:</b> Monitore regularmente e analise o desempenho da sua aplicação, e ajuste as políticas de dimensionamento conforme necessário para otimizar a alocação de recursos e manter um desempenho ideal em diversos recursos da AWS.</li>
  <li><b>Habilite o monitoramento detalhado:</b> Ative o monitoramento detalhado para seus grupos de dimensionamento automático para coletar métricas mais granulares e tomar decisões de dimensionamento mais informadas, independentemente do recurso utilizado.</li>
  <li><b>Utilize o dimensionamento agendado:</b> Aproveite as ações de dimensionamento agendadas para ajustar automaticamente a capacidade das suas instâncias, contêineres, bancos de dados, etc., com base em padrões previsíveis, como aumentar durante horários de pico e reduzir durante horários de menor demanda.</li>
  <li><b>Integre com outros serviços da AWS:</b> Aproveite a integração com outros serviços da AWS, como Amazon CloudWatch, Elastic Load Balancing, AWS Identity and Access Management (IAM), para obter um dimensionamento mais eficiente e dinâmico em uma variedade de recursos.</li>
  <li><b>Otimizar o período de espera:</b> Configure um período de espera apropriado para evitar que o dimensionamento automático inicie ou termine instâncias adicionais imediatamente após uma atividade de dimensionamento, permitindo tempo para que as novas instâncias se estabilizem, seja para instâncias EC2, serviços Docker, instâncias de banco de dados, etc.</li>
</ul>
</details>
