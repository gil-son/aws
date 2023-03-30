Lambda
<div align="center">
  <img src="https://spiraldatagroup.com.au/wp-content/uploads/2019/04/aws-lambda-logo-png-transparent.png" width="25%">
</div>

O AWS Lambda é um serviço de computação serverless que permite executar código sem a necessidade de provisionar ou gerenciar servidores. Ele permite que você crie funções que respondem a eventos, como upload de arquivos no S3, alterações em streams do Kinesis ou solicitações de API do Gateway da API do Amazon. O Lambda é escalável, confiável e pode ser usado para uma variedade de casos de uso, desde processamento de dados em tempo real até a criação de microservices para aplicativos web.
<details><summary> <h3>Recursos</h3></summary>
<ul>
    <li><b>Serverless:</b> O AWS Lambda é um serviço serverless, o que significa que você só paga pelo tempo em que o código é executado e não precisa se preocupar em provisionar ou gerenciar servidores.</li>
    <li><b>Integração com outros serviços AWS:</b> O AWS Lambda pode ser facilmente integrado com outros serviços AWS, como S3, DynamoDB, Kinesis e API Gateway.</li>
    <li><b>Escalabilidade:</b> O AWS Lambda é altamente escalável e pode ser usado para lidar com cargas de trabalho de qualquer tamanho.</li>
    <li><b>Tempo de execução personalizável:</b> O AWS Lambda suporta vários tempos de execução, incluindo Node.js, Python, Java, Go, C# e Ruby.</li>
    <li><b>Alta disponibilidade:</b> O AWS Lambda é projetado para garantir alta disponibilidade, com várias zonas de disponibilidade e recursos de failover automático.</li>
</ul> 
</details>
<details><summary> <h3>Termos e conceitos</h3></summary>
<ul>
<li><b>Funções:</b> Uma função do AWS Lambda é uma unidade de código que é executada em resposta a eventos.</li>
<li><b>Eventos:</b> Um evento é uma ação que ocorre em um serviço AWS, como upload de arquivo no S3 ou uma solicitação de API do Gateway da API do Amazon, que pode acionar a execução de uma função Lambda.</li>
<li><b>Tempo de execução:</b> O tempo de execução é o ambiente em que o código da função Lambda é executado.</li>
<li><b>Camadas:</b> As camadas permitem que você inclua bibliotecas, frameworks e outros arquivos de dependência na sua função Lambda, mantendo a separação dos seus códigos de negócios.</li>
<li><b>Política de execução:</b> A política de execução controla as permissões que uma função do Lambda tem para acessar outros recursos da AWS.</li>
<li><b>Alias:</b> Um alias é um ponteiro para uma versão específica de uma função do Lambda.</li>
</ul>
</details>

<details><summary><h3>Boas práticas para o uso do AWS Lambda</h3></summary>

Algumas boas práticas para o uso do AWS Lambda incluem:
<ul>
  <li>Projetar funções Lambda para serem pequenas e executar tarefas específicas</li>
  <li>Limitar o tempo de execução das funções para evitar a execução desnecessária ou a falha devido a limites de tempo</li>
  <li>Usar variáveis de ambiente para armazenar informações sensíveis, como chaves de API e senhas</li>
  <li>Gerenciar e monitorar o registro de logs das funções para solução de problemas e depuração</li>
  <li>Usar as opções de versionamento e controle de acesso para rastrear e gerenciar alterações nas funções Lambda</li>
  <li>Configurar as políticas de controle de acesso para limitar o acesso às funções Lambda e aos recursos usados por elas</li>
  <li>Usar os recursos de monitoramento, como CloudWatch Metrics e CloudWatch Logs, para monitorar e analisar o desempenho e a eficiência da função Lambda</li>
  <li>Testar e validar as funções Lambda antes de implantá-las em produção</li>
</ul>
</details>
