## Trilha Engenheira de Dados 

### 1 - Git e Versionamento
- **O que é versionamento?**
    - Registo de mudanças em arquivos, que possibilida a recuperação ou o acesso de versões anteriores.
    - Desenvolvimento de código em colaboração com outros integrantes.
- **O que é o Git?**
    - É  um sistema de versionamento, guarda  snapshots do estado do projeto, e o caminho.
### 2 - Redes e Sistemas
- Dois ou  mais dispositivos eletrônicos conectados entre si, que trocam informações por protocolo.
    - Conexão física via cabos
    - Conexial ou fibra óptica
    - Via Wireless através de rádio frequência, Bluetooth ou infravermelho
- **NIC** 
    - Placa de rede, responsável por permitir a conexão do computador com o cabo de rede Ethernet, ou por receber as onodas de rádio frequência.
- **Switch**
    - Comutação dos quadros entre os dispositivos, encaminhamento de informações.
- **Roteador** 
    - Tem a responsabilidade de procurar as melhores rotas na internet para entregas os pacotes do remetente ao destinatário no menor tempo possível.
- **Modem** 
    - É o equipamento responsável pela modulação e demodulação do sinal de Internet. 
- **ICANN**
    - A responsabilidade é de distribuir os endereçoes IP's e gerenciar os servidores DNS's
- **Cabeamento**
    - Padrões estabelecidos que definem como serão as organizações dos cabos e seus periféricos possibilitando melhor organização e performance na rede. 
- **Cabo par trançado**
    - UTP e STP, divididos em categorias que determinam a velocidade de tramissão de dadoes e o alcance em metros que o cabo pode suportar sem a perda de pacotes.
    - Cabo Coaxial, composto por fios de cobre e um fio central responsável por ser o condutor do pulso elétrico,malha metálica realizndo isolamento e uma blindagem plástica contra interferências.
- **Fibra Óptica**
    - Composta por pedaços de vidros que permitem a propagação dos raios de luz que são convertidos por conversores nas extremidades das fibras.
- **Rack** 
    - É um armário para hospedar os equipamentosde hardwares como tudo citado acima e organizar as coisas.
- **Modelo OSI**
    - 7 camadas, respectivamente: Física, Enlace, Rede, Transporte, Sessão, Apresentação e Aplicação.
    - Não confirma o recebimento de dados
- **Modelo TCP/IP**
    - 4 camadas, respectivamente: Acesso a Rede, Internet, Transporte e Aplicação. 
    - Confirma o recebimento de dados
- **IP Internet Protocol**
    - Responsável pelo endereçamento dos pacotes de rede na camada 3 do modelo OSI, ou seja, responsável por gerar um endereço no compudador ou qualquer.servidor, no momento que este conecta-se à internet.
    A tabela de classes pode determinar qual será a quantidade de hosts e de redes presentes em cada classe.
- **IPV4**
    - Formado de 32 bits
- **IPV6**
    - Formados por 128 bits
- **Domínios, DNS e latência**
    - Domínios raiz
    - https:// -> protocolo
    - www -> subdominio
    - nome -> dominio
    - .com -> TLD
    - .br -> subdiretório
    - latência pequena a velocidade é rápida
    - latência grande causa lentidão
    - o funcionamento do fluxo de uma resolução DNS é basicamente explicado pelo domínio raiz que encaminha para os servidores TLD's que direcionam para os servidores destinos.
- **Comandos de configuração**
    - ipconfig
    - ipconfig /flushdns -> limpar cache 
    - ping alguma.coisa -> ver se está respondendo
    - nslookup alguma.coisa -> ver se estou indo para o lugar certo
    - tracert alguma.coisa  -> quantos roteadores me conectei até achar o google
    - netstat -> mapear as portas que estão sendo utilizadas no nosso computador
- **Segurança**
    - Física ou Lógico
    - Utilizar SSo é importante para garantir que usuários façam logins com tokens diferente utilizando uma única senha.
- **Wireless**
    - Bandas e canais
    - Frequência
    - Podemos simular redes 
### 3 - Conteinerização com Docker
- **Docker**
    - Containers para isolar e otimizar aplicações e serviços, isolando-os em pequenos contextos que comunicam-se entre si.  
- **Comandos**
    - docker run -ti nginx --name nginx -p 8081:8081
    - docker ps 
    - docker -a 
    - docker build -t nomeimagem .
    - docker exec -ti 
    - docker scan
    - docker inspect 
- **Imagens**
    - Basicamente o app pronto para funcionar
- **Instruções Dockerfile**
    - FROM -> base do sistema operacional
    - WORKDIR -> acessa diretório
    - ENV -> adiciona variáveis de ambiente
    - RUN -> roda comandos em tempo de execução build/construção
    - CMD -> roda comando após o início do container, sempre
    - ENTRYPOINT -> a prioridade máxima
- **Imutabilidade**
    - o que roda na minha máquina roda em qualquer lugar
- **Volumes** 
    - Mantermos algumas informações mesmo após os containers deixarem de existir
- **Tipos de volumes**
    - Docker Volue -> monta o diretório dentro do container, pasta source
    - Docker Bind -> armazena o conteúdo, mas é limitado
    - tmpfs -> armazena temporáriamenta, bom para recursos sensíveis
- **Comunicação**
    - Contexto
- **Redes**
    - docker possui enereçamento de IP próprio
    - Bridge -> é o plugin default de rede, cria uma comunicação entre os constainers de forma que eles possam se comunicar dentro de ecossistemas isolados. Resolução DNS, em que podemos dar nomes.
    - Host -> Usa a rede do host e compartilha-a, portanto, o que for válido como rede para a máquina onde o Docker está rodando, será válido.
    - Overlay -> hosts distribuídos, comunicação segura.
- **Ecossitema**
    - --link
- **Docker Compose**
    - nos aulixia a criar stacks complets utilizando componetes como imagens, variáveis de ambiente. 
    - docker-compose up(-d) -> sobe containers
    - docker-compose logs -> verifica saúde e msgns
    - docker-compose ps -> vê se está rodando
    - docker-compose kill -> para todos os containers
    - docker-compose rm -f -> remove containers
- **Orquestradores**
    - monitoramento dos containers, um cluster
### 4 - Banco de dados
- **Tipos de dados e custo de armazenamento**
    - Neste link é possíver ver todos os tipos de dados que o POstgreSQL trabalha ``https://www.postgresql.org/docs/8.1/datatype.html``
- **Modelagem de entidades**
    - ``https://online.visual-paradigm.com/drive/#infoart:proj=0&dashboard`` -> link para modelagem de entidades
- **Normalização de dados**
    - **1ª forma normal**: Cada atibuto deve conter apenas um valor correspondente em um determinado registro.
    - **2ª forma normal**: Cada elemento da tabela deve depender apenas de sua chave primária.
    - **3ª forma normal**: Um elemento não chave da tabela não pode tepender de outro elemento não chave.
- **Exercícios**
    - Considere que você está modelando uma tabela que representa as transações de cartão de crédito processadas por um sistema de meios de pagamento. Para o campo de "horário da transação”, qual tipo de dado você deve utilizar? **datatime**
    - Considere que você está modelando uma tabela que representa as transações de cartão de crédito processadas por um sistema de meios de pagamento. Para o campo de "id”, que será chave primária da transação, qual tipo de dado é o mais adequado? **bigint** 
    - Em um banco de dados, o estado de aprovação de um pedido de reembolso é armazenado com um campo Booleano. Sobre esse tipo de dado, assinale a alternativa correta? **1 byte** 
    - Em um supermercado, uma tabela de marcas contém registros como Nestlé e Lacta, enquanto uma lista de produtos contém entradas como Nescau e Diamante negro. O relacionamento entre essas duas tabelas deve ser (considere o relacionamento de marca com produto, nesta ordem) **1 para N**
    - Em um pronto socorro, cada paciente tem um médico responsável, e cada médico atende pelo menos dez pacientes num dia. Assim sendo, assinale a alternativa correta: **A tabela de médicos se relaciona com a tabela de pacientes usando a chave estrangeira id_medico, contida na tabela de pacientes.**
- **Inserindo tabelas no banco**
    ````sql
    CREATE TABLE professores(
        id_professor integer,
        celuar varchar(14),
        nome varchar(40),
        id_disciplina integer,
        primary key (id_professor),
        foreign key (id_disciplina),
        references disciplinas(id_disciplina)
    )
    ````
- **Inserindo dados nas tabelas**
    ````sql
    INSERT INTO disciplinas VALUES
    (1, 'portugues', 'literatura e gramatica');
    ````
    ````sql
    INSERT INTO disciplinas VALUES
    (2, 'matematica', 'algebra e geometria'),
    (3, 'fisica', 'cinematica e dinamica');
    ````
- **Puxar dados para a tabela**
    ````sql
    copy disciplinas (id_disciplina, nome, ementa)
    from 'C:\disciplinas.csv'
    delimiter ','
    csv header;
    ````
- **Editando e removendo dados**
    ````sql
    updade disciplinas set nome = 'biologia'
    where id_disciplina = 7;
    ````
    ````sql
    delete from disciplinas
    where id_disciplina = 8;
    ````
- **Permissionamento ou Views**
    - Permissões de acesso de usuários
    ````sql
    create view matricula_com_sigila as
    (
        select 
            id_matricula,
            id_aluno,
            validade
        from matricula
    )
- **Índices**
    ````sql
    create index idx_nome on disciplinas(nome);
    ````
### Cloud Computing
- ****
    - 
    - 
    - 


