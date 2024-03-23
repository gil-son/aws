AWS Snow Family
<div align="center">
  <img src="https://thumbs2.imgbox.com/5c/94/COU1p1I7_t.png">
</div>
<br/>

A AWS Snow Family é um conjunto de dispositivos físicos projetados para transferir dados de forma segura e eficiente entre ambientes locais e a AWS Cloud. Esses dispositivos ajudam organizações com grandes volumes de dados a superar desafios relacionados à transferência de dados, migração e computação de borda. Eles são úteis quando é necessário executar operações em ambientes sem muitas condições, fora de data centers, e em locais onde há falta de conectividade de rede consistente:

  Dispositivos portáteis altamente seguros para coletar e processar dados na borda, e migrar dados para dentro e para fora da AWS. Existem 2 casos de uso, Migração de Dados e Computação de Borda.
      Computação de Borda:
          Snowcone
          Snowball Edge
      Migração de Dados:
          Snowcone
          SnowBall Edge
          Snowmobile
      <table>
        <tr>
          <th></th>
          <th>Snowcone & Snowcone SSD</th>
          <th>Snowball Edge Storage Optimized</th>
          <th>Snowmobile</th>
        </tr>  
        <tr>
          <td>Capacidade de Armazenamento</td>
          <td>8 TB HDD 14TB SSD</td>
          <td>80 TB utilizável</td>
          <td><100 PB</td>
        </tr>
        <tr>
          <td>Tamanho da Migração</td>
          <td>Até 24 TB, online e offline</td>
          <td>Até PBs, offline</td>
          <td>Até EB, offline</td>
        </tr>
        <tr>
          <td>Agente DataSync</td>
          <td>Pré-instalado</td>
          <td></td>
          <td></td>
        </tr>
  </table>

<hr/>
#### Por que Migrar Dados com a Família AWS Snow?

Bem, se olharmos para os tempos necessários para transferir muitos dados pela rede, pode levar muito tempo. Então, por exemplo, se quisermos transferir 100 terabytes por uma linha de rede de um gigabit por segundo, levará 12 dias para conseguirmos, certo?

E então, obviamente, se fizermos um petabyte, levará uma eternidade e assim por diante.
<div align="center">
<table>
  <tr>
    <th rowspan=2></th>
    <th colspan=3>Tempo de Transferência</th>
  </tr>
  <tr>
    <th>100 Mbps</th>
    <th>1 Gbps</th>
    <th>10 Gbps</th>
  </tr>
  <tr>
    <th>
      10 TB
    </th>
    <td>
      12 dias
    </td>
    <td>
      30 horas
    </td>
    <td>
      3 horas
    </td>
  </tr>
  <tr>
    <th>
      100 TB
    </th>
    <td>
      124 dias
    </td>
    <td>
      12 dias
    </td>
    <td>
      30 horas
    </td>
  </tr>
  <tr>
    <th>
      1 PB
    </th>
    <td>
      3 anos
    </td>
    <td>
      124 dias
    </td>
    <td>
      12 dias
    </td>
  </tr>
</table>
</div>

Então, como podemos ver, às vezes queremos que os dados cheguem à AWS rapidamente, e o desafio é que, às vezes, além de ter uma pequena transferência de rede, você tem conectividade limitada, largura de banda limitada, transferir dados pela rede pode custar dinheiro. Não é gratuito usar uma rede. Pode ser também que a largura de banda seja compartilhada. Por exemplo, se você baixar um vídeo da AWS e baixar 10 terabytes de dados, talvez vá bloquear toda a sua empresa, porque estará maximizando a banda na sua empresa. E então talvez a conexão não seja estável o suficiente. Então, você tem que tentar novamente, e assim por diante. Então, todas essas razões justificam o uso da Família Snow.

AWS Snow Family: dispositivos offline para realizar migrações de dados Se levar mais de uma semana para transferir pela rede, use os dispositivos Snowball!

  Upload direto para o S3:
      Se quisermos fazer o upload diretamente de um arquivo para o Amazon S3, o cliente envia os dados para o Amazon S3.
  <div align="center">
    <img src="https://thumbs2.imgbox.com/e7/e7/Ih9IrkFy_t.png" width="50%">
  </div>

  Com a Família Snow:
      Com o dispositivo da Família Snow, os clientes solicitam um dispositivo Snow. Nós o recebemos via correio, certo? A AWS entregará os dispositivos para nós. Carregamos os dados diretamente nos dispositivos localmente e, em seguida, os <b>enviamos de volta</b> para a AWS, para uma instalação da AWS. Então, eles pegarão o dispositivo e o conectarão à sua própria infraestrutura. E então os dados serão importados ou exportados com base no que você deseja fazer para um bucket Amazon S3 e você está pronto para começar.
   <div align="center">
    <img src="https://thumbs2.imgbox.com/9d/dd/WHpoBWQI_t.png">
  </div>

  Então, realmente é uma forma de transferir dados para a AWS, mas através da rota física, não da rota de rede

<hr/>

#### Computação de Borda (para transferência de dados)

<details>
   <summary>Snow Ball Edge</summary>
   <div align="center">
    <img src="https://www.ktexperts.com/wp-content/uploads/2019/11/Snowball-closed-600w.png" width="25%">
  </div>
  Snowball Edge é uma caixa enorme como você pode ver e será usada para:
    <ul>
      <li>Solução de transporte físico de dados, mover TBs ou PBs para dentro ou fora da AWS.</li>
      <li>Alternativa para mover dados pela rede (e pagar taxas de rede)</li>
      <li>Pagar pelo trabalho de transferência de dados</li>
      <li>Fornecer armazenamento em bloco e armazenamento de objeto compatível com o Amazon S3</li>
      <li><b>Snowball Edge Storage Optimed:</b> 80 TB de capacidade HDD para volume de bloco e armazenamento de objeto compatível com S3</li>
      <li><b>Snowball Edge Compute Optimed:</b> 42 TB de capacidade HDD ou 28 TB de capacidade NVMe para volume de bloco e armazenamento de objeto compatível com S3</li>
      <li>Casos de uso: grandes migrações de dados na nuvem, desativação de data center, recuperação de desastres</li>
    </ul>
</details>
<hr/>

#### Migrações de Dados

<details>
  <summary>AWS Snowcone</summary>
  <div align="center">
    <img src="https://mms.businesswire.com/media/20200617005657/en/799138/4/4440824_AWS_Snowcone_E_Ink_Label.jpg" width="25%">
  </div>

AWS Snowcone e Snowcone SSD:
  <ul>
    <li>Pequeno, computação portátil, em qualquer lugar, resistente e seguro, suporta ambientes severos</li>
    <li>Dispositivo usado para computação de borda, armazenamento e transferência de dados</li>
    <li>Snowcone - 8 TB de armazenamento HDD</li>
    <li>Snowcone SSD - 14 TB de armazenamento SSD</li>
  </ul>

Você usará o Snowcone onde o Snowball não couber, por exemplo, em um ambiente com espaço restrito, e você deve fornecer suas próprias baterias e cabos. Agora, para enviar os dados de volta para a AWS, você tem duas opções, Então, ou você envia os dados de volta offline enviando-os, ou pode conectar este dispositivo depois que capturou alguns dados em um data center, por exemplo, qualquer que tenha uma conexão com a internet, e então usar o serviço AWS DataSync para enviar os dados de volta para a AWS.
</details>
<details>
  <summary>AWS Snowball</summary>  
  <div align="center">
    <img src="https://www.ktexperts.com/wp-content/uploads/2019/11/Snowball-closed-600w.png" width="25%">
  </div>

  AWS Snowball é uma robusta solução de transporte de dados para transferir grandes volumes de dados de forma segura para e a partir da Nuvem AWS. Com recursos de segurança integrados e opções flexíveis de implantação, o Snowball garante transferência de dados confiável mesmo em ambientes desafiadores. Ideal para organizações que necessitam de migrações e backups de dados eficientes e de alta velocidade.

- Solução de transporte de dados em grande escala para transferir grandes quantidades de dados de forma segura para e a partir da Nuvem AWS.
- Projetado para lidar com petabytes de dados.
- Dispositivo físico com recursos de segurança integrados para proteção de dados durante o trânsito.
- Disponível em várias configurações com capacidades de armazenamento variadas.
- Adequado para casos de uso onde a transferência de dados pela internet é impraticável ou ineficiente.
- Pode ser usado em locais remotos ou de borda com conectividade de rede limitada.
- Oferece opções para transferência de dados offline enviando o dispositivo ou transferência de dados online via uma conexão de rede segura.
- Oferece integração com serviços da AWS como o AWS DataSync para transferência de dados contínua para serviços de armazenamento da AWS.
- Ideal para cenários que requerem transferência de dados rápida, segura e confiável, como migrações em larga escala, backups de dados ou operações de recuperação de desastres.

</details>
<details>
  <summary>AWS Snowmobile</summary>
  <div align="center">
    <img src="https://d1.awsstatic.com/products/Snow/Snowmobile_11082016_09_SO1_534x300.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.2a5a5677ec9c098f2c4fa915a620e5fd2baed5a4.png" width="50%">
  </div>

O Snowmobile é um caminhão real. Então, quando eles o anunciaram, eles realmente levaram um caminhão ao palco para mostrar que era um caminhão real que iria transferir dados. E então, com o Snowmobile, você pode transferir exabytes de dados:
  <ul>
    <li>Transferir exabytes de dados (1 EB = 1.000 PB = 1.000.000 TB)</li>
    <li>Cada Snowmobile terá 100 petabytes de capacidade (então você precisa de 10 Snowmobiles para atingir 1 exabyte, use vários em paralelo)</li>
    <li>Alta segurança, controlada por temperatura, GPS, vigilância por vídeo 24/7</li>
    <li>Melhor que o Snowball se você transferir mais de 10 PB</li>
  </ul>
</details>
<hr/>

### Processo de Uso

Ok, então como usamos um dispositivo da Família Snow?

Bem, você solicita o dispositivo no console para entrega. Em seguida, você instala o cliente Snowball ou usa o AWS Apps Hub que veremos nesta palestra em seus servidores. Então você conecta o Snowball aos servidores e começa a copiar os arquivos no cliente. Então você envia de volta o dispositivo quando estiver pronto. Ele irá diretamente para a instalação correta da AWS graças a um marcador E-Ink. E os dados serão carregados em um bucket S3. E então o Snowball será completamente apagado de acordo com as medidas de segurança mais altas. Etapas:
<ol>
  <li>Solicitar dispositivos Snowball no console da AWS para entrega</li>
  <li>Instalar o cliente Snowball / AWS OpsHub em seus servidores</li>
  <li>Conectar o Snowball aos seus servidores e copiar arquivos usando o cliente</li>
  <li>Enviar de volta o dispositivo quando terminar (vai para a instalação correta da AWS)</li>
  <li>Os dados serão carregados em um bucket S3</li>
  <li>O Snowball é completamente apagado</li>
</ol>

Então, isso é para a migração de dados. E esse era originalmente o único caso de uso para dispositivos Snowball. Mas o segundo caso de uso agora para a Família Snow é chamado de computação de borda.

### O que é Computação de Borda?

Computação de borda é quando você processa dados enquanto eles estão sendo criados em um local. Mas o segundo caso de uso agora para a Família Snow é chamado de computação de borda. A propósito, uma localização de borda é qualquer coisa que realmente não tenha internet ou que esteja longe de uma nuvem. Então, por exemplo, se você tiver um caminhão na estrada, ou se tiver um navio no mar, ou uma estação de mineração subterrânea, todas essas coisas podem ser chamadas de localizações de borda, porque podem produzir dados, mas não necessariamente ter conectividade com a internet.
<div align="center">
  <img src="https://thumbs2.imgbox.com/ab/cc/hRJPCEUF_t.png" width="50%">
</div>

Portanto, seja conectividade limitada ou sem acesso à internet, ou sem acesso a energia computacional. E assim, você ainda pode querer executar computação, processamento de dados nesses locais. E para isso, precisamos de computação de borda.
E então, para fazer computação de borda, podemos solicitar um dispositivo Snowball Edge ou um Snowcone, e o incorporamos a esses locais de borda e começamos a fazer computação de borda.

Portanto, os casos de uso da computação de borda são pré-processar dados, realizar aprendizado de máquina na borda sem precisar retornar à nuvem, transcodificar fluxos principais antecipadamente e, eventualmente, se necessário, transferir os dados de volta para a AWS. Você pode então enviar o dispositivo de volta para o seu Snowcone ou Snowball Edge. Essencialmente, você começa a processar os dados muito perto de onde eles estão sendo criados e, em seguida, os envia de volta para a AWS.

### Família Snow - Snow Edge

<ul>
  <li>Snowcone & Snowcone SSD (menor) 
    <ul>
      <li>2 CPUs, 4 GB de memória, acesso com fio ou sem fio</li>
      <li>Alimentação USB-C usando um cabo ou a bateria opcional</li>
    </ul>
  </li>
  <li> Snowball Edge - Computação
    <ul>
      <li>104 vCPU, 416 GiB de RAM</li>
      <li>GPU opcional (útil para processamento de vídeo ou Aprendizado de Máquina)</li>
      <li>Armazenamento utilizável de 28 TB NVMe ou 42 TB HDD</li>
      <li>Agrupamento de armazenamento disponível (até 16 nós)</li>
    </ul>
  </li>
  <li> Snowball Edge - Otimizado para Armazenamento
    <ul>
      <li>Até 40 vCPUs, 80 GiB de RAM, 80 TB de armazenamento</li>
    </ul>
  </li>
  <li>Todos: Podem executar Instâncias EC2 e funções AWS Lambda (usando AWS IoT Greengrass)</li>
  <li>Opções de implantação de longo prazo: precificação com desconto de 1 e 3 anos</li>
</ul>

### AWS OpsHub

Finalmente, para a Família Snow, existe o OpsHub:
<ul>
  <li>Historicamente, para usar dispositivos da Família Snow, você precisava de uma CLI (ferramenta de Interface de Linha de Comando)</li>
  <li>Hoje, você pode usar o AWS OpsHub (um software que você instala em seu computador) para gerenciar seu Dispositivo da Família Snow
    <ul>
      <li>Desbloqueio e configuração de dispositivos individuais ou em cluster</li>
      <li>Transferência de arquivos</li>
      <li>Inicialização e gerenciamento de instâncias em execução nos Dispositivos da Família Snow</li>
      <li>Monitoramento de métricas do dispositivo (capacidade de armazenamento, instâncias ativas no seu dispositivo)</li>
      <li>Inicialização de serviços AWS compatíveis em seus dispositivos (por exemplo: instâncias Amazon EC2, AWS DataSync, Sistema de Arquivos de Rede (NFS))</li>
    </ul>
  </li>
</ul>
<br/>
<div align="center">
  <img src="https://media.amazonwebservices.com/blog/2020/oh_dash_1.png">
</div>

