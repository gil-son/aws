<div align="center">
  <img src="https://miro.medium.com/v2/resize:fit:2570/1*YcNHxdrbPlV-lWjN_0Ek3g.png" width="50%">
</div>
<br/>
A Amazon Virtual Private Cloud (Amazon VPC) é um serviço de rede que permite que você crie uma rede virtual isolada na nuvem da Amazon. Com a Amazon VPC, você pode criar uma rede personalizada com sub-redes, roteamento, tabelas de roteamento, gateways de Internet, entre outros recursos, proporcionando controle total sobre sua infraestrutura de rede na nuvem.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Isolamento:</b> A Amazon VPC permite a criação de redes virtuais isoladas para separar sua infraestrutura na nuvem em ambientes distintos.</li>
    <li><b>Personalização:</b> Você pode personalizar sua VPC definindo sub-redes, tabelas de roteamento, gateways de Internet e outros recursos de rede de acordo com suas necessidades.</li>
    <li><b>Conectividade:</b> A VPC permite estabelecer conexões VPN (Virtual Private Network) para conectar sua rede local à sua infraestrutura na nuvem.</li>
    <li><b>Segurança:</b> Com recursos como grupos de segurança e listas de controle de acesso de rede (Network ACLs), você pode controlar o tráfego de rede para manter sua infraestrutura segura.</li>
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
