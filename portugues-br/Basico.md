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

Tudo isso pode ser externalizado?

</details>

<details>
  <summary><h4>Computação em Nuvem</h4></summary>
  <br>
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







