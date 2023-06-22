<h2>EC2 System Manager</h2>

<div align="center">
  <img src="https://i.ibb.co/FsrMgfn/aws.png">
</div>

O EC2 System Manager é um serviço oferecido pela Amazon Web Services (AWS) que permite gerenciar e operar instâncias EC2 de maneira simplificada. Com o EC2 System Manager, você pode realizar tarefas de gerenciamento, monitoramento, automação e segurança em suas instâncias EC2 de forma centralizada.

<details>
  <summary><h3>Recursos</h3></summary>
  <ul>
    <li><b>Visualização e controle:</b> O EC2 System Manager fornece uma interface gráfica que permite visualizar e controlar suas instâncias EC2 em um único painel de controle.</li>
    <li><b>Gerenciamento de patches:</b> Você pode usar o EC2 System Manager para aplicar patches de segurança e atualizações em suas instâncias EC2 de forma automatizada e programada.</li>
    <li><b>Acessibilidade remota:</b> O EC2 System Manager permite que você acesse suas instâncias EC2 remotamente sem a necessidade de abrir portas de entrada adicionais ou configurar VPNs.</li>
    <li><b>Automação de tarefas:</b> É possível automatizar tarefas de gerenciamento, como a execução de scripts ou comandos em várias instâncias EC2 simultaneamente.</li>
    <li><b>Métricas e monitoramento:</b> O EC2 System Manager integra-se com o Amazon CloudWatch, permitindo monitorar métricas de desempenho e definir alarmes para suas instâncias EC2.</li>
    <li><b>Segurança e conformidade:</b> O EC2 System Manager oferece recursos de segurança, como a execução de verificações de conformidade e a geração de relatórios.</li>
  </ul>
</details>

<details>
  <summary><h3>Termos e Conceitos</h3></summary>
  <ul>
    <li><b>Documentos do Systems Manager:</b> Os documentos do Systems Manager são arquivos JSON ou YAML que definem as ações a serem executadas em suas instâncias EC2. Eles são usados para configurar e controlar o comportamento do EC2 System Manager.</li>
    <li><b>Comandos do Systems Manager:</b> Os comandos do Systems Manager são instruções específicas que podem ser executadas nas instâncias EC2 por meio do EC2 System Manager. Eles permitem automatizar tarefas e executar ações em lote.</li>
    <li><b>Agent do Systems Manager:</b> O agent do Systems Manager é um software que é instalado nas instâncias EC2 e permite que elas se comuniquem e executem comandos enviados pelo EC2 System Manager.</li>
    <li><b>Logs do Systems Manager:</b> Os logs do Systems Manager registram as atividades e os resultados das ações executadas pelo EC2 System Manager em suas instâncias EC2.</li>
    <li><b>Automação de documentos:</b> A automação de documentos é um recurso do EC2 System Manager que permite criar fluxos de trabalho automatizados para realizar tarefas repetitivas.</li>
  </ul>
</details>

<details>
  <summary><h3>Boas Práticas</h3></summary>
  <ul>
    <li><b>Utilize o recurso de Patch Manager:</b> Aproveite o Patch Manager do EC2 System Manager para manter suas instâncias EC2 atualizadas com os últimos patches de segurança. Configure políticas de patch para automatizar o processo de aplicação de patches.</li>
    <li><b>Implemente uma estratégia de backup:</b> Faça uso do EC2 System Manager para criar snapshots de volumes EBS e armazená-los em um local seguro. Isso ajudará a proteger seus dados e facilitará a recuperação em caso de falhas.</li>
    <li><b>Monitore métricas e defina alarmes:</b> Utilize o EC2 System Manager em conjunto com o Amazon CloudWatch para monitorar métricas de desempenho e saúde de suas instâncias EC2. Configure alarmes para ser notificado sobre eventos indesejados.</li>
    <li><b>Automatize tarefas com documentos do Systems Manager:</b> Crie documentos do Systems Manager para automatizar tarefas de gerenciamento, como a instalação de software, configuração de segurança e execução de scripts. Isso ajuda a reduzir erros manuais e agiliza processos.</li>
    <li><b>Utilize o Systems Manager Run Command:</b> O Systems Manager Run Command permite executar comandos em várias instâncias EC2 simultaneamente. Aproveite esse recurso para executar ações em lote, como atualizações de software ou reinicializações.</li>
    <li><b>Implemente políticas de acesso granulares:</b> Utilize o AWS Identity and Access Management (IAM) para definir políticas de acesso granulares ao EC2 System Manager. Isso garante que apenas as pessoas autorizadas tenham permissões para gerenciar e operar as instâncias EC2.</li>
  </ul>
</details>
