EC2 Auto Scaling

<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:1200/1*Xd6ZqCDKUo5Cb79c2jdUxg.png" width="50%">
</div>

O Amazon EC2 Auto Scaling é um serviço que permite ajustar automaticamente o número de instâncias do Amazon EC2 em execução em resposta a alterações na demanda da aplicação. Com o Amazon EC2 Auto Scaling, você pode garantir que a sua aplicação tenha a capacidade necessária para lidar com a demanda atual e futura. Ele pode ajustar o número de instâncias EC2 automaticamente para lidar com picos de tráfego, além de reduzir o número de instâncias quando a demanda diminui.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Elasticidade:</b> O EC2 Auto Scaling ajusta automaticamente o número de instâncias em execução de acordo com a demanda da aplicação.</li>
<div align="center">
<img src="https://100daysofdevops.com/wp-content/uploads/2019/11/auto-scaling.png" width="50%">
</div>
  
<li><b>Escalabilidade:</b> O EC2 Auto Scaling ajuda a garantir que a sua aplicação tenha a capacidade necessária para lidar com a demanda atual e futura.</li>
  
<div align="center">
<img src="https://docs.amazonaws.cn/en_us/autoscaling/ec2/userguide/images/capacity-example-with-as-diagram.png" width="50%">
</div>  
  
  
<li><b>Balanceamento de carga:</b> O EC2 Auto Scaling trabalha em conjunto com o Elastic Load Balancing (ELB) para distribuir o tráfego entre as instâncias EC2.</li>
  
<div align="center">
<img src="https://media.amazonwebservices.com/blog/2014/elb_auto_scale_instances_2.png" width="50%">
</div>   
  
<li><b>Alta disponibilidade:</b> O EC2 Auto Scaling ajuda a garantir que a sua aplicação esteja sempre disponível, mesmo durante picos de tráfego.</li>
<li><b>Integração com outros serviços AWS:</b> O EC2 Auto Scaling pode ser facilmente integrado com outros serviços AWS, como o Amazon CloudWatch e o Amazon SNS.</li>
</ul> 
</details>
<details><summary> <h3>Termos e conceitos</h3></summary>
<ul>
<li><b>Grupos de Auto Scaling:</b> Um grupo de Auto Scaling é um conjunto de instâncias EC2 que são criadas a partir de uma única configuração. O grupo de Auto Scaling é escalado automaticamente para atender à demanda da aplicação.</li>
<li><b>Política de escala:</b> A política de escala é um conjunto de regras que o EC2 Auto Scaling segue para ajustar o número de instâncias em execução.</li>
<li><b>Métricas de escala:</b> As métricas de escala são as métricas usadas pelo EC2 Auto Scaling para determinar quando ajustar o número de instâncias em execução. Algumas métricas comuns incluem a utilização da CPU, a utilização da memória e o número de conexões de rede.</li>
<li><b>Lançamento automático:</b> O lançamento automático é o processo de criar novas instâncias EC2 automaticamente em resposta à demanda da aplicação.</li>
<li><b>Terminação automática:</b> A terminação automática é o processo de desligar instâncias EC2 automaticamente quando não são mais necessárias.</li>
</ul>
</details>

<details><summary><h3> Boas Práticas</h3></summary>

Algumas boas práticas para o uso do EC2 Auto Scaling da Amazon incluem:
<ul>
  <li>Definir alarmes e políticas de escalabilidade apropriadas para garantir que as instâncias EC2 sejam adicionadas ou removidas automaticamente conforme a demanda do aplicativo</li>
  <li>Configurar o balanceamento de carga para distribuir o tráfego entre as instâncias EC2 em execução, garantindo alta disponibilidade e escalabilidade horizontal</li>
  <li>Monitorar o uso das instâncias EC2 e definir alertas para anomalias ou problemas de segurança</li>
  <li>Usar as opções de configuração para garantir que as instâncias EC2 tenham a capacidade e os recursos necessários para atender à demanda do aplicativo</li>
  <li>Automatizar a implantação de aplicativos em instâncias EC2 para reduzir o tempo de inatividade e garantir a consistência entre as diferentes instâncias</li>
</ul>

É importante lembrar que o EC2 Auto Scaling é uma ferramenta poderosa para garantir a escalabilidade e a disponibilidade dos aplicativos, mas sua configuração deve ser cuidadosa e bem planejada. Além disso, é importante monitorar constantemente o desempenho do aplicativo e ajustar as políticas de escalabilidade de acordo com as mudanças na demanda e no uso.
