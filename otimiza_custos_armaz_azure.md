

Otimizar o custo de armazenamento no Azure Cosmos DB

Custo de armazenamento

Otimizar o custo com o tamanho do item
Otimizar o custo com a indexação
Otimizar o custo com tempo live e o feed de alterações
Mostrar mais 4

APLICA-SE AO:  NoSQL  MongoDB  Cassandra  Gremlin  Table

O Azure Cosmos DB oferece armazenamento ilimitado e taxa de transferência. Ao contrário de taxa de transferência,
que você precisa provisionar/configurar em seus contêineres do Azure Cosmos DB ou bancos de dados, o armazenamento é cobrado com base no consumo. 
Você será cobrado somente para o armazenamento lógico que você consumir e não precisa reservar nenhum armazenamento de antemão. O armazenamento automaticamente aumenta e diminui com base nos dados que você adicionar ou remover um contêiner do Azure Cosmos DB.


Custo de armazenamento

O armazenamento é cobrado com a unidade de GBs. Armazenamento baseado em SSD local é usado por seus dados e indexação. 
O armazenamento total usado é igual para o armazenamento necessário para os dados e os índices usados em todas as regiões em que você está usando o Azure Cosmos DB. Se você replicar globalmente uma conta do Azure Cosmos DB em três regiões, você pagará pelo custo total de armazenamento em cada uma dessas três regiões. Para estimar o requisito de armazenamento, consulte a ferramenta planejador de capacidade. O custo de armazenamento no Azure Cosmos DB é US $0,25 GB/mês, consulte a Página de preços para obter as atualizações mais recentes. Você pode configurar alertas para determinar o armazenamento usado por seu contêiner do Azure Cosmos DB para monitorar seu armazenamento, veja o artigo Monitor Azure Cosmos DB).

Otimizar o custo com o tamanho do item

O Azure Cosmos DB espera que o tamanho do item seja 2 MB ou menos para um desempenho ideal e benefícios de custo. S

e você precisar de qualquer item para armazenar mais de 2 MB de dados, considere a possibilidade de reformular o esquema de item. 

No caso raro que você não pode recriar o esquema, você pode dividir o item em subitens e vinculá-los logicamente a um identificador comum (ID).
Todos os recursos do Azure Cosmos DB funcionam de maneira consistente com ancoragem para esse identificador lógico.

Otimizar o custo com a indexação
Por padrão, os dados são automaticamente indexados, o que pode aumentar o armazenamento total consumido. 
No entanto, você pode aplicar políticas de índice personalizadas para reduzir essa sobrecarga. Indexação automática que não foi ajustada por meio da diretiva é cerca de 10 a 20% do tamanho do item. Removendo ou personalizando as políticas de índice, você não paga por gravações de custo extra e não exige a capacidade de taxa de transferência adicional. Consulte Indexar no Azure Cosmos DB para configurar políticas de indexação personalizadas. Se você tiver trabalhado com bancos de dados relacionais antes, você pode pensar que "indexar tudo" significa a duplicação de armazenamento ou superior. No entanto, no Azure Cosmos DB, no caso médio, é muito menor. No Azure Cosmos DB, a sobrecarga de armazenamento de índice é normalmente baixa (10 a 20%) mesmo com a indexação automática, porque foi projetado para um volume de armazenamento baixo. Ao gerenciar a política de indexação, você pode controlar a compensação de desempenho de consulta e o espaço de índice de uma maneira mais refinada.


Otimizar o custo com tempo live e o feed de alterações

Quando você não precisar mais dos dados, poderá excluí-los de sua conta do Azure Cosmos DB usando tempo de vida, alterar feed ou migrar os dados antigos para outro armazenamento de dados, como armazenamento de blobs do Azure ou data warehouse do Azure. Com a vida úti" ou TTL, o Azure Cosmos DB fornece a capacidade de excluir itens automaticamente de um contêiner após um determinado período de tempo. Por padrão, é possível definir a Vida Útil no nível do contêiner e substituir o valor em uma base por item. Após definir a Vida Útil em um nível de item ou contêiner, o Azure Cosmos DB removerá automaticamente esses itens após o período de tempo, desde a hora em que foram modificados pela última vez. Ao usar o feed de alterações, você pode migrar dados para qualquer outro contêiner no Azure Cosmos DB ou para um armazenamento de dados externo. A migração leva zero tempo de inatividade e quando você terminar de migrar, poderá excluir ou configurar o tempo de vida para excluir o contêiner do Azure Cosmos DB de origem.

Otimizar o custo com os tipos de dados de mídia avançada
Se você quiser armazenar tipos de mídia avançada, por exemplo, vídeos, imagens, etc., você tem várias opções no Azure Cosmos DB. 
Uma opção é armazenar esses tipos de mídia avançada como itens do Azure Cosmos DB. Há um limite de 2 MB por item e você pode evitar esse limite por meio do encadeamento do item de dados em vários subitens. Ou você pode armazená-los no armazenamento de BLOBs do Azure e usar os metadados para fazer referência a eles de seus itens do Azure Cosmos DB. Há alguns prós e contras com essa abordagem. A primeira abordagem oferece o melhor desempenho em termos de latência, SLAs de taxa de transferência e recursos de distribuição global prontos para uso para os tipos de dados de mídia avançada, além de seus itens regulares do Azure Cosmos DB. No entanto, o suporte está disponível em um preço mais alto. Ao armazenar a mídia no armazenamento de Blob do Azure, também seria possível reduzir seus custos gerais. Se a latência for crítica, você poderá usar o armazenamento premium para arquivos de mídia avançada referenciados em itens do Azure Cosmos DB. Isso se integra nativamente com a CDN para servir imagens do servidor de borda a custo menor para contornar a restrição geográfica. A desvantagem desse cenério é que você precisa lidar com dois serviços - Azure Cosmos DB e o armazenamento de Blob do Azure, que pode aumentar os custos operacionais.


Verificação do armazenamento consumido

Para verificar o consumo de armazenamento de um contêiner do Azure Cosmos DB, você pode executar uma solicitação HEAD ou GET no contêiner 

e inspecionar os cabeçalhos x-ms-request-quota e x-ms-request-usage. Como alternativa, ao trabalhar com o SDK do .NET, 
é possível usar as propriedades DocumentSizeQuota e DocumentSizeUsage para obter o armazenamento consumido.

Usando o SDK
C#

Copiar

// Measure the item size usage (which includes the index size)
ResourceResponse<DocumentCollection> collectionInfo = await client.ReadDocumentCollectionAsync(UriFactory.CreateDocumentCollectionUri("db", "coll"));   

Console.WriteLine("Item size quota: {0}, usage: {1}", collectionInfo.DocumentQuota, collectionInfo.DocumentUsage);

Próximas etapas
A seguir, você poderá saber mais sobre a otimização de custos no Azure Cosmos DB nos seguintes artigos:

Saiba mais sobre Otimizando para desenvolvimento e teste

Saiba mais sobre Entender sua cobrança do Azure Cosmos DB

Saiba mais sobre Otimizando o custo da taxa de transferência

Saiba mais sobre Otimizando o custo de leituras e gravações

Saiba mais sobre Otimizando o custo de consultas

Saiba mais sobre Otimizar o custo de contas do Azure Cosmos DB em várias regiões

Tentando fazer o planejamento da capacidade para uma migração para o Azure Cosmos DB? 

Você pode usar informações sobre o cluster de banco de dados existente para fazer isso.
Se você sabe apenas o número de vCores e servidores no cluster de banco de dados existente, 

leia sobre como estimar unidades de solicitação com vCores ou vCPUs

Se souber as taxas de solicitação típicas da carga de trabalho do banco de dados atual, 

leia sobre como estimar unidades de solicitação usando o planejador de capacidade do Azure Cosmos DB
