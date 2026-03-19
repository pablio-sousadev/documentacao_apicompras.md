# Documentação de Endpoints – API de Compras Governamentais

## Módulo Material
O Catálogo de Materiais (CATMAT) identifica todos os materiais licitados e adquiridos pela Administração Pública Federal.

*   **1. Consultar Grupo de Material**
    *   **Descrição:** Serviço que permite consultar os dados de um grupo de material pelo código do grupo de material e/ou status do grupo.
    *   **Endpoint:** `GET /modulo-material/1_consultarGrupoMaterial`
    *   **Exemplo de Resposta:** 
    ```json
{
  "resultado": [
    {
      "codigoGrupo": 16,
      "nomeGrupo": "COMPONENTES E ACESSORIOS DE AERONAVES",
      "statusGrupo": true,
      "dataHoraAtualizacao": "2021-10-16T09:16:33.723625"
    }
  ],
  "totalRegistros": 1
}
```

*   **2. Consultar Classe de Material**
    *   **Descrição:** Serviço que permite consultar os dados de uma classe de material pelo código do grupo de material, código da classe e/ou status do grupo.
    *   **Endpoint:** `GET /modulo-material/2_consultarClasseMaterial`

*   **3. Consultar PDM (Produto Descritivo Básico)**
    *   **Descrição:** Serviço que permite consultar os dados de um Produto Descritivo Básico - PDM de material pelo código de PDM, código do grupo de material, código da classe e/ou status do PDM.
    *   **Endpoint:** `GET /modulo-material/3_consultarPdmMaterial`

*   **4. Consultar Item de Material**
    *   **Descrição:** Serviço que permite consultar os dados de um item de material pelo código do grupo de material, código da classe, código do PDM, código do item e/ou status do grupo.
    *   **Endpoint:** `GET /modulo-material/4_consultarItemMaterial`

*   **5. Consultar Natureza de Despesa do Item**
    *   **Descrição:** Serviço que permite consultar os dados de uma natureza de material pelo código do PDM e/ou código da natureza de despesa.
    *   **Endpoint:** `GET /modulo-material/5_consultarMaterialNaturezaDespesa`

*   **6. Consultar Unidade de Fornecimento**
    *   **Descrição:** Serviço que permite consultar os dados de unidade de fornecimento de material pelo código do PDM.
    *   **Endpoint:** `GET /modulo-material/6_consultarMaterialUnidadeFornecimento`

*   **7. Consultar Características de Materiais**
    *   **Descrição:** Serviço que permite consultar os dados de características de material pelo código do PDM do item.
    *   **Endpoint:** `GET /modulo-material/7_consultarMaterialCaracteristicas`

---

## Módulo Serviço
O Catálogo de Serviços (CATSER) identifica todos os serviços licitados e contratados pela Administração Pública Federal.

*   **1. Consultar Seção de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de uma seção de serviço pelo código da seção e/ou status da seção.
    *   **Endpoint:** `GET /modulo-servico/1_consultarSecaoServico`

*   **2. Consultar Divisão de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de uma divisão de serviço pelo código da seção, da divisão e/ou status da divisão.
    *   **Endpoint:** `GET /modulo-servico/2_consultarDivisaoServico`

*   **3. Consultar Grupo de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de um grupo de serviço pelo código da divisão, do grupo e/ou status do grupo.
    *   **Endpoint:** `GET /modulo-servico/3_consultarGrupoServico`

*   **4. Consultar Classe de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de uma classe de serviço pelo código do grupo, da classe e/ou status da classe.
    *   **Endpoint:** `GET /modulo-servico/4_consultarClasseServico`

*   **5. Consultar SubClasse de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de uma subclasse de serviço pelo código da classe, da subclasse e/ou status da subclasse.
    *   **Endpoint:** `GET /modulo-servico/5_consultarSubClasseServico`

*   **6. Consultar Item de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de um item de serviço pelo código da subclasse, do cpc, do serviço do e/ou status do serviço.
    *   **Endpoint:** `GET /modulo-servico/6_consultarItemServico`

*   **7. Consultar Unidade de Medida de Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de unidade de medida pelo código do serviço e/ou status da unidade e medida.
    *   **Endpoint:** `GET /modulo-servico/7_consultarUndMedidaServico`

*   **8. Consultar Natureza de Despesa do Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de natureza de despesa pelo código do serviço, da natureza de despesa e/ou status da natureza de despesa.
    *   **Endpoint:** `GET /modulo-servico/8_consultarNaturezaDespesaServico`

---

## Módulo Pesquisa de Preço
Permite acesso aos dados de itens comprados pela Administração para auxiliar os órgãos governamentais na etapa de pesquisa de preços.

*   **1. Consultar Material**
    *   **Descrição:** Serviço que permite consultar os dados de preços praticados na aquisição de materiais pelo sistema Compras.gov.br.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/1_consultarMaterial`

*   **1.1 Consultar Material (CSV)**
    *   **Descrição:** Versão do endpoint de consulta de material que retorna os dados formatados em CSV.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/1.1_consultarMaterial_CSV`

*   **2. Consultar Detalhe do Material**
    *   **Descrição:** Serviço que permite consultar os dados das descrições dos itens de materiais.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/2_consultarMaterialDetalhe`

*   **2.1 Consultar Detalhe do Material (CSV)**
    *   **Descrição:** Versão do endpoint de detalhe do material em formato CSV.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/2.1_consultarMaterialDetalhe_CSV`

*   **3. Consultar Serviço**
    *   **Descrição:** Serviço que permite consultar os dados de preços praticados na contratação de serviços pelo sistema Compras.gov.br.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/3_consultarServico`

*   **3.1 Consultar Serviço (CSV)**
    *   **Descrição:** Versão do endpoint de serviço em formato CSV.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/3.1_consultarServico_CSV`

*   **4. Consultar Detalhe do Serviço**
    *   **Descrição:** Serviço que permite consultar os dados das descrições dos itens de serviços.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/4_consultarServicoDetalhe`

*   **4.1 Consultar Detalhe do Serviço (CSV)**
    *   **Descrição:** Versão do endpoint de detalhe de serviço em formato CSV.
    *   **Endpoint:** `GET /modulo-pesquisa-preco/4.1_consultarServicoDetalhe_CSV`

---

## Módulo PGC
O Planejamento e Gerenciamento de Contratações (PGC) é a ferramenta estratégica utilizada para otimizar os processos de compras e garantir eficiência, economicidade e transparência.

*   **1. Consultar Itens do Plano de Contratação (Detalhe)**
    *   **Descrição:** Serviço que permite consultar os dados dos itens do plano de contratação de um órgão.
    *   **Endpoint:** `GET /modulo-pgc/1_consultarPgcDetalhe`

*   **1.1 Consultar Itens do Plano (CSV)**
    *   **Descrição:** Versão do endpoint de detalhe que retorna os dados formatados em CSV.
    *   **Endpoint:** `GET /modulo-pgc/1.1_consultarPgcDetalhe_CSV`

*   **2. Consultar Itens por Catálogo (CATMAT/CATSER)**
    *   **Descrição:** Serviço que permite consultar os dados de itens do planejamento da contratação por código de catmat ou catser.
    *   **Endpoint:** `GET /modulo-pgc/2_consultarPgcDetalheCatalogo`

*   **2.1 Consultar Itens por Catálogo (CSV)**
    *   **Descrição:** Versão do endpoint de catálogo em formato CSV.
    *   **Endpoint:** `GET /modulo-pgc/2.1_consultarPgcDetalheCatalogo_CSV`

*   **3. Consultar Agregação do Plano (Totais)**
    *   **Descrição:** Serviço que permite consultar os dados de quantidade total de um item e valor total planejado do plano de contratação de um órgão.
    *   **Endpoint:** `GET /modulo-pgc/3_consultarPgcAgregacao`

*   **3.1 Consultar Agregação do Plano (CSV)**
    *   **Descrição:** Versão do endpoint de agregação em formato CSV.
    *   **Endpoint:** `GET /modulo-pgc/3_consultarPgcAgregacao_CSV`

---

## Módulo UASG
A Unidade Administrativa de Serviços Gerais (UASG) representa as unidades operacionais dentro de diversos órgãos e entidades do governo federal que executam atividades de serviços gerais.

*   **1. Consultar UASG**
    *   **Descrição:** Serviço que permite consultar dados de uma Uasg.
    *   **Endpoint:** `GET /modulo-uasg/1_consultarUasg`

*   **1.1 Consultar UASG (CSV)**
    *   **Descrição:** Versão do endpoint de consulta de UASG que retorna os dados formatados em CSV.
    *   **Endpoint:** `GET /modulo-uasg/1.1_consultarUasg_CSV`

*   **2. Consultar Órgão**
    *   **Descrição:** Serviço que permite consultar os dados dos Órgãos pertencentes ao sistema Compras.gov.br.
    *   **Endpoint:** `GET /modulo-uasg/2_consultarOrgao`

*   **2.1 Consultar Órgão (CSV)**
    *   **Descrição:** Versão do endpoint de consulta de Órgão que retorna os dados formatados em CSV.
    *   **Endpoint:** `GET /modulo-uasg/2.1_consultarOrgao_CSV`

---

## Módulo Legado
Possibilita a obtenção de dados sobre licitações tradicionais do Governo Federal de acordo com a Lei 8.666/93.

*   **1. Consultar Compras com Licitação**
    *   **Descrição:** Possibilita a obtenção de dados sobre as Licitações realizadas pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/1_consultarLicitacao`

*   **1.1 Consultar Compras com Licitação por ID**
    *   **Descrição:** Busca uma licitação específica pelo seu identificador único.
    *   **Endpoint:** `GET /modulo-legado/1.1_consultarLicitacao_Id`

*   **2. Consultar Itens de Compras com Licitação**
    *   **Descrição:** Possibilita a obtenção de dados sobre os itens de licitações realizadas pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/2_consultarItemLicitacao`

*   **2.1 Consultar Itens de Licitação por ID**
    *   **Descrição:** Busca um item específico de uma licitação pelo ID da compra e do item.
    *   **Endpoint:** `GET /modulo-legado/2.1_consultarItemLicitacao_Id`

*   **3. Consultar Pregões**
    *   **Descrição:** Possibilita a obtenção de dados sobre os pregões realizados pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/3_consultarPregoes`

*   **3.1 Consultar Pregões por ID**
    *   **Descrição:** Busca um pregão específico pelo ID da compra.
    *   **Endpoint:** `GET /modulo-legado/3.1_consultarPregoes_ID`

*   **4. Consultar Itens de Pregões**
    *   **Descrição:** Possibilita a obtenção de dados sobre os itens de pregões realizados pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/4_consultarItensPregoes`

*   **4.1 Consultar Itens de Pregões por ID**
    *   **Descrição:** Busca um item de pregão pelo ID.
    *   **Endpoint:** `GET /modulo-legado/4.1_consultarItensPregoes_ID`

*   **5. Consultar Compras sem Licitação**
    *   **Descrição:** Possibilita a obtenção de dados sobre as compras sem licitação realizadas pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/5_consultarComprasSemLicitacao`

*   **5.1 Consultar Compra sem Licitação por ID**
    *   **Descrição:** Busca uma dispensa ou inexigibilidade específica pelo ID.
    *   **Endpoint:** `GET /modulo-legado/5.1_consultarCompraSemLicitacao_Id`

*   **6. Consultar Itens de Compra sem Licitação**
    *   **Descrição:** Possibilita a obtenção de dados sobre os itens de compra sem licitação realizadas pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/6_consultarCompraItensSemLicitacao`

*   **6.1 Consultar Itens de Compra sem Licitação por ID**
    *   **Descrição:** Busca um item específico de uma dispensa/inexigibilidade pelo ID.
    *   **Endpoint:** `GET /modulo-legado/6.1_consultarItensComprasSemLicitacao_Id`

*   **7. Consultar RDC (Regime Diferenciado de Contratações)**
    *   **Descrição:** Possibilita a obtenção de dados sobre licitações do tipo RDC realizadas pelo Governo Federal.
    *   **Endpoint:** `GET /modulo-legado/7_consultarRdc`

---

## Módulo Contratações (PNCP)
Acesso a informações detalhadas sobre os procedimentos de contratação dos órgãos públicos em conformidade com a nova lei de licitações (Lei nº 14.133/2021).

*   **1. Consultar Contratações (Lei 14.133/21)**
    *   **Descrição:** Serviço que permite acessar informações detalhadas sobre contratações realizadas com base na Lei 14.133/2021.
    *   **Endpoint:** `GET /modulo-contratacoes/1_consultarContratacoes_PNCP_14133`

*   **1.1 Consultar Contratações por ID (Lei 14.133/21)**
    *   **Descrição:** Busca uma contratação específica pelo seu identificador único ou número de controle do PNCP.
    *   **Endpoint:** `GET /modulo-contratacoes/1.1_consultarContratacoes_PNCP_14133_Id`

*   **2. Consultar Itens de Contratações (Lei 14.133/21)**
    *   **Descrição:** Serviço que oferece acesso aos dados específicos de itens vinculados às contratações regidas pela Lei 14.133/2021.
    *   **Endpoint:** `GET /modulo-contratacoes/2_consultarItensContratacoes_PNCP_14133`

*   **2.1 Consultar Itens de Contratações por ID**
    *   **Descrição:** Busca um item específico de uma contratação.
    *   **Endpoint:** `GET /modulo-contratacoes/2.1_consultarItensContratacoes_PNCP_14133_Id`

*   **3. Consultar Resultados dos Itens (Lei 14.133/21)**
    *   **Descrição:** Serviço que permite consultar os resultados associados aos itens contratados, incluindo detalhes de desempenho e conformidade com a Lei 14.133/2021.
    *   **Endpoint:** `GET /modulo-contratacoes/3_consultarResultadoItensContratacoes_PNCP_14133`

*   **3.1 Consultar Resultados dos Itens por ID**
    *   **Descrição:** Busca o resultado de um item específico pelo ID da compra e do item.
    *   **Endpoint:** `GET /modulo-contratacoes/3.1_consultarResultadoItensContratacoes_PNCP_14133_Id`

---

## Módulo ARP
As Atas de Registro de Preços (ARP) são documentos que estabelecem condições para futuras aquisições. Este módulo facilita o monitoramento e a gestão destas atas.

*   **1. Consultar ARP**
    *   **Descrição:** Consulta as Atas de Registro de Preços vigentes ou cadastradas, listando informações como número da ata, objeto, órgão gerenciador e período de validade.
    *   **Endpoint:** `GET /modulo-arp/1_consultarARP`

*   **1.1 Consultar ARP por ID**
    *   **Descrição:** Busca os dados detalhados de uma ARP específica utilizando seu identificador único no PNCP.
    *   **Endpoint:** `GET /modulo-arp/1.1_consultarARP_Id`

*   **1.2 Consultar ARP por Fim de Vigência**
    *   **Descrição:** Endpoint específico para filtrar ARPs com base no término de sua vigência.
    *   **Endpoint:** `GET /modulo-arp/1.2_consultarARP_FimVigencia`

*   **2. Consultar Item da ARP**
    *   **Descrição:** Retorna a lista de itens associados a uma ARP, incluindo descrição, quantidades registradas e condições de fornecimento.
    *   **Endpoint:** `GET /modulo-arp/2_consultarARPItem`

*   **2.1 Consultar Item da ARP por ID**
    *   **Descrição:** Busca os detalhes de itens de uma ARP específica pelo ID do PNCP.
    *   **Endpoint:** `GET /modulo-arp/2.1_consultarARPItem_Id`

*   **3. Consultar Unidades do Item**
    *   **Descrição:** Serviço que permite consultar os dados das unidades participantes e saldos de um item específico de uma Ata de Registro de Preços.
    *   **Endpoint:** `GET /modulo-arp/3_consultarUnidadesItem`

*   **4. Consultar Empenhos e Saldo do Item**
    *   **Descrição:** Serviço que permite consultar os saldos e quantidades empenhadas de um item em uma Ata de Registro de Preços.
    *   **Endpoint:** `GET /modulo-arp/4_consultarEmpenhosSaldoItem`

*   **5. Consultar Adesões do Item**
    *   **Descrição:** Serviço que permite consultar as adesões realizadas (caronas) a um item específico de uma Ata de Registro de Preços.
    *   **Endpoint:** `GET /modulo-arp/5_consultarAdesoesItem`

---

## Módulo Contratos
Acompanhe a execução contratual com dados sobre os contratos firmados, como objeto, valor, prazo de vigência e as partes envolvidas.

*   **1. Consultar Contratos**
    *   **Descrição:** Retorna um conjunto de contratos registrados, incluindo dados como número do contrato, objeto, vigência e órgãos participantes.
    *   **Endpoint:** `GET /modulo-contratos/1_consultarContratos`

*   **1.1 Consultar Contratos por ID**
    *   **Descrição:** Busca os dados detalhados de um contrato específico utilizando seu identificador único no PNCP.
    *   **Endpoint:** `GET /modulo-contratos/1.1_consultarContratos_Id`

*   **1.2 Consultar Contratos por Fim de Vigência**
    *   **Descrição:** Permite filtrar contratos cujo fim de vigência ocorra dentro de um intervalo de datas específico.
    *   **Endpoint:** `GET /modulo-contratos/1.2_consultarContratos_FimVigencia`

*   **2. Consultar Item de Contratos**
    *   **Descrição:** Lista ou detalha os itens vinculados a cada contrato, exibindo quantidades, valores e eventuais atualizações contratuais (aditivos, por exemplo).
    *   **Endpoint:** `GET /modulo-contratos/2_consultarContratosItem`

*   **2.1 Consultar Item de Contratos por ID**
    *   **Descrição:** Busca os itens de um contrato específico utilizando o número de controle do PNCP.
    *   **Endpoint:** `GET /modulo-contratos/2.1_consultarContratosItem_Id`

---

## Módulo Fornecedor
Reúne informações cadastrais de fornecedores que atuam com a Administração Pública, facilitando a identificação e o acompanhamento das empresas.

*   **1. Consultar Fornecedor**
    *   **Descrição:** Lista ou detalha os dados cadastrais dos fornecedores, exibindo informações como CNPJ ou CPF, razão social, localização, porte, atividade econômica (CNAE) e situação de habilitação para licitar.
    *   **Endpoint:** `GET /modulo-fornecedor/1_consultarFornecedor`

---

## Módulo OCDS (Open Contracting Data Standard)
O OCDS é um padrão global de dados abertos para contratações públicas que facilita a interoperabilidade e a análise comparativa.

*   **1. Consultar Releases**
    *   **Descrição:** Serviço que permite consultar as contratações ("releases") formatadas segundo o padrão Open Contracting Data Standard, possibilitando a extração de todo o ciclo de vida da contratação em um formato universalmente aceito.
    *   **Endpoint:** `GET /modulo-ocds/1_releases`
