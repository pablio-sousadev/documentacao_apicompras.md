# Documentação da API de Dados Abertos de Compras Governamentais

**Base URL:** `https://dadosabertos.compras.gov.br`

O Sistema Integrado de Administração de Serviços Gerais – Siasg é o sistema informatizado de apoio às atividades operacionais do Sistema de Serviços Gerais – Sisg. A API de Dados Abertos permite o acesso a informações de materiais, serviços, licitações, contratos e outros módulos essenciais.

---

# Índice da Documentação

## 📦 Módulos Principais
*   [1. Módulo Material](#módulo-material)
    *   [1. Consultar Grupo de Material](#1-consultar-grupo-de-material)
    *   [2. Consultar Classe de Material](#2-consultar-classe-de-material)
    *   [3. Consultar PDM](#3-consultar-pdm-produto-descritivo-básico)
    *   [4. Consultar Item de Material](#4-consultar-item-de-material)
    *   [5. Consultar Natureza de Despesa](#5-consultar-natureza-de-despesa-do-item)
    *   [6. Consultar Unidade de Fornecimento](#6-consultar-unidade-de-fornecimento)
    *   [7. Consultar Características](#7-consultar-características-de-materiais)

*   [2. Módulo Serviço](#módulo-serviço)
    *   [1. Consultar Seção](#1-consultar-seção-de-serviço)
    *   [2. Consultar Divisão](#2-consultar-divisão-de-serviço)
    *   [3. Consultar Grupo](#3-consultar-grupo-de-serviço)
    *   [4. Consultar Classe](#4-consultar-classe-de-serviço)
    *   [5. Consultar SubClasse](#5-consultar-subclasse-de-serviço)
    *   [6. Consultar Item](#6-consultar-item-de-serviço)

*   [3. Módulo Pesquisa de Preço](#módulo-pesquisa-de-preço)
    *   [1. Consultar Material](#1-consultar-material)
    *   [2. Consultar Detalhe do Material](#2-consultar-detalhe-do-material)
    *   [3. Consultar Serviço](#3-consultar-serviço)
    *   [4. Consultar Detalhe do Serviço](#4-consultar-detalhe-do-serviço)

*   [4. Módulo PGC](#módulo-pgc)
    *   [1. Consultar Itens do Plano (Detalhe)](#1-consultar-itens-do-plano-de-contratação-detalhe)
    *   [2. Consultar Itens por Catálogo](#2-consultar-itens-por-catálogo-catmatcatser)
    *   [3. Consultar Agregação (Totais)](#3-consultar-agregação-do-plano-totais)

*   [5. Módulo UASG](#módulo-uasg)
    *   [1. Consultar UASG](#1-consultar-uasg)
    *   [2. Consultar Órgão](#2-consultar-órgão)

*   [6. Módulo Legado](#módulo-legado)
    *   [1. Consultar Compras com Licitação](#1-consultar-compras-com-licitação)
    *   [2. Consultar Itens de Compras](#2-consultar-itens-de-compras-com-licitação)
    *   [3. Consultar Pregões](#3-consultar-pregões)
    *   [4. Consultar Itens de Pregões](#4-consultar-itens-de-pregões)
    *   [5. Consultar Compras sem Licitação](#5-consultar-compras-sem-licitação)
    *   [6. Consultar Itens sem Licitação](#6-consultar-itens-de-compra-sem-licitação)
    *   [7. Consultar RDC](#7-consultar-rdc-regime-diferenciado-de-contratações)

*   [7. Módulo Contratações (PNCP)](#módulo-contratações-pncp)
    *   [1. Consultar Contratações](#1-consultar-contratações-lei-1413321)
    *   [1.1 Consultar por ID](#11-consultar-contratações-por-id-lei-1413321)
    *   [2. Consultar Itens](#2-consultar-itens-de-contratações-lei-1413321)
    *   [3. Consultar Resultados](#3-consultar-resultados-dos-itens-lei-1413321)

*   [8. Módulo ARP](#módulo-arp)
    *   [1. Consultar ARP](#1-consultar-arp)
    *   [1.2 Consultar ARP por Fim de Vigência](#12-consultar-arp-por-fim-de-vigência)
    *   [2. Consultar Item da ARP](#2-consultar-item-da-arp)
    *   [3. Consultar Unidades do Item](#3-consultar-unidades-do-item)
    *   [4. Consultar Empenhos e Saldo](#4-consultar-empenhos-e-saldo-do-item)
    *   [5. Consultar Adesões](#5-consultar-adesões-do-item)

*   [9. Módulo Contratos](#módulo-contratos)
    *   [1. Consultar Contratos](#1-consultar-contratos)
    *   [1.1 Consultar Contratos por ID](#11-consultar-contratos-por-id)
    *   [1.2 Consultar Contratos por Fim de Vigência](#12-consultar-contratos-por-fim-de-vigência)
    *   [2. Consultar Item de Contratos](#2-consultar-item-de-contratos)

*   [10. Módulo Fornecedor](#módulo-fornecedor)
    *   [1. Consultar Fornecedor](#1-consultar-fornecedor)

*   [11. Módulo OCDS](#módulo-ocds)
    *   [1. Consultar Releases](#1-consultar-releases)

---

# Módulo Material

Este módulo reúne os serviços de consulta ao Catálogo de Materiais (CATMAT), permitindo o acesso a grupos, classes, PDMs (Padrão Descritivo de Materiais) e itens específicos.

### 1. Consultar Grupo de Material
Retorna dados de um grupo de material pelo código e/ou status.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/1_consultarGrupoMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `codigoGrupo` | Inteiro | Não | Código do grupo do material. |
| `statusGrupo` | Booleano | Não | Status do grupo. 0 - False/Inativo 1 - True/Ativo. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/1_consultarGrupoMaterial?codigoGrupo=16`

**Resposta:**
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
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 2. Consultar Classe de Material
Consulta dados de uma classe de material pelo código do grupo, código da classe e/ou status.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/2_consultarClasseMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `codigoGrupo` | Inteiro | Não | Código do grupo do material. |
| `codigoClasse` | Inteiro | Não | Código da classe do material. |
| `statusClasse` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |
| `bps` | Booleano | Não | Indica se a compra segue as Boas Práticas de Suprimentos. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/2_consultarClasseMaterial?codigoClasse=1615`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoGrupo": 16,
 "nomeGrupo": "COMPONENTES E ACESSORIOS DE AERONAVES",
 "codigoClasse": 1615,
 "nomeClasse": "PÁS DE ROTOR DE HELICOPTERO, MECANISMOS DE TRANSMISSÃO E COMPONENTES",
 "statusClasse": true,
 "dataHoraAtualizacao": "2021-10-16T09:17:13.045775"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 3. Consultar PDM (Produto Descritivo Básico)
Consulta dados de um PDM pelo código, grupo, classe e/ou status.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/3_consultarPdmMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `statusPdm` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |
| `codigoPdm` | Inteiro | Não | Código do PDM. |
| `codigoGrupo` | Inteiro | Não | Código do grupo. |
| `codigoClasse` | Inteiro | Não | Código da classe. |
| `bps` | Booleano | Não | Indica se segue as Boas Práticas de Suprimentos. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/3_consultarPdmMaterial?statusPdm=1&codigoPdm=10468`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoGrupo": 16,
 "nomeGrupo": "COMPONENTES E ACESSORIOS DE AERONAVES",
 "codigoClasse": 1615,
 "nomeClasse": "PÁS DE ROTOR DE HELICOPTERO...",
 "codigoPdm": 10468,
 "nomePdm": "PAS DE ROTORES DE ACIONAMENTO DE HELICOPTEROS",
 "statusPdm": true,
 "dataHoraAtualizacao": "2021-10-16T09:21:41.961529"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 4. Consultar Item de Material
Consulta dados detalhados de um item de material específico.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/4_consultarItemMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite máx. de 500 registros por página. |
| `codigoItem` | Inteiro | Não | Código do item do material. |
| `codigoGrupo` | Inteiro | Não | Código do grupo. |
| `codigoClasse` | Inteiro | Não | Código da classe. |
| `codigoPdm` | Inteiro | Não | Código do PDM. |
| `descricaoItem` | Texto | Não | Descrição do item. |
| `statusItem` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |
| `codigo_ncm` | Texto | Não | Código NCM. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/4_consultarItemMaterial?codigoItem=46736`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoGrupo": 0,
 "nomeGrupo": "string",
 "codigoClasse": 0,
 "nomeClasse": "string",
 "codigoPdm": 0,
 "nomePdm": "string",
 "codigoItem": 46736,
 "descricaoItem": "string",
 "statusItem": true,
 "itemSustentavel": true,
 "codigo_ncm": "string",
 "descricao_ncm": "string",
 "aplica_margem_preferencia": true,
 "dataHoraAtualizacao": "2025-05-07T17:49:19.424Z"
 }
 ],
 "totalRegistros": 0,
 "totalPaginas": 0,
 "paginasRestantes": 0
}
```

---

### 5. Consultar Natureza de Despesa do Item
Consulta a relação entre materiais e naturezas de despesa.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/5_consultarMaterialNaturezaDespesa`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoPdm` | Inteiro | Não | Código do PDM. |
| `codigoNaturezaDespesa` | Texto | Não | Código da natureza de despesa. |
| `statusNaturezaDespesa` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/5_consultarMaterialNaturezaDespesa?codigoNaturezaDespesa=33903016`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoPdm": 6,
 "codigoNaturezaDespesa": "33903016",
 "nomeNaturezaDespesa": "MATERIAL DE CONSUMO - MATERIAL DE EXPEDIENTE",
 "statusNaturezaDespesa": true
 }
 ],
 "totalRegistros": 69,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 6. Consultar Unidade de Fornecimento
Consulta as unidades de fornecimento válidas para um PDM.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/6_consultarMaterialUnidadeFornecimento`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoPdm` | Inteiro | Não | Código do PDM. |
| `statusUnidadeFornecimentoPdm` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |

**Exemplo de Requisição:**

**URL:** `{{baseUrl}}/modulo-material/6_consultarMaterialUnidadeFornecimento?codigoPdm=11&statusUnidadeFornecimentoPdm=True`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoPdm": 11,
 "siglaUnidadeFornecimento": "KG",
 "nomeUnidadeFornecimento": "QUILOGRAMA",
 "descricaoUnidadeFornecimento": "UNIDADE DE MEDIDA DE PESO EQUIVALENTE A 1000 GRAMAS.",
 "siglaUnidadeMedida": null,
 "capacidadeUnidadeFornecimento": 0,
 "numeroSequencialUnidadeFornecimento": 13,
 "statusUnidadeFornecimentoPdm": true,
 "dataHoraAtualizacao": "2021-10-16T09:30:54.651407"
 }
 ],
 "totalRegistros": 18,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 7. Consultar Características de Materiais
Retorna as características técnicas associadas a um item de material.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/7_consultarMaterialCaracteristicas`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoItem` | Inteiro | Não | Código do item do material. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/7_consultarMaterialCaracteristicas?codigoItem=46736`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoItem": 46736,
 "itemSustentavel": false,
 "statusItem": true,
 "codigoCaracteristica": "AAYZ",
 "nomeCaracteristica": "NOME",
 "statusCaracteristica": true,
 "codigoValorCaracteristica": null,
 "nomeValorCaracteristica": "PAS DE ROTORES DE ACIONAMENTO DE HELICOP",
 "statusValorCaracteristica": null,
 "numeroCaracteristica": 1,
 "siglaUnidadeMedida": null,
 "dataHoraAtualizacao": "2021-10-16T09:43:08.030221"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

***

# Módulo Serviço

Este módulo permite a consulta detalhada ao Catálogo de Serviços (CATSER) do Governo Federal, possibilitando navegar pela estrutura hierárquica desde a seção até o item de serviço específico, incluindo naturezas de despesa e unidades de medida.

### 1. Consultar Seção de Serviço
Retorna dados de uma seção de serviço pelo código e/ou status.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/1_consultarSecaoServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `codigoSecao` | Inteiro | Não | Código da seção do serviço. |
| `statusSecao` | Booleano | Não | Indica se a seção está ativa (true) ou inativa (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/1_consultarSecaoServico?codigoSecao=5`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoSecao": 5,
 "nomeSecao": "SERVIÇO DE CONSTRUÇÃO",
 "statusSecao": true,
 "dataHoraAtualizacao": "2021-10-16T09:04:05.777056"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 2. Consultar Divisão de Serviço
Consulta dados de uma divisão de serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/2_consultarDivisaoServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoSecao` | Inteiro | Não | Código de seção do serviço. |
| `codigoDivisao` | Inteiro | Não | Código de divisão do serviço. |
| `statusDivisao` | Booleano | Não | Indica se a divisão está ativa (true) ou inativa (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/2_consultarDivisaoServico?codigoDivisao=54`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoSecao": 5,
 "nomeSecao": "SERVIÇO DE CONSTRUÇÃO",
 "codigoDivisao": 54,
 "nomeDivisao": "SERVIÇO DE CONSTRUÇÃO",
 "statusDivisao": true,
 "dataHoraAtualizacao": "2021-10-16T09:05:08.8001"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 3. Consultar Grupo de Serviço
Consulta dados de um grupo de serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/3_consultarGrupoServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoDivisao` | Inteiro | Não | Código de divisão do serviço. |
| `codigoGrupo` | Inteiro | Não | Código de grupo do serviço. |
| `statusGrupo` | Booleano | Não | Indica se o grupo está ativo (true) ou inativo (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/3_consultarGrupoServico?codigoGrupo=541`

**Resposta:**
```json
{
 "resultado": [
 {
 "nomeSecao": null,
 "codigoDivisao": 54,
 "nomeDivisao": "SERVIÇO DE CONSTRUÇÃO",
 "codigoGrupo": 541,
 "nomeGrupo": "SERVIÇOS GERAIS DE CONSTRUÇÃO DOS EDIFÍCIOS",
 "statusGrupo": true,
 "dataHoraAtualizacao": "2021-10-16T09:07:04.535092"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 4. Consultar Classe de Serviço
Consulta dados de uma classe de serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/4_consultarClasseServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoGrupo` | Inteiro | Não | Código de grupo do serviço. |
| `codigoClasse` | Inteiro | Não | Código de classe do serviço. |
| `statusGrupo` | Booleano | Não | Indica se o grupo está ativo (true) ou inativo (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/4_consultarClasseServico?codigoClasse=5411`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoGrupo": 541,
 "nomeGrupo": "SERVIÇOS GERAIS DE CONSTRUÇÃO DOS EDIFÍCIOS",
 "codigoClasse": 5411,
 "nomeClasse": "SERVIÇOS GERAIS DE CONSTRUÇÃO DOS EDIFÍCIOS RESIDÊNCIAIS",
 "statusGrupo": true,
 "dataHoraAtualizacao": "2021-10-16T09:07:45.670793"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 5. Consultar SubClasse de Serviço
Consulta dados de uma subclasse de serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/5_consultarSubClasseServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoClasse` | Inteiro | Não | Código de classe do serviço. |
| `codigoSubclasse` | Inteiro | Não | Código de subclasse do serviço. |
| `statusSubclasse` | Booleano | Não | Indica se a subclasse está ativa (true) ou inativa (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/5_consultarSubClasseServico?codigoSubclasse=54111`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoClasse": 5411,
 "nomeClasse": "SERVIÇOS GERAIS DE CONSTRUÇÃO DOS EDIFÍCIOS RESIDÊNCIAIS",
 "codigoSubclasse": 54111,
 "nomeSubclasse": "SERVIÇOS GERAIS DE CONSTRUÇÃO DOS EDIFÍCIOS DE UMA OU DUAS MORADIAS",
 "statusSubclasse": true,
 "dataHoraAtualizacao": "2021-10-16T09:08:14.379916"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 6. Consultar Item de Serviço
Consulta dados de um item de serviço específico, permitindo filtragem por toda a hierarquia ou CPC.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/6_consultarItemServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite máx. de 500 registros por página (Padrão: 10). |
| `codigoSecao` | Inteiro | Não | Código de seção do serviço. |
| `codigoDivisao` | Inteiro | Não | Código de divisão do serviço. |
| `codigoGrupo` | Inteiro | Não | Código de grupo do serviço. |
| `codigoClasse` | Inteiro | Não | Código de classe do serviço. |
| `codigoSubclasse` | Inteiro | Não | Código de subclasse do serviço. |
| `codigoCpc` | Inteiro | Não | Código de CPC. |
| `codigoServico` | Inteiro | Não | Código de serviço. |
| `exclusivoCentralCompras` | Booleano | Não | 0 - False; 1 - True. |
| `statusServico` | Booleano | Não | Indica se o serviço está ativo (true) ou inativo (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/6_consultarItemServico?codigoServico=1627`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoSecao": 5,
 "nomeSecao": "SERVIÇO DE CONSTRUÇÃO",
 "codigoDivisao": 54,
 "nomeDivisao": "SERVIÇO DE CONSTRUÇÃO",
 "codigoGrupo": 545,
 "nomeGrupo": "TIPOS ESPECIAIS DE SERVIÇOS DE CONSTRUÇÃO",
 "codigoClasse": null,
 "nomeClasse": null,
 "codigoSubclasse": null,
 "nomeSubclasse": null,
 "codigoServico": 1627,
 "nomeServico": "MANUTENCAO / REFORMA PREDIAL",
 "codigoCpc": 545,
 "exclusivoCentralCompras": false,
 "statusServico": true,
 "dataHoraAtualizacao": "2021-10-16T09:09:59.689615"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 7. Consultar Unidade de Medida de Serviço
Consulta as unidades de medida associadas a um serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/7_consultarUndMedidaServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoServico` | Inteiro | Não | Código de serviço. |
| `statusUnidadeMedida` | Booleano | Não | Indica se a unidade de medida está ativa (true) ou inativa (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/7_consultarUndMedidaServico?codigoServico=19`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoServico": 19,
 "siglaUnidadeMedida": "UN",
 "nomeUnidadeMedida": "UNIDADE",
 "statusUnidadeMedida": true
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 8. Consultar Natureza de Despesa do Serviço
Consulta a relação entre serviços e naturezas de despesa.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-servico/8_consultarNaturezaDespesaServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoServico` | Inteiro | Não | Código de serviço. |
| `codigoNaturezaDespesa` | Texto | Não | Código da natureza de despesa do serviço. |
| `statusNaturezaDespesa` | Booleano | Não | Indica se a natureza de despesa está ativa (true) ou inativa (false). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/8_consultarNaturezaDespesaServico?codigoNaturezaDespesa=33903905`

**Resposta:**
```json
{
 "resultado": [
 {
 "codigoServico": 19,
 "codigoNaturezaDespesa": "33903905",
 "nomeNaturezaDespesa": "OUTROS SERVICOS DE TERCEIROS - PESSOA JURIDICA - SERVICOS TECNICOS PROFISSIONAIS",
 "statusNaturezaDespesa": true
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

***

# Módulo Pesquisa de Preço

Este módulo permite consultar dados de preços praticados na aquisição de materiais e contratação de serviços pelo Governo Federal, servindo como insumo para a formação de preços de referência.

### 1. Consultar Material
Consulta os preços praticados na aquisição de um item de material específico.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/1_consultarMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `codigoItemCatalogo` | Inteiro | **Sim** | Código do item do material (CATMAT). |
| `codigoUasg` | Inteiro | Não | Código da UASG. |
| `estado` | Texto | Não | Sigla da UF. |
| `codigoMunicipio` | Inteiro | Não | Código do município (IBGE). |
| `dataResultado` | Texto | Não | Filtro por data do resultado. |
| `codigoClasse` | Inteiro | Não | Código da classe do material. |

**Exemplo de Resposta:**
```json
{
  "resultado": [
    {
      "idCompra": "79101006003642023",
      "idItemCompra": 2527019,
      "forma": "SISPP",
      "modalidade": 6,
      "criterioJulgamento": " ",
      "numeroItemCompra": 1,
      "descricaoItem": "CABO ELÉTRICO ISOLADO...",
      "codigoItemCatalogo": 470419,
      "nomeUnidadeMedida": null,
      "siglaUnidadeFornecimento": "M",
      "quantidade": 1,
      "precoUnitario": 451.98,
      "niFornecedor": "30814518000120",
      "nomeFornecedor": "MANHUACU CONSTRUCAO...",
      "marca": "CABO PP",
      "codigoUasg": "795500",
      "nomeUasg": "BASE DE FUZILEIROS NAVAIS DO RIO MERITI",
      "estado": "RJ",
      "dataCompra": "2023-03-29T03:00:00.000+00:00"
    }
  ],
  "totalRegistros": 1,
  "totalPaginas": 1
}
```

---

### 1.1 Consultar Material (CSV)
Versão do endpoint acima que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/1.1_consultarMaterial_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarMaterial`.

---

### 2. Consultar Detalhe do Material
Retorna a descrição detalhada do objeto da compra e do item de material.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/2_consultarMaterialDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `idCompra` | Texto | **Sim** | Código identificador da compra. |
| `codigoItemCatalogo` | Inteiro | Não | Código do item do material. |

**Exemplo de Resposta:**
```json
{
  "resultado": [
    {
      "idCompra": "98108305000252023",
      "idItemCompra": 3845064,
      "numeroItemCompra": 1,
      "codigoItemCatalogo": 446573,
      "objetoCompra": "Objeto: Pregão Eletrônico - É o REGISTRO DE PRECOS...",
      "descricaoDetalhadaItem": "ACESSÓRIOS / EQUIPAMENTOS OFICINA MANUTENÇÃO..."
    }
  ],
  "totalRegistros": 1,
  "totalPaginas": 1
}
```

---

### 2.1 Consultar Detalhe do Material (CSV)
Versão do endpoint de detalhe em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/2.1_consultarMaterialDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarMaterialDetalhe`.

---

### 3. Consultar Serviço
Consulta os preços praticados na contratação de um item de serviço específico.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/3_consultarServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoItemCatalogo` | Inteiro | **Sim** | Código do item do serviço (CATSER). |
| `codigoUasg` | Inteiro | Não | Código da UASG. |
| `estado` | Texto | Não | Sigla da UF. |
| `codigoMunicipio` | Inteiro | Não | Código do município. |
| `dataResultado` | Texto | Não | Filtro por data do resultado. |

**Exemplo de Resposta:**
```json
{
  "resultado": [
    {
      "idCompra": "15306306001502023",
      "idItemCompra": 2477001,
      "forma": "SISPP",
      "modalidade": 6,
      "numeroItemCompra": 4,
      "descricaoItem": "MANUTENCAO / REFORMA PREDIAL",
      "codigoItemCatalogo": 1627,
      "nomeUnidadeMedida": "UNIDADE",
      "quantidade": 1,
      "precoUnitario": 2365.6,
      "nomeFornecedor": "JVV ENGENHARIA SERVICOS E COMERCIO LTDA",
      "nomeUasg": "UNIVERSIDADE FEDERAL DO PARA/PA",
      "estado": "PA",
      "dataCompra": "2023-03-22T03:00:00.000+00:00"
    }
  ],
  "totalRegistros": 31451,
  "totalPaginas": 63
}
```

---

### 3.1 Consultar Serviço (CSV)
Versão do endpoint de serviço em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/3.1_consultarServico_CSV`

**Parâmetros:** Os mesmos do endpoint `3_consultarServico`.

---

### 4. Consultar Detalhe do Serviço
Retorna a descrição detalhada do objeto da compra e do item de serviço.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/4_consultarServicoDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `idCompra` | Texto | **Sim** | Código identificador da compra. |
| `codigoItemCatalogo` | Inteiro | Não | Código do item do serviço. |

**Exemplo de Resposta:**
```json
{
  "resultado": [
    {
      "idCompra": "7001905000472023",
      "idItemCompra": 4182566,
      "numeroItemCompra": 1,
      "codigoItemCatalogo": 1627,
      "objetoCompra": "Objeto: Pregão Eletrônico - Prestação de serviços de manutenções prediais...",
      "descricaoDetalhadaItem": "Prestação de serviços de manutenções prediais preventivas e corretivas..."
    }
  ],
  "totalRegistros": 1,
  "totalPaginas": 1
}
```

---

### 4.1 Consultar Detalhe do Serviço (CSV)
Versão do endpoint de detalhe de serviço em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/4.1_consultarServicoDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `4_consultarServicoDetalhe`.

---

# Módulo PGC

O PGC (Sistema de Planejamento e Gerenciamento de Contratações) é a ferramenta utilizada para elaborar o Plano de Contratações Anual. Este módulo da API permite consultar os itens planejados, servindo como base para o mercado se preparar para as futuras licitações do governo.

### 1. Consultar Itens do Plano de Contratação (Detalhe)
Consulta os itens detalhados do planejamento de contratação de um órgão específico para um determinado ano.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/1_consultarPgcDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `orgao` | Texto | **Sim** | CNPJ do Órgão (sem pontuação). |
| `anoPcaProjetoCompra` | Inteiro | **Sim** | Ano do projeto/plano (ex: 2022). |
| `codigoUasg` | Inteiro | Não | Código da UASG da contratação. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoUasg": "540004",
 "nomeUasg": "COORDENAÇÃO-GERAL DE RECURSOS LOGÍSTICOS",
 "orgao": "05457283000119",
 "numeroArtefato": 30,
 "anoArtefato": 2021,
 "descricaoObjetoDfd": "Adquirir microcomputadores",
 "tipoItem": "M",
 "codigoItemCatalogo": "453965",
 "descricaoItemCatalogo": "MICROCOMPUTADOR, MEMÓRIA RAM: SUPERIOR A 8 GB...",
 "quantidadeItem": 25,
 "valorUnitarioItem": 7200,
 "valorTotalItem": 180000,
 "anoPcaProjetoCompra": 2022,
 "dataHoraPublicacaoPncp": "2023-05-20T05:20:57.248023"
 }
 ],
 "totalRegistros": 143,
 "totalPaginas": 15,
 "paginasRestantes": 14
}
```

---

### 1.1 Consultar Itens do Plano (CSV)
Versão do endpoint de detalhe que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/1.1_consultarPgcDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarPgcDetalhe`.

---

### 2. Consultar Itens por Catálogo (CATMAT/CATSER)
Permite consultar quem está planejando comprar um determinado material (Classe) ou serviço (Grupo), útil para fornecedores encontrarem oportunidades por tipo de produto.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/2_consultarPgcDetalheCatalogo`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `anoPcaProjetoCompra` | Inteiro | **Sim** | Ano do projeto. |
| `tipo` | Texto | **Sim** | Tipo do item: `Material` ou `Servico`. |
| `codigo` | Inteiro | **Sim** | Código da Classe (se Material) ou Grupo (se Serviço). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoUasg": "110001",
 "nomeUasg": "SECRETARIA DE ADMINISTRAÇÃO",
 "orgao": "00394411000109",
 "descricaoObjetoDfd": "MICROCOMPUTADOR, MEMÓRIA RAM SUPERIOR A 8...",
 "tipoItem": "M",
 "codigoClasseMaterial": 7010,
 "nomeClasseMaterial": "COMPUTADORES",
 "codigoPdmMaterial": 6661,
 "nomePdmMaterial": "MICROCOMPUTADOR",
 "quantidadeItem": 1065,
 "valorTotalItem": 7455000,
 "tituloProjetoCompra": "Aquisição computadores",
 "dataPrevistaFormalizacaoDemanda": "2022-06-01T00:00:00"
 }
 ],
 "totalRegistros": 3821,
 "totalPaginas": 383,
 "paginasRestantes": 382
}
```

---

### 2.1 Consultar Itens por Catálogo (CSV)
Versão do endpoint de catálogo em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/2.1_consultarPgcDetalheCatalogo_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarPgcDetalheCatalogo`.

---

### 3. Consultar Agregação do Plano (Totais)
Retorna os totais consolidados (quantidade de itens e valor total estimado) do plano de um órgão.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/3_consultarPgcAgregacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `orgao` | Texto | **Sim** | CNPJ do Órgão (sem pontuação). |
| `ano` | Inteiro | **Sim** | Ano do plano (YYYY). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "orgao": "05457283000119",
 "ano": 2022,
 "poder": "E",
 "esfera": "F",
 "dataHoraPublicacaoPncp": "2023-05-20T05:21:14.511956",
 "quantidadeTotalItens": 230,
 "valorTotalEstimado": 219821084.64
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1
}
```

---

### 3.1 Consultar Agregação do Plano (CSV)
Versão do endpoint de agregação em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/3_consultarPgcAgregacao_CSV`

**Parâmetros:** Os mesmos do endpoint `3_consultarPgcAgregacao`.

***

# Módulo UASG

UASG é a sigla para Unidade Administrativa de Serviços Gerais, uma denominação utilizada no contexto do SISG (Sistema Integrado de Serviços Gerais). As UASGs são unidades operacionais dentro de diversos órgãos e entidades do governo federal que executam atividades de serviços gerais, como contratações e aquisições.

### 1. Consultar UASG
Serviço que permite consultar dados detalhados de uma UASG, incluindo sua vinculação a órgãos superiores e localização.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/1_consultarUasg`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `codigoUasg` | Texto | Não | Código da UASG (Unidade Administrativa). |
| `usoSisg` | Booleano | Não | Filtra se o órgão utiliza o SISG (0 - False / 1 - True). |
| `cnpjCpfOrgao` | Texto | Não | CNPJ do órgão (sem máscara). |
| `cnpjCpfOrgaoVinculado` | Texto | Não | CNPJ do órgão vinculado (sem máscara). |
| `cnpjCpfOrgaoSuperior` | Texto | Não | CNPJ do órgão superior (sem máscara). |
| `siglaUf` | Texto | Não | Sigla da Unidade Federativa (UF). |
| `statusUasg` | Booleano | **Sim** | Status da UASG. 0 - Inativo / 1 - Ativo. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoUasg": "200014",
 "nomeUasg": "PR-ARQUIVO NACIONAL-RJ",
 "usoSisg": true,
 "adesaoSiasg": true,
 "siglaUf": "RJ",
 "codigoMunicipio": 60011,
 "codigoMunicipioIbge": 3304557,
 "nomeMunicipioIbge": "RIO DE JANEIRO",
 "codigoUnidadePolo": 0,
 "nomeUnidadePolo": null,
 "codigoUnidadeEspelho": 0,
 "nomeUnidadeEspelho": null,
 "uasgCadastradora": true,
 "cnpjCpfUasg": "394494001299",
 "codigoOrgao": 20101,
 "cnpjCpfOrgao": "00394411000109",
 "cnpjCpfOrgaoVinculado": "00394411000109",
 "cnpjCpfOrgaoSuperior": null,
 "codigoSiorg": "334",
 "statusUasg": true,
 "dataImplantacaoSidec": "1999-07-15T03:00:00.000+00:00",
 "dataHoraMovimento": "2023-07-06T14:14:00"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 1.1 Consultar UASG (CSV)
Versão do endpoint de consulta de UASG que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/1.1_consultarUasg_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarUasg`.

---

### 2. Consultar Órgão
Serviço que permite consultar os dados dos Órgãos pertencentes ao sistema Compras.gov.br, identificando sua estrutura hierárquica (vinculado/superior) e esfera administrativa.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/2_consultarOrgao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `cnpjCpfOrgao` | Texto | Não | CNPJ do órgão (sem máscara). |
| `cnpjCpfOrgaoVinculado` | Texto | Não | CNPJ do órgão vinculado. |
| `cnpjCpfOrgaoSuperior` | Texto | Não | CNPJ do órgão superior. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `statusOrgao` | Booleano | **Sim** | Status do órgão. 0 - Inativo / 1 - Ativo. |
| `usoSisg` | Booleano | Não | Filtra se o órgão utiliza o SISG. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoOrgao": 26000,
 "nomeOrgao": "MINISTERIO DA EDUCACAO",
 "nomeMnemonicoOrgao": "MIN.EDUCACAO",
 "cnpjCpfOrgao": "00394445000101",
 "codigoOrgaoVinculado": 20101,
 "cnpjCpfOrgaoVinculado": "00394411000109",
 "nomeOrgaoVinculado": "PRESIDENCIA DA REPUBLICA",
 "codigoOrgaoSuperior": 20000,
 "cnpjCpfOrgaoSuperior": "00394411000109",
 "nomeOrgaoSuperior": "PRESIDENCIA DA REPUBLICA - PRES",
 "codigoTipoAdministracao": 1,
 "nomeTipoAdministracao": "ADMINISTRACAO DIRETA",
 "poder": "E",
 "esfera": "F",
 "usoSisg": true,
 "statusOrgao": true,
 "dataHoraMovimento": "2023-07-06T09:12:00"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

---

### 2.1 Consultar Órgão (CSV)
Versão do endpoint de consulta de Órgão que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/2.1_consultarOrgao_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarOrgao`.

***

# Módulo Legado

Este módulo possibilita a obtenção de dados sobre as licitações realizadas pelo Governo Federal (compras tradicionais, pregões e RDC). Embora denominado "Legado", ele é fundamental para a transparência histórica e para processos de transição.

### 1. Consultar Compras com Licitação
Retorna dados gerais sobre licitações (exceto pregões).

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/1_consultarLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `uasg` | Inteiro | Não | Código da UASG. |
| `numero_aviso` | Inteiro | Não | Número da licitação. |
| `modalidade` | Inteiro | Não | Código da modalidade de licitação. |
| `data_publicacao_inicial` | Texto | **Sim** | Data início da publicação. |
| `data_publicacao_final` | Texto | **Sim** | Data final da publicação (limitado a 365 dias). |
| `pertence14133` | Booleano | Não | Indica se a licitação pertence à Lei nº 14.133/2021. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "id_compra": "12063205000942023",
 "identificador": "12063205942023",
 "numero_processo": "67437002017202347",
 "uasg": 120632,
 "modalidade": 5,
 "nome_modalidade": "PREGÃO",
 "numero_aviso": 942023,
 "situacao_aviso": "Publicado",
 "tipo_pregao": "eletronico",
 "tipo_recurso": "Nacional",
 "objeto": "Pregão Eletrônico Registro de Preços para aquisição de medicamentos...",
 "data_publicacao": "2023-12-11",
 "pertence14133": true
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1
}
```

---

### 1.1 Consultar Compras com Licitação por ID
Busca uma licitação específica pelo seu identificador único.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/1.1_consultarLicitacao_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `id_compra` | Texto | **Sim** | Código da compra (ex.: 15322905000942023). |
| `dt_alteracao` | Texto | Não | Filtro por data de alteração. |

---

### 2. Consultar Itens de Compras com Licitação
Retorna os itens pertencentes a uma licitação específica.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/2_consultarItemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `uasg` | Inteiro | Não | Código da UASG. |
| `numero_aviso` | Inteiro | Não | Número do aviso. |
| `modalidade` | Inteiro | **Sim** | Código da modalidade de licitação. |
| `decreto_7174` | Booleano | Não | Filtro para itens vinculados ao Decreto nº 7.174/2010. |
| `codigo_item_material` | Inteiro | Não | Código do item (Material). |
| `codigo_item_servico` | Inteiro | Não | Código do item (Serviço). |
| `cnpj_fornecedor` | Texto | Não | CNPJ do vencedor. |
| `cpfVencedor` | Texto | Não | CPF do vencedor. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "id_compra": "25500001000181997",
 "id_compra_item": "2550000100018199700001",
 "numero_item_licitacao": 1,
 "uasg": 255000,
 "criterio_julgamento": "Menor Valor",
 "nome_servico": "TRANSCRICAO DE TEXTO",
 "quantidade": "1",
 "valor_estimado": 0
 }
 ],
 "totalRegistros": 3498690,
 "totalPaginas": 349870
}
```

---

### 2.1 Consultar Itens de Licitação por ID
Busca um item específico de uma licitação pelo ID da compra e do item.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/2.1_consultarItemLicitacao_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `id_compra` | Texto | **Sim** | Código da compra. |
| `id_compra_item` | Texto | Não | Código identificador do item. |
| `dt_alteracao` | Texto | Não | Data de alteração. |

---

### 3. Consultar Pregões
Retorna dados específicos sobre pregões (presenciais ou eletrônicos).

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/3_consultarPregoes`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `co_orgao` | Inteiro | Não | Código do órgão. |
| `numero` | Inteiro | Não | Número do pregão. |
| `ds_tipo_pregao_compra` | Texto | Não | Tipo de compra (ex: SISRP). |
| `dt_data_edital_inicial` | Texto | **Sim** | Data inicial de disponibilização do edital. |
| `dt_data_edital_final` | Texto | **Sim** | Data final de disponibilização do edital. |
| `pertence14133` | Booleano | Não | Indica se pertence à Lei 14.133/2021. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "id_compra": "15846405000012023",
 "co_processo": "23295023748202246",
 "co_uasg": 158464,
 "numero": 12023,
 "ds_situacao_pregao": "homologado",
 "ds_tipo_pregao": "eletronico",
 "tx_objeto": "Contratação de empresa especializada...",
 "pertence14133": true
 }
 ]
}
```

---

### 3.1 Consultar Pregões por ID
Busca um pregão específico pelo ID da compra.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/3.1_consultarPregoes_ID`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `id_compra` | Texto | **Sim** | Código da compra. |
| `dt_alteracao` | Texto | Não | Data de alteração. |

---

### 4. Consultar Itens de Pregões
Retorna os itens pertencentes a um pregão.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/4_consultarItensPregoes`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `decreto_7174` | Texto | Não | Filtro decreto 7174 (TRUE/FALSE). |
| `fornecedor_vencedor` | Texto | Não | Nome do fornecedor vencedor. |
| `dt_hom_inicial` | Texto | Não | Data de homologação inicial. |
| `dt_hom_final` | Texto | Não | Data de homologação final. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "id_compra": "11000105000832022",
 "id_compra_item": "1100010500083202200001",
 "situacao_item": "homologado",
 "descricao_item": "Prestação de Serviços de Portaria / Recepção",
 "valorHomologadoItem": "72900.00",
 "dt_hom": "2023-01-09"
 }
 ]
}
```

---

### 4.1 Consultar Itens de Pregões por ID
Busca um item de pregão pelo ID.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/4.1_consultarItensPregoes_ID`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `id_compra` | Texto | **Sim** | Código da compra. |
| `id_compra_item` | Texto | Não | Código do item. |
| `dt_alteracao` | Texto | Não | Data de alteração. |

---

### 5. Consultar Compras sem Licitação
Retorna dados sobre dispensas e inexigibilidades de licitação.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/5_consultarComprasSemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `dt_ano_aviso` | Inteiro | **Sim** | Ano da compra. |
| `nu_aviso_licitacao` | Inteiro | Não | Número da dispensa/inexigibilidade. |
| `co_modalidade_licitacao` | Inteiro | Não | Código da modalidade. |
| `co_orgao` | Inteiro | Não | Código do órgão. |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `dtPublicacao` | Texto | Não | Data da publicação. |
| `pertence14133` | Booleano | Não | Indica se pertence à Lei 14.133/2021. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "idCompra": "20060206000012023",
 "co_uasg": 200602,
 "no_ausg": "PENITENCIÁRIA FEDERAL EM MOSSORO - RN",
 "co_modalidade_licitacao": 6,
 "ds_fundamento_legal": "Fundamento Legal: Art. 75º, Inciso II da Lei nº 14.133...",
 "pertence14133": true
 }
 ]
}
```

---

### 5.1 Consultar Compra sem Licitação por ID
Busca uma dispensa ou inexigibilidade específica pelo ID.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/5.1_consultarCompraSemLicitacao_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `idCompra` | Texto | **Sim** | Código da compra. |

---

### 6. Consultar Itens de Compra sem Licitação
Retorna os itens de uma compra realizada sem licitação.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/6_consultarCompraItensSemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `dt_ano_aviso_licitacao` | Inteiro | **Sim** | Ano da compra. |
| `co_modalidade_licitacao` | Inteiro | Não | Código da modalidade. |
| `co_conjunto_materiais` | Inteiro | Não | Código do material. |
| `co_servico` | Inteiro | Não | Código do serviço. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "idCompra": "17013306000082023",
 "co_uasg": 170133,
 "no_modalidade_licitacao": "Dispensa",
 "ds_objeto_licitacao": "Objeto: Contratação de serviço de instalação...",
 "vr_estimado": 15640.66
 }
 ]
}
```

---

### 6.1 Consultar Itens de Compra sem Licitação por ID
Busca um item específico de uma dispensa/inexigibilidade pelo ID.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/6.1_consultarItensComprasSemLicitacao_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `id_compra` | Texto | **Sim** | Código da compra. |
| `id_compra_item` | Texto | Não | Código do item. |
| `dt_alteracao` | Texto | Não | Data de alteração. |

---

### 7. Consultar RDC (Regime Diferenciado de Contratações)
Consulta licitações realizadas sob o regime RDC.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/7_consultarRdc`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `data_publicacao_max` | Texto | **Sim** | Data máxima da publicação. |
| `data_publicacao_min` | Texto | **Sim** | Data mínima da publicação. |
| `modalidade` | Inteiro | Não | Código da modalidade. |
| `uasg` | Inteiro | Não | Código da UASG. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "data_publicacao": "2019-01-08",
 "identificador": "2544459922012019",
 "modalidade": 99,
 "numero_aviso": 22012019,
 "objeto": "Obra para adequação civil...",
 "tipo_recurso": "Nacional"
 }
 ]
}
```

***

# Módulo Contratações (PNCP)

Este módulo oferece acesso a informações sobre os procedimentos de contratação dos órgãos públicos em conformidade com a legislação vigente (Lei nº 14.133/2021). É possível consultar dados desde a abertura do processo, itens da compra e os resultados homologados.

### 1. Consultar Contratações (Lei 14.133/21)
Retorna a lista de contratações (editais/avisos) publicadas no PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/1_consultarContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `dataPublicacaoPncpInicial` | Texto | **Sim** | Data inicial da publicação no PNCP (YYYY-MM-DD). |
| `dataPublicacaoPncpFinal` | Texto | **Sim** | Data final da publicação no PNCP (YYYY-MM-DD). |
| `codigoModalidade` | Inteiro | **Sim** | Código da modalidade da licitação (ex: 5 - Pregão). |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade do órgão. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `unidadeOrgaoCodigoIbge` | Inteiro | Não | Código do IBGE da unidade. |
| `unidadeOrgaoUfSigla` | Texto | Não | Sigla da UF. |
| `amparoLegalCodigoPncp` | Inteiro | Não | Código do amparo legal específico no PNCP. |
| `contratacaoExcluida` | Booleano | Não | Indica se a contratação foi excluída. |
| `dataAualizacaoPncp` | Texto | Não | Data de atualização no PNCP.* |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "idCompra": "92501005000292023",
 "numeroControlePNCP": "18715615000160-1-001376/2023",
 "anoCompraPncp": 2023,
 "orgaoEntidadeCnpj": "18715615000160",
 "orgaoEntidadeRazaoSocial": "ESTADO DE MINAS GERAIS",
 "unidadeOrgaoNomeUnidade": "CAMARA MUNICIPAL DE UBERLÂNDIA - MG",
 "numeroCompra": "00029",
 "modalidadeNome": "Pregão - Eletrônico",
 "objetoCompra": "Contratação de empresa para fornecimento de equipamento...",
 "valorTotalHomologado": 143655,
 "situacaoCompraNomePncp": "Divulgada no PNCP",
 "dataPublicacaoPncp": "2024-01-15T07:03:38"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1
}
```

---

### 1.1 Consultar Contratações por ID (Lei 14.133/21)
Busca uma contratação específica pelo seu identificador único ou número de controle do PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/1.1_consultarContratacoes_PNCP_14133_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `tipo` | Texto | **Sim** | Indica o tipo do código: `idCompra` ou `numeroControlePNCPCompra`. |
| `codigo` | Texto | **Sim** | Código de identificação da compra. |
| `dataAtualizacaoPncp` | Texto | Não | Data de atualização (YYYY-MM-DD). |

---

### 2. Consultar Itens de Contratações (Lei 14.133/21)
Lista os itens (materiais ou serviços) vinculados às contratações.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/2_consultarItensContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `dataInclusaoPncpInicial` | Texto | **Sim** | Data de Inclusão Inicial no PNCP (YYYY-MM-DD). |
| `dataInclusaoPncpFinal` | Texto | **Sim** | Data de Inclusão Final no PNCP (YYYY-MM-DD). |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade. |
| `materialOuServico` | Texto | Não | `M` - Material ou `S` - Serviço. |
| `situacaoCompraItem` | Texto | Não | Situação do item (ex: 4 - Deserto). |
| `codItemCatalogo` | Inteiro | Não | Código do Item no Catálogo. |
| `codigoClasse` | Inteiro | Não | Código da classe. |
| `temResultado` | Booleano | Não | Informa se tem resultado (`true`/`false`). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "idCompra": "20035006000162023",
 "idContratacaoPNCP": "00394494000136-1-000602/2023",
 "descricaoResumida": "Algodão",
 "materialOuServico": "M",
 "codItemCatalogo": 279727,
 "descricaodetalhada": "Algodão Tipo: Hidrófilo , Apresentação: Em Bolas...",
 "quantidade": 5,
 "valorUnitarioEstimado": 18.56,
 "situacaoCompraItemNome": "Deserto",
 "dataInclusaoPncp": "2023-10-01T19:16:04"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1
}
```

---

### 2.1 Consultar Itens de Contratações por ID
Busca um item específico de uma contratação.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/2.1_consultarItensContratacoes_PNCP_14133_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `tipo` | Texto | **Sim** | `idCompra` ou `numeroControlePNCPCompra`. |
| `codigo` | Texto | **Sim** | Código de identificação da compra. |
| `idCompraItem` | Texto | Não | Código de identificação do item da compra. |
| `dataAtualizacaoPncp` | Texto | Não | Data de atualização (YYYY-MM-DD). |

---

### 3. Consultar Resultados dos Itens (Lei 14.133/21)
Retorna os resultados (homologação) dos itens, incluindo fornecedores vencedores e valores finais.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/3_consultarResultadoItensContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `dataResultadoPncpInicial` | Texto | **Sim** | Data inicial do resultado no PNCP. |
| `dataResultadoPncpFinal` | Texto | **Sim** | Data final do resultado no PNCP. |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade do órgão. |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `nifFornecedor` | Texto | Não | CPF/CNPJ do fornecedor. |
| `valorTotalHomologadoFinal` | Texto | Não | Valor total final homologado. |
| `aplicacaoMargemPreferencia` | Booleano | Não | Se houve margem de preferência. |
| `aplicacaoBeneficioMeepp` | Booleano | Não | Se houve benefício ME/EPP. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "idCompra": "15512405900762024",
 "numeroItemPncp": 12,
 "niFornecedor": "28546470000174",
 "nomeRazaoSocialFornecedor": "SOUZA MED COMERCIO DE MATERIAIS...",
 "quantidadeHomologada": 300,
 "valorUnitarioHomologado": 13.55,
 "valorTotalHomologado": 4065,
 "situacaoCompraItemResultadoNome": "Informado",
 "dataResultadoPncp": "2024-11-01T00:00:00"
 }
 ],
 "totalRegistros": 0,
 "totalPaginas": 0
}
```

---

### 3.1 Consultar Resultados dos Itens por ID
Busca o resultado de um item específico pelo ID da compra e do item.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/3.1_consultarResultadoItensContratacoes_PNCP_14133_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `tipo` | Texto | **Sim** | `idCompra` ou `numeroControlePNCPCompra`. |
| `codigo` | Texto | **Sim** | Código de identificação da compra. |
| `idCompraItem` | Texto | Não | Código de identificação do item. |
| `dataAtualizacaoPncp` | Texto | Não | Data de atualização (YYYY-MM-DD). |

***

# Módulo ARP

As Atas de Registro de Preços (ARP) são documentos que estabelecem condições e quantidades para futuras aquisições de bens e serviços. Por meio deste módulo, obtêm-se detalhes das ARPs vigentes e de suas especificidades, facilitando o planejamento e o monitoramento das compras.

### 1. Consultar ARP
Retorna uma lista de Atas de Registro de Preços com base nos filtros informados.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/1_consultarARP`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `codigoUnidadeGerenciadora` | Inteiro | Não | Código da unidade responsável pela ata. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade de compra. |
| `numeroAtaRegistroPreco` | Texto | Não | Número da Ata de Registro de Preço. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data mínima de início da vigência (YYYY-MM-DD). |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data máxima de início da vigência (YYYY-MM-DD). |
| `dataAssinaturaInicial` | Texto | Não | Data inicial da assinatura. |
| `dataAssinaturaFinal` | Texto | Não | Data final da assinatura. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "numeroAtaRegistroPreco": "00044/2023",
 "codigoUnidadeGerenciadora": 160482,
 "nomeUnidadeGerenciadora": "COMANDO/1A BRIGADA DE INFANTARIA DE SELVA",
 "codigoOrgao": 52121,
 "nomeOrgao": "COMANDO DO EXERCITO",
 "linkAtaPNCP": "https://pncp.gov.br/app/atas/...",
 "dataAssinatura": "2023-12-22",
 "dataVigenciaInicial": "2023-12-22",
 "dataVigenciaFinal": "2024-12-22"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1
}
```

---

### 1.1 Consultar ARP por ID
Busca os dados detalhados de uma ARP específica utilizando seu identificador único no PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/1.1_consultarARP_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroControlePncpAta` | Texto | **Sim** | Número de controle da Ata no PNCP. |
| `dataAtualizacao` | Texto | Não | Data de atualização para filtro incremental. |

---

### 1.2 Consultar ARP por Fim de Vigência
Endpoint específico para filtrar ARPs com base no término de sua vigência.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/1.2_consultarARP_FimVigencia`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `dataVigenciaFinalMin` | Texto | **Sim** | Data mínima do fim da vigência. |
| `dataVigenciaFinalMax` | Texto | **Sim** | Data máxima do fim da vigência. |
| `codigoUnidadeGerenciadora` | Inteiro | Não | Código da unidade gerenciadora. |
| `numeroAtaRegistroPreco` | Texto | Não | Número da Ata. |

---

### 2. Consultar Item da ARP
Retorna a lista de itens associados a uma ARP, incluindo descrição, quantidades e fornecedores.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/2_consultarARPItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoUnidadeGerenciadora` | Inteiro | Não | Código da unidade gerenciadora. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data mínima de início da vigência. |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data máxima de início da vigência. |
| `numeroItem` | Inteiro | Não | Número do item na ata. |
| `codigoItem` | Inteiro | Não | Código do item (material/serviço). |
| `tipoItem` | Texto | Não | Tipo do item (M - Material / S - Serviço). |
| `niFornecedor` | Texto | Não | CNPJ/CPF do fornecedor. |

---

### 2.1 Consultar Item da ARP por ID
Busca os detalhes de itens de uma ARP específica pelo ID do PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/2.1_consultarARPItem_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroControlePncpAta` | Texto | **Sim** | Número de controle da Ata no PNCP. |
| `dataAtualizacao` | Texto | Não | Data de atualização. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "numeroAtaRegistroPreco": "string",
 "codigoUnidadeGerenciadora": 0,
 "nomeUnidadeGerenciadora": "string",
 "valorTotal": 0,
 "quantidadeItens": 0,
 "numeroControlePncpAta": "string",
 "idCompra": "string"
 }
 ]
}
```

---

### 3. Consultar Unidades do Item
Serviço que permite consultar os dados das unidades participantes e saldos de um item específico de uma Ata.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/3_consultarUnidadesItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Inteiro | **Sim** | Código da unidade gerenciadora. |
| `numeroItem` | Inteiro | **Sim** | Número do item na ata. |
| `pagina` | Inteiro | Não | Paginação dos resultados. |

---

### 4. Consultar Empenhos e Saldo do Item
Permite consultar os saldos e quantidades já empenhadas de um item em uma Ata de Registro de Preços.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/4_consultarEmpenhosSaldoItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Inteiro | **Sim** | Código da unidade gerenciadora. |
| `pagina` | Inteiro | Não | Paginação dos resultados. |

---

### 5. Consultar Adesões do Item
Lista as adesões ("caronas") realizadas a um item da ata por outros órgãos.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/5_consultarAdesoesItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Inteiro | **Sim** | Código da unidade gerenciadora. |
| `numeroItem` | Inteiro | Não | Número do item. |
| `unidade` | Inteiro | Não | Código da unidade aderente. |

***

# Módulo Contratos

Este módulo reúne dados referentes aos contratos firmados no âmbito público, abrangendo informações como objeto, valor, prazo de vigência e partes envolvidas. Ele permite acompanhar a execução contratual e monitorar prazos de vencimento.

### 1. Consultar Contratos
Retorna uma lista de contratos com base nos filtros aplicados, como órgão, unidade gestora e período de vigência inicial.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/1_consultarContratos`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `codigoUnidadeGestora` | Inteiro | Não | Código da unidade gestora. |
| `codigoUnidadeGestoraOrigemContrato`| Inteiro | Não | Código da UG de origem do contrato. |
| `codigoUnidadeRealizadoraCompra` | Inteiro | Não | Código da UG que realizou a compra. |
| `numeroContrato` | Texto | Não | Número do contrato. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade de compra. |
| `codigoTipo` | Inteiro | Não | Código do tipo de contrato. |
| `codigoCategoria` | Inteiro | Não | Código da categoria do contrato. |
| `niFornecedor` | Texto | Não | CPF/CNPJ do fornecedor. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data inicial mínima da vigência (YYYY-MM-DD). |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data inicial máxima da vigência (YYYY-MM-DD). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoOrgao": 99537,
 "nomeOrgao": "PMSP - SUBPREFEITURA SAPOPEMBA",
 "codigoUnidadeGestora": 110161,
 "nomeUnidadeGestora": "SUPERINTENDENCIA REG. DE ADMIN. DA 1ª REGIAO",
 "numeroContrato": "2023NE053456",
 "numeroCompra": "00006/2023",
 "codigoModalidadeCompra": "6",
 "nomeModalidadeCompra": "Dispensa",
 "codigoTipo": 99,
 "nomeTipo": "Empenho",
 "niFornecedor": "46051880000126",
 "nomeRazaoSocialFornecedor": "FB MULTI NEGOCIOS LTDA",
 "objeto": "LAGE EM CONCRETO ARMADO PARA BOCA DE LOBO.",
 "dataVigenciaInicial": "2023-08-28T00:00:00",
 "dataVigenciaFinal": "2023-08-28T00:00:00",
 "valorGlobal": 16315,
 "numeroControlePncpContrato": "05546795000151-2-000140/2023"
 }
 ],
 "totalRegistros": 44,
 "totalPaginas": 5
}
```

---

### 1.1 Consultar Contratos por ID
Busca os dados detalhados de um contrato específico utilizando seu identificador único no PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/1.1_consultarContratos_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroControlePncpContrato` | Texto | **Sim** | Identificador único do contrato (25 dígitos). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoOrgao": "string",
 "nomeOrgao": "string",
 "numeroContrato": "string",
 "niFornecedor": "string",
 "nomeRazaoSocialFornecedor": "string",
 "objeto": "string",
 "dataVigenciaInicial": "2026-01-19T14:22:41.995Z",
 "dataVigenciaFinal": "2026-01-19T14:22:41.995Z",
 "valorGlobal": 0,
 "numeroControlePncpContrato": "string",
 "contratoExcluido": true
 }
 ]
}
```

---

### 1.2 Consultar Contratos por Fim de Vigência
Permite filtrar contratos cujo fim de vigência ocorra dentro de um intervalo de datas específico.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/1.2_consultarContratos_FimVigencia`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `dataVigenciaFinalMin` | Texto | **Sim** | Data mínima do fim da vigência (YYYY-MM-DD). |
| `dataVigenciaFinalMax` | Texto | **Sim** | Data máxima do fim da vigência (YYYY-MM-DD). |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `codigoUnidadeGestora` | Inteiro | Não | Código da unidade gestora. |
| `niFornecedor` | Texto | Não | CNPJ/CPF do fornecedor. |

---

### 2. Consultar Item de Contratos
Lista os itens (materiais ou serviços) vinculados aos contratos, exibindo quantidades e valores unitários.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/2_consultarContratosItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `codigoUnidadeGestora` | Inteiro | Não | Código da unidade gestora. |
| `numeroContrato` | Texto | Não | Número do contrato. |
| `codigoItem` | Inteiro | Não | Código do item (CATMAT/CATSER). |
| `tipoItem` | Texto | Não | Tipo do item (Material/Serviço). |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data inicial mínima da vigência. |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data inicial máxima da vigência. |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "codigoOrgao": 22000,
 "numeroContrato": "00062/2021",
 "niFornecedor": "30479645000110",
 "nomeRazaoSocialFornecedor": "AMR SOLUCOES LABORATORIAIS LTDA",
 "dataVigenciaInicial": "2021-10-27T00:00:00",
 "dataVigenciaFinal": "2022-01-24T00:00:00",
 "valorGlobal": 20078,
 "codigoItem": 409245,
 "descricaoIitem": "BALÃO LABORATÓRIO",
 "quantidadeItem": 100,
 "valorUnitarioItem": 89,
 "valorTotalItem": 8900
 }
 ]
}
```

---

### 2.1 Consultar Item de Contratos por ID
Busca os itens de um contrato específico utilizando o número de controle do PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/2.1_consultarContratosItem_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroControlePncpContrato` | Texto | **Sim** | Identificador único do contrato no PNCP. |

***

# Módulo Fornecedor

Este módulo reúne informações cadastrais de fornecedores que atuam com a Administração Pública, facilitando a identificação, análise e acompanhamento dos registros nos sistemas governamentais.

### 1. Consultar Fornecedor
Lista ou detalha os dados cadastrais dos fornecedores, exibindo informações como CNPJ ou CPF, razão social, localização, porte, atividade econômica (CNAE) e situação de habilitação para licitar.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-fornecedor/1_consultarFornecedor`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `cnpj` | Texto | Não | CNPJ do fornecedor (sem pontuação). |
| `cpf` | Texto | Não | CPF do fornecedor (sem pontuação). |
| `naturezaJuridicaId` | Inteiro | Não | ID da natureza jurídica. |
| `porteEmpresaId` | Inteiro | Não | ID do porte da empresa. |
| `codigoCnae` | Inteiro | Não | Código CNAE (Classificação Nacional de Atividades Econômicas). |
| `ativo` | Booleano | **Sim** | Indica se o fornecedor está ativo (`true`) ou inativo (`false`). |

**Exemplo de Resposta:**
```json
{
 "resultado": [
 {
 "ativo": true,
 "cnpj": "00001172000180",
 "cpf": null,
 "habilitadoLicitar": true,
 "codigoCnae": 5822101,
 "nomeCnae": "EDICAO INTEGRADA A IMPRESSAO DE JORNAIS",
 "nomeMunicipio": "BRASILIA",
 "naturezaJuridicaId": 2038,
 "naturezaJuridicaNome": "SOCIEDADE DE ECONOMIA MISTA",
 "porteEmpresaId": 3,
 "porteEmpresaNome": "DEMAIS",
 "nomeRazaoSocialFornecedor": "EMPRESA BRASILEIRA DE CORREIOS E TELEGRAFOS",
 "ufSigla": "DF"
 }
 ],
 "totalRegistros": 1,
 "totalPaginas": 1,
 "paginasRestantes": 0
}
```

***

# Módulo OCDS

O OCDS (Open Contracting Data Standard) é um padrão global de dados abertos para contratações públicas. Este módulo entrega os dados estruturados conforme normas internacionais, facilitando a interoperabilidade e a análise comparativa de gastos públicos.

### 1. Consultar Releases
Serviço que permite consultar as contratações ("releases") formatadas segundo o padrão *Open Contracting Data Standard*, possibilitando a extração de todo o ciclo de vida da contratação em um formato universalmente aceito.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-ocds/1_releases`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `page` | Inteiro | Não | Referente a paginação dos resultados (Padrão: 1). |
| `offset` | Inteiro | Não | Quantidade de registros a pular (deslocamento). |
| `buyerID` | Texto | **Sim** | Identificador único do comprador (Órgão/Unidade). |
| `releaseStartDate` | Texto | **Sim** | Data inicial do período de publicação do release (YYYY-MM-DD). |
| `releaseEndDate` | Texto | **Sim** | Data final do período de publicação do release (YYYY-MM-DD). |
