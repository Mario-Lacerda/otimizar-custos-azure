

Examinar os custos estimados no portal do Azure

Exiba o custo estimado por mês durante a adição de um serviço no portal do Azure. 

Por exemplo, quando você escolhe o tamanho de sua VM do Windows, vê o custo mensal estimado para as horas de computação:

Captura de tela mostrando uma VM do Windows A1 com custo estimado por mês.

Os preços mencionados são apenas para exemplificar. Eles não se destinam a implicar os custos reais.

Monitorar custos ao usar os serviços do Azure

É possível monitorar custos com as seguintes ferramentas:

Orçamento e alertas de custo

Análise de custo

Acompanhar os custos com orçamentos e alertas de custo

Crie orçamentos para gerenciar custos e crie alertas que notificam você e os stakeholders automaticamente de anomalias de gastos e gastos em excesso.

Explorar e analisar os custos com a análise de custo

Depois que os serviços do Azure estiverem em execução, verifique os custos regularmente para acompanhar seus gastos do Azure.

Use a análise de custo para entender a procedência dos custos para o uso do Azure.

Visite a página Gerenciamento de Custos + Cobrança no portal do Azure.

Selecione Análise de custo no lado esquerdo da tela para ver o custo atual dividido por vários pivôs, como serviço, localização e assinatura. Depois de adicionar um serviço ou fazer uma compra, aguarde 24 horas para que os dados sejam exibidos. Por padrão, a análise de custo mostra o custo do escopo em que você está. Por exemplo, na captura de tela abaixo, o custo da conta de cobrança da Contoso é exibido. Use o item Escopo para alterar para outro escopo na análise de custo. Para obter mais informações sobre escopos, confira Entender e trabalhar com escopos

Captura de tela do modo de exibição de análise de custo no portal do Azure.

Filtre por várias propriedades, como marcas, tipo de recurso e período de tempo. 

Selecione Adicionar filtro para adicionar o filtro de uma propriedade e selecione os valores a serem filtrados.

Selecione Exportar para exportar a exibição para um arquivo de valores separados por vírgula (.csv).

Além disso, selecione os rótulos do gráfico para ver o histórico de gastos diário para esse rótulo.

Por exemplo, na captura de tela abaixo, a seleção de uma máquina virtual exibe o custo diário de executar suas VMs.

Captura de tela da exibição do histórico de gastos no portal do Azure.

Otimizar e reduzir custos
Se você não estiver familiarizado com os princípios de gerenciamento de custos, 

leia Como otimizar seu investimento em nuvem com o Gerenciamento de Custos.

No portal do Azure, também é possível otimizar e reduzir custos do Azure com desligamento automático para VMs e recomendações do Assistente.

Considere recursos de redução de custos, como o desligamento automático para VMs

Dependendo do cenário, você pode configurar o desligamento automático para suas VMs no portal do Azure. 

Para saber mais, confira Desligamento automático de máquinas virtuais usando o Azure Resource Manager.

Captura de tela da opção de desligamento automático no portal do Azure.

O desligamento automático não é igual a desligar a VM com as opções de energia padrão. 

O desligamento automático interrompe e desaloca suas VMs para parar as cobranças adicionais. 

Para saber mais, confira os estados de VM nas Perguntas frequentes sobre preços de VMs Linux e VMs Windows.

Para obter mais recursos de redução de custos para os ambientes de desenvolvimento e teste, confira Azure DevTest Labs.

Ativar e examinar recomendações do Assistente do Azure

O Assistente do Azure ajuda a reduzir os custos identificando recursos com baixa utilização. 

Pesquise Assistente no portal do Azure:

Captura de tela do botão do Assistente do Azure no portal do Azure.

Selecione Custo no lado esquerdo. Você verá recomendações práticas na guia Custo:

Captura de tela de exemplo de recomendação de custo do Assistente.

Os preços mencionados são apenas para exemplificar. Eles não se destinam a implicar os custos reais.

Examine o tutorial Otimizar custos de recomendações para obter um tutorial guiado sobre recomendações do Assistente para economia de custos.

Evite encargos indesejados

Para evitar encargos indesejados em uma assinatura, você pode acessar o menu Recursos da assinatura e selecionar os recursos que deseja excluir. Se não quiser ter nenhum encargo para a assinatura, selecione todos os recursos de assinatura e, em seguida, Exclua-os . Essencialmente, a assinatura se torna um contêiner vazio sem encargos.

Captura de tela mostrando a exclusão das configurações.

Se você tiver um plano de suporte, poderá continuar a ser cobrado por ele. Para excluir um plano de suporte, navegue até Gerenciamento de Custos + Cobrança e selecione Encargos recorrentes. Selecione o plano de suporte e desative a renovação automática.

Captura de tela mostrando as configurações de Renovação de alteração

Integrar com APIs de gerenciamento de custos e cobrança
Use as APIs de automação cobrança e Gerenciamento de Custos do Azure para obter dados de cobrança e custo de forma programática. 

Use a API RateCard junto com a API de Uso para obter seu uso cobrado.

Casos especiais e recursos adicionais

Clientes do CSP e do Sponsorship

Fale com seu gerente de conta ou parceiro do Azure para começar.


Oferta	Recursos

Programa do CSP (Provedor de Soluções na Nuvem)	Fale com seu provedor

Azure Sponsorship	Portal do Sponsorship

Se estiver gerenciando TI em uma grande organização, recomendamos a leitura de Azure enterprise scaffold

e enterprise IT white paper (baixe o .pdf, somente em inglês).

Visualizações de custo do Contrato Enterprise no portal do Azure

As visualizações de custo Enterprise estão, no momento, em Visualização Pública. Itens a serem observados:


Os custos de assinatura são baseados no uso e não incluem valores pré-pagos, excedentes, quantidades incluídas, 

ajustes e impostos. Os encargos reais são calculados no nível de registro.

Se você não está vendo os custos, isso pode ser por um dos seguintes motivos:

Você não tem permissões no nível da assinatura. Para ver as exibições de custo empresarial, 
você precisa ser um Leitor de Cobrança, Leitor, Colaborador ou Proprietário no nível da assinatura.

Você é um Proprietário de Conta e seu Administrador de registro desabilitou a configuração “Encargos de exibição do AO”. 
Contate o Administrador de registro para obter acesso aos custos.

Você é um administrador de departamento e seu administrador de registro desabilitou a configuração Encargos de exibição do DA. 
Entre em contato com o Administrador de registro para obter acesso.

Você comprou o Azure por meio de um parceiro de canal e o parceiro não liberou informações sobre preços.

Os clientes diretos do EA podem atualizar as configurações relacionadas a custos no portal do Microsoft Azure.

Navegue até o menu Políticas para alterar as configurações.

Limite de gastos e diretrizes de fatura não se aplicam às assinaturas do Contrato Enterprise.

Verificar assinatura e acesso

Para exibir os custos, você precisa ter acesso no nível de conta ou de assinatura às informações de custo ou de cobrança. 

O acesso varia de acordo com o tipo de conta de cobrança. Para saber mais sobre contas de cobrança e verificar o tipo de sua conta de cobrança, 
confira Exibir contas de cobrança no portal do Azure.

Caso tenha acesso ao Azure por meio de uma conta de cobrança do MOSP (Programa do Microsoft Online Services), 
confira Gerenciar o acesso às informações de cobrança para o Azure.

Caso tenha acesso ao Azure por meio de uma conta de cobrança do EA (Contrato Enterprise), 
confira Entender as funções administrativas do Contrato Enterprise do Azure no Azure.

Caso tenha acesso ao Azure por meio de uma conta de cobrança do MCA (Contrato de Cliente da Microsoft), 
confira Entender as funções administrativas do Contrato de Cliente da Microsoft no Azure.

Solicitar um crédito do Contrato de Nível de Serviço para um incidente de serviço

O SLA (Contrato de Nível de Serviço) descreve os compromissos da Microsoft com relação ao tempo de atividade e à conectividade.

Um incidente de serviço é relatado quando os serviços do Azure enfrentam um problema que afeta o tempo de atividade ou a conectividade, 
geralmente denominado interrupção. Se não alcançarmos e mantivermos os Níveis de Serviço para cada serviço, conforme descrito no SLA, 
você poderá ser qualificado para um crédito para uma parte de seus valores de serviço mensais.

Para solicitar um crédito:

Entre no portal do Azure. Se você tiver várias contas, use a que foi afetada pelo tempo de inatividade do Azure. 
Em seguida, crie uma solicitação de suporte.

Em Tipo de problema, selecione Cobrança e, em Tipo de problema, selecione Solicitação de Reembolso.

Adicione detalhes para especificar que você está solicitando um crédito SLA, mencione a data/hora/fuso horário, 
além dos serviços afetados (VMs, sites etc.)

Por fim, verifique seus detalhes de contato e selecione Criar para enviar sua solicitação.

Para alguns serviços, há pré-requisitos para o SLA aplicar. Por exemplo,
as máquinas virtuais devem ter duas ou mais instâncias implantadas no mesmo conjunto de disponibilidade.

Para obter mais informações, confira Contratos de Nível de Serviço e a documentação Resumo do SLA para serviços do Azure
