# Armazenamento no Microsoft Azure

**O Armazenamento no Microsoft Azure** é uma solução de nuvem altamente escalável, segura e disponível que permite o armazenamento de grandes volumes de dados, tanto estruturados quanto não estruturados. Ele pode ser usado por empresas e desenvolvedores para armazenar e gerenciar dados de maneira confiável e econômica. A plataforma oferece diversas opções de armazenamento, com flexibilidade para atender a diferentes cenários e cargas de trabalho.

## Tipos de Armazenamento e Utilização

### 1. Blob Storage
- **Utilização**: Usado para armazenar grandes volumes de dados não estruturados, como imagens, vídeos, documentos e backups. Ideal para armazenar arquivos de mídia e dados binários. Também é amplamente utilizado para streaming de mídia e backup de arquivos.
- **Criação**:
  - No portal Azure, navegue até "Conta de Armazenamento".
  - Crie uma nova conta de armazenamento e selecione o tipo "Blob".
  - Configure opções como redundância (LRS, GRS) e nível de acesso (Hot, Cool, Archive) com base na frequência de uso dos dados.
  - Use Azure Storage Explorer, SDKs ou APIs REST para enviar e gerenciar blobs.

### 2. File Storage (Azure Files)
- **Utilização**: Oferece compartilhamento de arquivos baseado em SMB (Server Message Block) e NFS, o que permite a migração de aplicações legadas para a nuvem sem a necessidade de alterações no código. Ideal para acessar arquivos de maneira simultânea a partir de várias instâncias de máquinas virtuais.
- **Criação**:
  - No portal Azure, crie uma conta de armazenamento.
  - Selecione o serviço "Azure Files" e configure o compartilhamento de arquivos.
  - Defina permissões e quotas, e monte o compartilhamento em uma máquina virtual ou em máquinas on-premise via comandos SMB ou NFS.

### 3. Disk Storage
- **Utilização**: Usado principalmente para armazenar discos de máquinas virtuais. Existem diferentes tipos de discos (SSD, HDD) que variam em desempenho e custo, sendo usados em cargas de trabalho intensivas, como bancos de dados e aplicações empresariais.
- **Criação**:
  - Ao criar uma máquina virtual no Azure, escolha a opção de disco gerenciado.
  - Selecione o tipo de disco (Premium SSD, Standard SSD, Standard HDD) com base nas necessidades de desempenho.
  - O disco será associado automaticamente à VM. Também é possível adicionar discos adicionais conforme necessário.

### 4. Queue Storage
- **Utilização**: Utilizado para armazenar mensagens em fila para processamento assíncrono. É útil para desacoplar componentes de sistemas e assegurar que mensagens sejam processadas de forma independente, facilitando a construção de aplicações distribuídas e escaláveis.
- **Criação**:
  - Crie uma conta de armazenamento e selecione "Queue" como o serviço desejado.
  - Defina o nome da fila e use bibliotecas como o Azure SDK para inserir, ler ou excluir mensagens da fila.

### 5. Table Storage
- **Utilização**: Um banco de dados NoSQL para armazenamento de grandes volumes de dados estruturados em formato de chave-valor. Ideal para armazenar dados com necessidade de alta disponibilidade e recuperação rápida, como logs de atividades, telemetria ou metadados.
- **Criação**:
  - Crie uma conta de armazenamento e selecione "Table" como o serviço desejado.
  - Defina a tabela e use bibliotecas de clientes como Azure SDKs ou APIs REST para inserir, atualizar ou consultar dados na tabela.

## Como Criar e Configurar o Armazenamento no Azure

### 1. Criação de Conta de Armazenamento
- **Passo 1**: Acesse o portal do Azure.
- **Passo 2**: No painel de navegação à esquerda, clique em "Conta de Armazenamento" e selecione "Criar".
- **Passo 3**: Escolha a assinatura, grupo de recursos, e nomeie a conta de armazenamento.
- **Passo 4**: Selecione a localização (região onde os dados serão armazenados), o tipo de redundância (LRS, GRS) e o desempenho desejado (Standard ou Premium).
- **Passo 5**: Configure o acesso público (se necessário) e outras opções de segurança, como criptografia e firewalls.
- **Passo 6**: Conclua a criação da conta e, após isso, você poderá adicionar os tipos de armazenamento desejados (Blob, Files, Disk, Queue ou Table).

### 2. Ferramentas para Gerenciamento
- **Azure Storage Explorer**: Uma ferramenta gráfica para gerenciar e acessar seus dados no Azure Storage de forma fácil e intuitiva.
- **Azure CLI**: Ferramenta de linha de comando que pode ser usada para gerenciar contas de armazenamento e dados de forma programática.
- **SDKs e APIs REST**: Azure oferece SDKs para várias linguagens de programação (C#, Python, Java, etc.), além de APIs REST para integração com aplicações.

### 3. Segurança
- O Microsoft Azure Storage oferece suporte nativo à criptografia de dados, tanto em repouso quanto em trânsito. Você pode configurar políticas de segurança, como chave de criptografia gerenciada pelo cliente (CMK), e definir permissões granulares por meio do controle de acesso baseado em função (RBAC).

## Exemplos de Uso

- **Backup e Recuperação**: Usar Blob Storage ou File Storage para armazenar backups de longo prazo e garantir recuperação em caso de desastres.
- **Hospedagem de Aplicações Web**: Utilizar Blob Storage para hospedar arquivos estáticos, como imagens e scripts.
- **Aplicações Distribuídas**: Queue Storage para permitir comunicação assíncrona entre microserviços em uma arquitetura distribuída.
- **Big Data e Analytics**: Armazenar grandes volumes de dados não estruturados e integrá-los a ferramentas de análise de dados, como Azure Data Lake e Azure Synapse Analytics.
