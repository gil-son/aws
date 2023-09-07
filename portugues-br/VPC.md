<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:2570/1*YcNHxdrbPlV-lWjN_0Ek3g.png" width="50%">
</div>
<br/>

   <h2>Como organizar os Recursos?</h2>
<p>
  <ul>
   <li>
     <b>Escritório:</b>
       <img src="https://i.ytimg.com/vi/_x9gZt2Lw9Y/maxresdefault.jpg" /> 
   </li>
    <li>
     <b>Nuvem:</b>
       <img src="https://docs.aws.amazon.com/pt_br/AmazonRDS/latest/UserGuide/images/con-VPC-sec-grp.png" /> 
   </li>
  </ul>
</p>

<p>A Amazon Virtual Private Cloud (Amazon VPC) é um serviço de rede que permite que você crie uma rede virtual isolada na nuvem da Amazon. Com a Amazon VPC, você pode criar uma rede personalizada com sub-redes, roteamento, tabelas de roteamento, gateways de Internet, entre outros recursos, proporcionando controle total sobre sua infraestrutura de rede na nuvem.
</p>

<details><summary> <h3>Recursos</h3></summary>
<ul>
   <li>
     <b>Sub-rede privada:</b>
       <p>Imagine que existe uma instância EC2 no qual acessa o banco de dados, onde devolve alguma informação para outra instÂncia EC2, não faz sentido estar exposto na internet, logo está em uma sub-rede  privada.</p>
   </li>
    <li>
     <b>Sub-rede pública:</b>
       <p>A instância de sub-rede pública é conectada com a internet, pode receber tanto dados de entrada quanto de saída. É uma instância de um servidor HTTP que pode receber ou fazer requisições, normalmente feitas via Gateway</p>
        <img src="https://res.cloudinary.com/practicaldev/image/fetch/s--gLjFa2Xt--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_800/https://dev-to-uploads.s3.amazonaws.com/uploads/articles/nti327hmr7a642l03njz.png" />
    </li>
    <li><b>Conectividade e Segurança:</b> 
        <ul>
          <li>
            <p>VPC permite estabelecer conexões VPN (Virtual Private Network) para conectar em sub-rede privada à sua infraestrutura na nuvem:</p>
        <img src="https://uploads-ssl.webflow.com/611b82111c177de53409c4b5/624465dfe2552c5f29e83625_iE6_z3bFB8uMSnfUz8R2uHqvlYh0E7_mAi7odxPszG5GeA4OXTwp6s8GYKf1N8AFS6OcYCDrHBpouNps1VohYqXTvlV_ZmLCG0xKogzjPjRTT8txNbOqv9oh64W-rqJJ2WqrQgG_.png" />
          </li>
           <li>
            <p>Caso seja necessário mais segurança e velocidade na interação dos recursos, sem ser pela internet em si, ou seja, uma conexão dedicada, com redes isoladas, é possível pela AWS Direct Connect:</p>
    <img src="https://www.w3schools.com/aws/images/directconnect.png" />
          </li>
        </ul>
    </li>
    <li><b>Listas de controle de acesso:</b><p>A nível de sub-rede, para que os dados trafeguem em uma VPC de forma segura, é bacana utilizar uma configuração que é chamado de Network ACLs (Access Control List). O Network ACL é uma lista de controle de acesso que age como um firewall a nível de sub-rede da VPC (Virtual Private Cloud):</p>
    <img src="https://docs.aws.amazon.com/images/vpc/latest/userguide/images/security-diagram_updated.png" />
    <p>
      O Network ACLs possui comportamento Stateless, logo não armazena estado, ele tem regras para entradas e saídas de dados. Por exemplo: entrou um pacote dados para um banco, foi verificado e dentro das configurações foi permitida tal entrada, mas isso não significa que a saída vai ser permitida, também será verificada dentro do que foi permitido (pode ser configurada).
    </p>
    </li>
    <li><b> Grupos de Segurança:</b><p>A nível de EC2, com recursos como grupos de segurança, o comportamento muda para Stateful, então tudo que pôde entrar, pode sair. Logo só será barrada a entrada, se passou, então a saída não será verificada. Essa é a configuração padrão (pode ser ajusta):</p>
    <img src="https://uploads-ssl.webflow.com/611b82111c177de53409c4b5/624465dfa8356e5ee15fe3ce_A0pF_xA7TfbCk8yMYt3AmKtVWL7f0_3yZvrYulgIxW_Gt4H6Q-vfqeqCnjrM03SktstA1IUZS-GmsM3xbumitDsTXSM-FI87Lb00dedOS_C1pTi7ZXd9q0kF4h8a4h4ytP94j4eN.png" />
    </li>
    <li><b>Personalização:</b> Você pode personalizar sua VPC definindo sub-redes, tabelas de roteamento, gateways de Internet e outros recursos de rede de acordo com suas necessidades.</li>
    <li><b>Elasticidade:</b> A Amazon VPC é altamente escalável, permitindo a adição de recursos de rede conforme sua infraestrutura cresce.</li>
</ul> 
</details>
<details><summary> <h3>Termos e conceitos</h3></summary>
<ul>
<li><b>Sub-redes:</b> As sub-redes na Amazon VPC são divisões lógicas de sua rede virtual, onde você pode executar recursos e aplicar configurações de segurança.</li>
<li><b>Tabelas de Roteamento:</b> As tabelas de roteamento na VPC determinam como o tráfego de rede é encaminhado entre sub-redes, gateways e outros recursos de rede.</li>
<li><b>Gateway de Internet:</b> Um Gateway de Internet permite que recursos em suas sub-redes acessem a Internet de forma controlada.</li>
<li><b>Grupos de Segurança:</b> Grupos de segurança são conjuntos de regras de firewall que controlam o tráfego de entrada e saída de recursos na VPC.</li>
<li><b>Network ACLs:</b> As listas de controle de acesso de rede são regras de segurança em nível de sub-rede que controlam o tráfego de rede entre sub-redes.</li>
<li><b>VPN (Virtual Private Network):</b> Uma VPN permite estabelecer uma conexão segura entre sua rede local e sua VPC na nuvem, estendendo sua infraestrutura de rede.</li>
</ul>
</details>
<details><summary> <h3>Boas práticas</h3></summary>
<ul>
  <li>Planejar cuidadosamente a estrutura de sua VPC, incluindo a definição de sub-redes e tabelas de roteamento para atender às necessidades de sua aplicação.</li>
  <li>Utilizar grupos de segurança para controlar o tráfego de rede de entrada e saída para recursos em sua VPC.</li>
  <li>Implementar listas de controle de acesso de rede (Network ACLs) para adicionar camadas adicionais de segurança em nível de sub-rede.</li>
  <li>Utilizar gateways de Internet somente quando necessário, e aplicar políticas de controle de acesso para garantir a segurança.</li>
  <li>Configurar conexões VPN seguras para conectar sua rede local à sua VPC, estendendo sua infraestrutura de rede de forma segura.</li>
  <li>Monitorar o tráfego de rede e configurar alertas para detectar atividades suspeitas ou problemas de desempenho.</li>
  <li>Manter uma documentação clara da configuração de sua VPC e seus recursos de rede para facilitar a gestão e solução de problemas.</li>
</ul>
</details>
