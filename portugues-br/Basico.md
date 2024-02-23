<details><summary><h4>Do que é composto um servidor?</h4></summary>
  
<br>

##### Um servidor é composto por:

- Computação: CPU 
- Memória: RAM 
- Armazenamento: Dados
- Banco de Dados: Armazena dados de forma estruturada
- Rede: Roteadores, switches, servidor DNS
  - Rede: cabos, roteadores e servidores conectados entre si
  - Roteador: um dispositivo de rede que encaminha pacotes de dados entre redes de computadores. Eles sabem para onde enviar seus pacotes na internet!
  - Switch: pega um pacote e o envia para o servidor/cliente correto na sua rede

 <div alignr="center">
<img src="https://thumbs2.imgbox.com/c6/e8/H9K98LHQ_t.png" />
 </div>


##### Não faz muito tempo, essa era a maneira de construir uma infraestrutura (abordagem tradicional de TI):
 <div alignr="center">
<img src="https://thumbs2.imgbox.com/4b/02/AKnOfE3s_t.png" />
 </div>

##### Problemas com a abordagem tradicional de TI

- Pagar pelo aluguel do data center
- Pagar pelo fornecimento de energia, refrigeração, manutenção
- Adicionar e substituir hardware leva tempo
- A escalabilidade é limitada
- Contratar uma equipe 24/7 para monitorar a infraestrutura
- Como lidar com desastres? (terremotos, desligamentos de energia, incêndios...)

Tudo isso pode ser externalizado? Veja o próximo tópico para aprender sobre isso.

</details>

<details>
  <summary><h4>Computação em Nuvem</h4></summary>
  <br>

  Na nossa discussão anterior, exploramos a natureza intensiva em recursos de construir e manter servidores físicos, o que muitas vezes se traduz em custos substanciais e requisitos de espaço. Felizmente, existe uma solução mais eficiente para organizar recursos de servidor. As plataformas de computação em nuvem não apenas oferecem segurança aprimorada, mas também apresentam uma alternativa mais econômica aos servidores físicos e recursos tradicionais.

<div align="center">
  <img src="https://thumbs2.imgbox.com/0d/20/ts9DxwE4_t.png" />
</div>

Uma plataforma de Computação em Nuvem abrange uma variedade abrangente de recursos, oferecendo não apenas as capacidades de um servidor tradicional, mas também uma ampla gama de serviços adicionais. Este ambiente dinâmico funciona como um hub para várias tecnologias. Por exemplo:

- **Hospede Seu Servidor:**
  - Amazon EC2 (Elastic Compute Cloud): Fornece capacidade de computação redimensionável na nuvem.
  - Amazon ECS (Elastic Container Service): Serviço altamente escalável de orquestração de contêineres.

- **Hospede Seu Banco de Dados:**
  - Amazon RDS (Relational Database Service): Bancos de dados relacionais gerenciados na nuvem.
  - Amazon DynamoDB: Um serviço de banco de dados NoSQL totalmente gerenciado.

- **Crie Sua Infraestrutura de Rede:**
  - Rede Definida por Software (SDN): Abordagem moderna de rede que virtualiza e abstrai a infraestrutura de rede.
  - Amazon VPC (Virtual Private Cloud): Permite provisionar uma seção logicamente isolada na AWS Cloud.
  - Sub-redes: Segmentos de uma rede, frequentemente criados dentro de uma VPC, para organizar e proteger recursos.

Esses exemplos apenas arranham a superfície das diversas funcionalidades disponíveis dentro de uma plataforma de computação em nuvem. Seja para implantar servidores, gerenciar bancos de dados ou projetar estruturas de rede complexas, a nuvem oferece um ecossistema versátil e escalável para todas as suas necessidades tecnológicas.

A computação em nuvem apresenta inúmeros benefícios! Continue lendo para saber mais!

</details>

<details>
<summary><h4>Tipos de Computação em Nuvem</h4></summary>
<br>
  
##### Infraestrutura como Serviço (IaaS)
  
- Fornece blocos de construção para a computação em nuvem
- Oferece rede, computadores e espaço de armazenamento de dados
- Maior flexibilidade
- Fácil paralelo com a TI tradicional no local
 - Exemplo
   <table cellspacing="0" cellpadding="0">
     <tr>
       <td> - Amazon EC2</td>
       <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /></td>
     </tr>
   </table>

##### Plataforma como Serviço (PaaS)
  
- Elimina a necessidade de sua organização gerenciar a infraestrutura subjacente
- Concentra-se na implantação e gerenciamento de suas aplicações
- Exemplo
   <table cellspacing="0" cellpadding="0">
     <tr>
       <td>- Elastic Beanstalk</td>
       <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /></td>
     </tr> 
   </table>
  
 ##### Software como Serviço (SaaS)  
 - Produto completo que é executado e gerenciado pelo provedor de serviços
 - Exemplo   
   <table cellspacing="0" cellpadding="0">
     <tr> 
       <td>- Muitos Serviços da AWS (ex: Rekognition para Aprendizado de Máquina) </td>
        <td><img width="15%" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQWPOov6TZhY9Lso6rbo4_iFQ7OfEgWgy_Fk_INpumtuiPGjltSfJPYyzlbaIbmAtcbSOQ&usqp=CAU" /></td>
     </tr>
   </table>
 <hr/>
 <div align="center">
   <img src="https://thumbs2.imgbox.com/c6/71/c5rgRvNJ_t.png" />
 </div>
</details>

<details><summary><h4>Cinco características essenciais</h4></summary>
<br>

Este modelo de nuvem é composto por cinco características essenciais:

- <b>Serviço sob demanda:</b> Os usuários podem provisionar recursos de computação, como instâncias de servidor ou armazenamento, conforme necessário, sem exigir intervenção humana do provedor de serviços.

- <b>Acesso amplo à rede:</b> Os serviços de nuvem são acessíveis pela rede por meio de mecanismos padrão, promovendo ampla disponibilidade. Os usuários podem acessar os serviços por meio de uma variedade de dispositivos, como laptops, smartphones e tablets.

- <b>Agrupamento de recursos:</b> Os recursos de computação do provedor são agrupados para atender a vários clientes, com diferentes recursos físicos e virtuais atribuídos e reatribuídos dinamicamente de acordo com a demanda. Isso possibilita a utilização eficiente de recursos e escalabilidade.

- <b>Elasticidade rápida:</b> Os recursos de computação podem ser dimensionados rapidamente para cima ou para baixo para acomodar cargas de trabalho em constante mudança. Isso garante que o ambiente de nuvem seja flexível e responsivo às demandas variáveis, proporcionando agilidade para empresas e usuários.

- <b>Serviço medido:</b> Os sistemas de nuvem controlam e otimizam automaticamente o uso de recursos, aproveitando uma capacidade de medição em algum nível de abstração apropriado ao tipo de serviço (por exemplo, armazenamento, processamento, largura de banda e contas de usuário ativas). O uso de recursos pode ser monitorado, controlado e relatado, proporcionando transparência e permitindo que os usuários paguem apenas pelos recursos que consomem.

</details><details><summary><h4>Três drivers fundamentais de custo com a AWS</h4></summary>
<br>

Existem três drivers fundamentais de custo com a AWS: computação, armazenamento e transferência de dados de saída. Essas características variam um pouco, dependendo do produto da AWS e do modelo de precificação escolhido.
</details>


<details>
  <summary><h4>Preços da Nuvem - Visão Geral Rápida</h4></summary>
  <br>

  A AWS possui 3 fundamentos de preços, seguindo o modelo de pagamento conforme o uso:

  - Computação:
    - Pague pelo tempo de computação
      <table>
          <tr>
            <td rowspan="4"><img width="30%" src="https://thumbs2.imgbox.com/65/c8/IMPrp1MZ_t.png" /></td>
          </tr>
          <tr>
          <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d88319dfa5d204f019b4284149886c59-7d586ea82f792b61a8c87de60565133d.svg" /> </td>
          </tr>
          <tr>
          <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/d43b67a293d39d11b046bd1813c804cb-4bc0ce71c93950e1ad695b25a4f1d4b5.svg" /> </td>
          </tr>
          <tr>
          <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/945f3fc449518a73b9f5f32868db466c-926961f91b072604c42b7f39ce2eaf1c.svg" /> </td>
          </tr>
      </table>

  - Armazenamento:
    - Pague pelos dados armazenados na Nuvem
      <table>
        <tr>
          <td rowspan="4"><img width="30%" src="https://thumbs2.imgbox.com/57/8c/zH60PUMU_t.png" /></td>
        </tr>
        <tr>
        <td><img src="https://d2q66yyjeovezo.cloudfront.net/icon/c0828e0381730befd1f7a025057c74fb-43acc0496e64afba82dbc9ab774dc622.svg" /> </td>
        </tr>
        <tr>
        <td><img width="8%" src="https://seeklogo.com/images/A/amazon-elastic-file-system-logo-E7053CDC9F-seeklogo.com.png" /> </td>
        </tr>
        <tr>
        <td><img width="8%" src="https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/aws-storage/choose-the-right-storage-service/images/75c6bec122ddc0a1a76b0bf99a89cae0_2-c-235-e-2-f-2448-40-c-3-8-c-7-b-e-9753-d-6-b-0-df-5.png" /> </td>
        </tr>
      </table>

  - Transferência de dados PARA FORA da Nuvem:
    - A transferência de dados PARA DENTRO é gratuita

    <table>
        <tr>
          <td><img width="25%" src="https://hotmart.s3.amazonaws.com/product_pictures/2b279618-20d6-4514-b9e4-d5feb84bc025/aws.png" /></td>
        </tr>
    </table>

  - Resolve o problema caro da TI tradicional
</details>


<details><summary><h4>Modelo de Responsabilidade Compartilhada</h4></summary>
<br>

- O Cliente é responsável pela segurança <b>NA</b> Nuvem

- A AWS é responsável pela segurança <b>DA</b> Nuvem

<div align="center">
<img src="https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg" />
</div>

<a href="https://aws.amazon.com/compliance/shared-responsibility-model" >Mais</a>
</details>

<details><summary><h4>Política de Uso Aceitável</h4></summary>
<br>

A AWS possui políticas sobre o uso da plataforma!

Você não pode usar, facilitar ou permitir que outros usem os Serviços ou o Site da AWS:

- para qualquer atividade ilegal ou fraudulenta;
- para violar os direitos de terceiros;
- para ameaçar, incitar, promover ou encorajar ativamente violência, terrorismo ou outros danos graves;
- para qualquer conteúdo ou atividade que promova exploração ou abuso sexual infantil;
- para violar a segurança, integridade ou disponibilidade de qualquer usuário, rede, computador ou sistema de comunicação, aplicativo de software ou dispositivo de rede ou computação;
- para distribuir, publicar, enviar ou facilitar o envio de emails em massa não solicitados ou outras mensagens, promoções, publicidade ou solicitações (ou "spam").

<a href="https://aws.amazon.com/aup/" >Mais</a>
</details>



<details><summary><h4>Como escolher uma Região da AWS?</h4></summary>
<br>

- Conformidade:
  - <b>com requisitos de governança de dados e legais:</b> os dados nunca saem de uma região sem a sua permissão explícita.
- Proximidade:
  - <b>para os clientes:</b> reduza a latência.
- Serviços disponíveis:
  - <b>dentro de uma Região:</b> novos serviços e recursos nem sempre estão disponíveis em todas as Regiões.
- Preços:
  - <b>avalie:</b> os preços variam de região para região e são transparentes na página de preços do serviço.

 <div alignr="center">
<img src="https://www.awsgeek.com/AWS-Regions/AWS-Regions.jpg" />
 </div>

</details>

<details><summary><h4>Zonas de Disponibilidade da AWS</h4></summary>
<br>

- Cada região tem muitas zonas de disponibilidade (geralmente 3, mínimo 3, máximo 6). Exemplo:
  - ap-southeast-2a 
  - ap-southeast-2b
  - ap-southeast-2c
- Cada zona de disponibilidade (AZ) é um ou mais centros de dados discretos com energia, rede e conectividade redundantes.
- Elas são separadas umas das outras para que estejam isoladas de desastres.
- Elas são conectadas com uma rede de alta largura de banda e latência ultra baixa.

 <div alignr="center">
  <img src="https://thumbs2.imgbox.com/d8/f4/VNzQ8gbj_t.png" />
 </div>

</details>


<details><summary><h4>Como os usuários podem acessar a AWS?</h4></summary>
<br>
<ul>
  <li>Para acessar a AWS, você tem três opções:
      <ul>
        <li>Console de Gerenciamento da AWS (protegido por senha + MFA)</li>
        <li>Interface de Linha de Comando da AWS (CLI): protegida por chaves de acesso:
          <ul>
           <li>Uma ferramenta que permite interagir com os serviços da AWS usando comandos no seu shell de linha de comando:
            <div align="center">
              <img src="https://i.ytimg.com/vi/FwbavIglhis/maxresdefault.jpg" />
            </div>
            (Isso é apenas uma ilustração. Não compartilhe suas informações de conexão da AWS!)
          </li>
          <li>Você pode usar diferentes tipos de sistemas operacionais para se conectar à AWS:
          <div align="center">
            <img src="https://www.thelambdablog.com/img/a-concise-guide-to-setting-up-the-aws-command-line-libraries-on-your-local-development-environment-850x446.png" />
           </div>
          </li>
        </ul>
      </li>
      <li>Kit de Desenvolvimento de Software da AWS (SDK) - para código: protegido por chaves de acesso:
          <ul>
            <li>Kit de Desenvolvimento de Software da AWS (AWS SDK)</li>
            <li>APIs específicas de linguagem (conjunto de bibliotecas)</li>
            <li>Permite acessar e gerenciar serviços da AWS de forma programática</li>
            <li>Incorporado dentro da sua aplicação</li>
            <li>Suporta:
                <ul>
                  <li>SDKs (JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)</li>
                  <li>SDKs para dispositivos móveis (Android, iOS, ...)</li>
                  <li>SDKs para dispositivos IoT (Embarcados, C, Arduino, ...)</li>
                </ul>
            </li>
          </ul>
      </li> 
    </ul>
  </li>  
  <li>Chaves de acesso são geradas através do Console da AWS</li>
  <li>Os usuários gerenciam suas próprias chaves de acesso</li>
  <li>Chaves de acesso são secretas, assim como uma senha. Não as compartilhe</li>
  <li>ID da Chave de Acesso ~= nome de usuário</li>
  <li>Chave de Acesso Secreta ~= senha</li>
</ul> 
</details>




