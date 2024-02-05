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
  <details><summary><h4>Escalabilidade</h4></summary>
        <ul>
          <li>Escalabilidade significa que a aplicação/sistema pode lidar com cargas maiores ao se adaptar.</li>
          <li>Há dois tipos de escalabilidade:
            <ul>
              <li>Escalabilidade Vertical
                <ul>
                  <li>Escalabilidade Vertical significa aumentar o tamanho da instância.</li>
                  <li>Melhorar qualquer parte da instância.</li>
                  <li>Sua aplicação roda em um t2.micro, escalar verticalmente significa rodá-la em um t2.large, por exemplo.</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/d4/1a/yPfIV4ZR_t.png">
                  </div>
                  <li>A escalabilidade vertical é muito comum para sistemas não distribuídos, como um banco de dados.</li>
                  <li>Geralmente, há um limite para o quanto você pode escalar verticalmente (limite de hardware).</li>
                </ul>
              </li>
              <li>Escalabilidade Horizontal (= elasticidade)
                  <ul>
                  <li>Escalabilidade Horizontal significa aumentar o número de instâncias/sistemas para sua aplicação.</li>
                  <li>A escalabilidade horizontal implica em sistemas distribuídos.</li>
                  <li>Isso é muito comum em aplicações web/aplicações modernas.</li>
                  <div align="center">
                    <img src="https://thumbs2.imgbox.com/1e/13/1NerXmnE_t.png">
                  </div>
                </ul>
              </li>
            </ul>
          </li>
        </ul>
  </details>
  <details><summary><h4>Disponibilidade</h4></summary>
  <ul>
    <li>A Alta Disponibilidade geralmente está associada à escalabilidade horizontal.</li>
    <li>Alta disponibilidade significa executar sua aplicação/sistema em pelo menos 2 Zonas de Disponibilidade.</li>
    <li>O objetivo da alta disponibilidade é sobreviver à perda de um centro de dados (desastre).</li>
    <div align="center">
      <img src="https://thumbs2.imgbox.com/78/63/coxLKVbv_t.png">
    </div>
    <div align="center">
      <img src="https://thumbs2.imgbox.com/c6/b3/Sjg8TioT_t.png">
    </div>
  </ul>
</details>

 <details><summary><h4>Escalabilidade vs Elasticidade (vs Agilidade)</h4></summary>
  <ul>
    <li><b>Escalabilidade:</b> capacidade de acomodar uma carga maior tornando o hardware mais poderoso (escalar para cima) ou adicionando nós (escalar para fora)</li>
    <li><b>Elasticidade:</b> uma vez que um sistema é escalável, a elasticidade significa que haverá algum "auto-escalonamento" para que o sistema possa se adaptar à carga. Isso é "amigável à nuvem", pagamento por uso, atende à demanda, otimiza custos</li>
    <li><b>Agilidade:</b> (não relacionado à escalabilidade - distrativo) novos recursos de TI estão a apenas um clique de distância, o que significa que você reduz o tempo para disponibilizar esses recursos para seus desenvolvedores de semanas para apenas minutos.</li>
  </ul>
  <hr/>
</details> 

<details><summary><h4>Grupos de Auto Dimensionamento - Estratégias de Dimensionamento</h4></summary>
      <ul>
          <li><b>Dimensionamento Manual:</b> atualiza o tamanho de um Grupo de Auto Dimensionamento manualmente</li>
          <li><b>Dimensionamento Dinâmico:</b> responde à demanda em constante mudança
              <ul>
                <li><b>Dimensionamento Simples / por Etapas</b>
                    <ul>
                      <li>Quando um alarme CloudWatch é acionado (por exemplo, CPU > 70%), então adicione 2 unidades</li>
                      <li>Quando um alarme CloudWatch é acionado (por exemplo, CPU < 30%), então remova</li>
                        <div align="center">
                          <img src="https://100daysofdevops.com/wp-content/uploads/2019/11/auto-scaling.png" width="50%">
                        </div>
                        (Ajusta o número de instâncias em execução com base na demanda da aplicação)
                    </ul>
                </li>
                 <li><b>Dimensionamento por Acompanhamento de Alvo</b>
                    <ul>
                      <li>Exemplo: quero que a CPU média do Grupo de Auto Dimensionamento fique em torno de 40%</li>
                    </ul>
                </li>
                <li><b>Dimensionamento Agendado</b>
                    <ul>
                      <li>Antecipe um dimensionamento com base em padrões de uso conhecidos</li>
                      <li>Exemplo: aumente a capacidade mínima para 10 às 17h de quarta-feira</li>
                    </ul>
                    <div align="center">
                      <img src="https://docs.amazonaws.cn/en_us/autoscaling/ec2/userguide/images/capacity-example-with-as-diagram.png" width="50%">
                    </div>
                    (O Auto Dimensionamento ajuda a garantir que sua aplicação tenha a capacidade necessária para lidar tanto com a demanda atual quanto com a futura)
                </li>
              </ul>
          </li>
          <li><b>Dimensionamento Preditivo</b>
              <ul>
                <li>Utiliza aprendizado de máquina para prever o tráfego futuro com antecedência</li>
                <li>Provisiona automaticamente o número correto de recursos com antecedência</li>    
             </ul>
          </li>  
      </ul>
 </details>


</details>

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
