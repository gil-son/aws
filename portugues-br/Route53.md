Amazon Route 53
<div align="center">
  <img src="https://static-00.iconduck.com/assets.00/aws-route53-icon-423x512-3ohbrj3h.png" width="25%">
</div>

Amazon Route 53 é um serviço de Sistema de Nomes de Domínio (DNS) altamente disponível e escalável fornecido pela Amazon Web Services (AWS). Ele permite que você registre e gerencie nomes de domínio, direcione solicitações de usuários para recursos globalmente distribuídos da AWS e conecte seu domínio a vários serviços da AWS.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Escalar:</b> Route 53 foi projetado para escalar com suas aplicações e pode lidar com volumes elevados de consultas necessárias para direcionar solicitações de usuários para seus recursos.</li>
    <li><b>Alta Disponibilidade:</b> Com vários servidores DNS distribuídos geograficamente, o Route 53 garante alta disponibilidade e confiabilidade para seus nomes de domínio.</li>
    <li><b>Registro de Domínio:</b> O Route 53 permite que você registre novos nomes de domínio ou transfira os existentes, sendo uma solução única para gerenciamento de DNS e registro de domínio.</li>
    <li><b>Integração com Serviços AWS:</b> Conecte facilmente seu domínio a vários serviços da AWS, como Amazon S3, EC2, Elastic Load Balancing e outros.</li>
    <li><b>Verificações de Saúde:</b> Route 53 fornece verificações de saúde para monitorar a integridade de seus recursos e rotear automaticamente o tráfego para longe de recursos não saudáveis.</li>
    <li><b>Alcance Global:</b> Utilize a rede global anycast de servidores DNS para garantir resolução de nomes de domínio com baixa latência e alto desempenho em todo o mundo.</li>
</ul> 
</details>
<details><summary> <h3>Termos e Conceitos</h3></summary>
<ul>
<li><b>Zonas Hospedadas:</b> Uma zona hospedada é um contêiner para registros e é onde você define registros DNS para seu domínio.</li>
<li><b>Registros:</b> Registros DNS dentro de uma zona hospedada definem como o tráfego é roteado para seu domínio, incluindo endereços IP, servidores de e-mail e outras informações.</li>
<li><b>Registro de Nome de Domínio:</b> O processo de registrar um nome de domínio com o Route 53, permitindo que você gerencie seus registros DNS dentro do serviço.</li>
<li><b>Políticas de Roteamento:</b> Definir como o Route 53 responde a consultas DNS. As políticas incluem roteamento simples, roteamento ponderado, roteamento baseado em latência e roteamento baseado em geolocalização.</li>
<li><b>Registros de Alias:</b> Um registro de Alias é usado para mapear seu domínio para um recurso da AWS, como um bucket S3, distribuição CloudFront ou um Balanceador de Carga Elástica, proporcionando flexibilidade e integração perfeita.</li>
<li><b>DNS Privado:</b> O Route 53 suporta DNS privado dentro de uma Virtual Private Cloud (VPC), permitindo a resolução de nomes de domínio para endereços IP privados.</li>
</ul>
</details>
<details><summary> <h3>Melhores Práticas</h3></summary>
<ul>
  <li>Monitore e gerencie regularmente suas zonas hospedadas e registros DNS para garantir precisão e confiabilidade.</li>
  <li>Implemente verificações de saúde para recursos críticos para permitir failover automático em caso de problemas.</li>
  <li>Aproveite as políticas de roteamento com base nas necessidades de sua aplicação, considerando fatores como latência, geolocalização e distribuição ponderada de tráfego.</li>
  <li>Use registros de Alias para conectar seu domínio a vários recursos da AWS sem a necessidade de endereços IP explícitos.</li>
  <li>Considere o uso do Route 53 Resolver para arquiteturas de nuvem híbrida, possibilitando a resolução de DNS entre redes locais e a AWS.</li>
  <li>Implemente autenticação de dois fatores (MFA) para maior segurança ao gerenciar configurações do Route 53.</li>
  <li>Revise e atualize regularmente as informações de registro de domínio para garantir propriedade e detalhes de contato precisos.</li>
</ul>
</details>
