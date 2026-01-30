<div align="center">

# 🏛️ API de Dados Abertos de Compras Governamentais

![Gov.br](https://www.gov.br/transferegov/pt-br/noticias/noticias/arquivos-e-imagens/mgi.png)

![Status](https://img.shields.io/badge/Status-Online-00995D?style=for-the-badge)
![Versão](https://img.shields.io/badge/Versão-v3.0-FFCD00?style=for-the-badge&labelColor=gov.br)

**Base URL:** `https://dadosabertos.compras.gov.br`

</div>

---

O Sistema Integrado de Administração de Serviços Gerais – Siasg, instituído pelo art. 7º do Decreto nº 1.094, de 23 de março de 1994, é o sistema informatizado de apoio às atividades operacionais do Sistema de Serviços Gerais – Sisg. A finalidade do Siasg é integrar os órgãos da Administração Pública Federal direta, autárquica e fundacional. Após a reestruturação do Sisg (nova releitura), o SIASG passa a receber o sistema de contratações do governo federal, Compras.gov.br. O Compras.gov.br é composto por diversos módulos responsáveis pela operacionalização de cada uma das várias etapas da cadeia da contratação pública: SICAF, PGC, Catálogo, Divulgação de compras, Sala de disputa, Contratos e muito mais.

O ecossistema Compras.gov.br deverá ser um sistema único e integrado, permitindo a operacionalização e controle de diversas etapas ao longo do ciclo de vida da compra pública. Será possível aos servidores públicos, gestores de governo, fornecedores, órgãos de controle e cidadãos interagirem entre si no sistema, e com o sistema, extraindo, dele, seu objetivo final.

Dessa forma, o Compras.gov.br ganha relevância estratégica, passando a ser visto como um instrumento de apoio, transparência e controle na execução das atividades do Sisg, por meio da informatização e operacionalização do conjunto de suas atividades, bem como no gerenciamento de todos os seus processos.

A prestação de dados como um serviço governamental traz vantagens para toda a sociedade, incluindo o próprio governo. O Ministério Economia está racionando recursos através da publicação dessas informações na Internet.

A disponibilização dos dados das Compras Governamentais é um compromisso firmado pelo governo brasileiro na Parceria para Governo Aberto (Open Government Partnership - OGP do inglês). O governo está comprometido em promover a transparência dos gastos públicos, fornecer informações de valor agregado à sociedade e promover a pesquisa e inovação tecnológica através da implementação da política brasileira de dados abertos.

https://dadosabertos.compras.gov.br/swagger-ui/index.html


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

O Catálogo de Materiais (CATMAT) e o Catálogo de Serviços (CATSER), do Sistema Integrado de Administração e Serviços Gerais – SIASG, são as bases de dados que identificam todos os materiais licitados e adquiridos e todos serviços licitados contratados pela Administração Pública Federal. Todas as operações realizadas por meio do SIASG/Compras Governamentais utilizam esses catálogos para definir os objetos das respectivas licitações e contratações. A organização dos dados nos catálogos tem impacto direto na qualidade da informação proveniente do SIASG e no cruzamento de informações sobre o gasto público.

Ferramenta de auxiliar: https://catalogo.compras.gov.br/cnbs-web/busca

### 1. Consultar Grupo de Material
Serviço que permite consultar os dados de um grupo de material pelo código do grupo de material e/ou status do grupo.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>

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
</details>

---

### 2. Consultar Classe de Material
Serviço que permite consultar os dados de uma classe de material pelo código do grupo de material, código da classe e/ou status do grupo.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 3. Consultar PDM (Produto Descritivo Básico)
Serviço que permite consultar os dados de um Produto Descritivo Básico - PDM de material pelo código de PDM, código do grupo de material, código da classe e/ou status do PDM.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 4. Consultar Item de Material
Serviço que permite consultar os dados de um item de material pelo código do grupo de material, código da classe, código do PDM, código do item e/ou status do grupo.

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
| `bps` | Booleano | Não | Indica se segue as Boas Práticas de Suprimentos. |
| `codigo_ncm` | Texto | Não | Código NCM. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/4_consultarItemMaterial?codigoItem=46736`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 5. Consultar Natureza de Despesa do Item
Serviço que permite consultar os dados de uma nautreza de material pelo código do PDM e/ou código da natureza de despesa.

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

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/5_consultarMaterialNaturezaDespesa?codigoPdm=6&codigoNaturezaDespesa=33903016&statusNaturezaDespesa=true`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
    "totalRegistros": 1,
    "totalPaginas": 0,
    "paginasRestantes": 0
}
```
</details>

---

### 6. Consultar Unidade de Fornecimento
Serviço que permite consultar os dados de unidade de fornecimento de material pelo código do PDM.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/6_consultarMaterialUnidadeFornecimento`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoPdm` | Inteiro | Não | Código do PDM. |
| `statusUnidadeFornecimentoPdm` | Booleano | Não | 0 - False/Inativo; 1 - True/Ativo. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/6_consultarMaterialUnidadeFornecimento?codigoPdm=11&statusUnidadeFornecimentoPdm=True`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
 }...
```
</details>

---

### 7. Consultar Características de Materiais
Serviço que permite consultar os dados de características de material pelo código do PDM do item.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-material/7_consultarMaterialCaracteristicas`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoItem` | Inteiro | Não | Código do item do material. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/7_consultarMaterialCaracteristicas?codigoItem=46736`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

***

# Módulo Serviço

O Catálogo de Materiais (CATMAT) e o Catálogo de Serviços (CATSER), do Sistema Integrado de Administração e Serviços Gerais – SIASG, são as bases de dados que identificam todos os materiais licitados e adquiridos e todos serviços licitados contratados pela Administração Pública Federal. Todas as operações realizadas por meio do SIASG/Compras Governamentais utilizam esses catálogos para definir os objetos das respectivas licitações e contratações. A organização dos dados nos catálogos tem impacto direto na qualidade da informação proveniente do SIASG e no cruzamento de informações sobre o gasto público.

Ferramenta de auxiliar: https://catalogo.compras.gov.br/cnbs-web/busca

### 1. Consultar Seção de Serviço
Serviço que permite consultar os dados de uma seção de serviço pelo código da seção e/ou status da seção.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 2. Consultar Divisão de Serviço
Serviço que permite consultar os dados de uma divisão de serviço pelo código da seção, da divisão e/ou status da divisão.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>

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
</details>

---

### 3. Consultar Grupo de Serviço
Serviço que permite consultar os dados de um grupo de serviço pelo código da divisão, do grupo e/ou status do grupo.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 4. Consultar Classe de Serviço
Serviço que permite consultar os dados de uma classe de serviço pelo código do grupo, da classe e/ou status da classe.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 5. Consultar SubClasse de Serviço
Serviço que permite consultar os dados de uma subclasse de serviço pelo código da classe, da subclasse e/ou status da subclasse.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 6. Consultar Item de Serviço
Serviço que permite consultar os dados de um item de serviço pelo código da subclasse, do cpc, do serviço do e/ou status do serviço.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 7. Consultar Unidade de Medida de Serviço
Serviço que permite consultar os dados de unidade de medida pelo código do serviço e/ou status da unidade e medida.

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

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 8. Consultar Natureza de Despesa do Serviço
Serviço que permite consultar os dados de natureza de despesa pelo código do serviço, da natureza de despesa e/ou status da natureza de despesa.

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

**URL:** `https://dadosabertos.compras.gov.br/modulo-servico/8_consultarNaturezaDespesaServico?codigoServico=19&codigoNaturezaDespesa=33903905&statusNaturezaDespesa=true`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

***

# Módulo Pesquisa de Preço

O serviço de consulta permite acesso aos dados e informações de itens comprados por meio da Administração, o qual tem como objetivo auxiliar os órgãos governamentais na etapa de pesquisa de preços, que é um passo crucial no planejamento de compras e contratações públicas.

### 1. Consultar Material
Serviço que permite consultar os dados de preços praticados na aquisição de materias pelo sistema Compras.gov.br.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/1_consultarMaterial`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `codigoItemCatalogo` | Inteiro | **Sim** | Código do item do material (CATMAT). |
| `codigoUasg` | Texto | Não | Código da UASG. |
| `estado` | Texto | Não | Sigla da UF. |
| `codigoMunicipio` | Inteiro | Não | Código do município (IBGE). |
| `dataResultado` | Booleano | Não | Filtro por data do resultado. |
| `codigoClasse` | Inteiro | Não | Código da classe do material. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pesquisa-preco/1_consultarMaterial?pagina=1&tamanhoPagina=10&codigoItemCatalogo=470419&estado=RJ&codigoMunicipio=3303302&codigoClasse=6145`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "79158006900142024",
            "idItemCompra": 4737361,
            "forma": "SISPP",
            "modalidade": 6,
            "criterioJulgamento": "1",
            "numeroItemCompra": 11,
            "descricaoItem": "CABO ELÉTRICO ISOLADO, MATERIAL CONDUTOR: COBRE NU , TÊMPERA CONDUTOR: MOLE , SEÇÃO NOMINAL: 2,5 MM2, TENSÃO ISOLAMENTO: 0,6/1 KV, COR DO ISOLAMENTO: PRETA , CARACTERÍSTICAS ADICIONAIS: EXTRA FLEXÍVEL ISOLAÇÃO DE HEPR 90ºC , APLICAÇÃO: INSTALAÇÕES ELÉTRICAS , NORMAS TÉCNICAS: NBR 5410, NBR 7286 E NBR NM 280 , QUANTIDADE CONDUTORES: 4 , CLASSE DE ENCORDOAMENTO: 5 ",
            "codigoItemCatalogo": 470419,
            "nomeUnidadeMedida": null,
            "siglaUnidadeMedida": null,
            "nomeUnidadeFornecimento": "METRO",
            "siglaUnidadeFornecimento": "M",
            "capacidadeUnidadeFornecimento": 0E-8,
            "quantidade": 200.00000000,
            "precoUnitario": 3.50000000,
            "percentualMaiorDesconto": 0E-8,
            "niFornecedor": "52347972000150",
            "nomeFornecedor": "GATHUS COMERCIAL LTDA",
            "marca": "dvs",
            "codigoUasg": "791580",
            "nomeUasg": "BASE ALMIRANTE CASTRO E SILVA",
            "codigoMunicipio": 3303302,
            "municipio": "NITERÓI",
            "estado": "RJ",
            "codigoOrgao": 52131,
            "nomeOrgao": "COMANDO DA MARINHA",
            "poder": "E",
            "esfera": "F",
            "dataCompra": "2024-03-27T03:00:00.000+00:00",
            "dataHoraAtualizacaoCompra": "2025-03-28T03:29:59.886503",
            "dataHoraAtualizacaoItem": "2025-03-28T03:59:59.883588",
            "dataResultado": "2024-03-27T03:00:00.000+00:00",
            "dataHoraAtualizacaoUasg": "2025-08-21T10:02:00",
            "codigoClasse": 6145,
            "nomeClasse": "FIOS E CABOS ELÉTRICOS"
        }...
```
</details>

---

### 1.1 Consultar Material (CSV)
Versão do endpoint acima que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/1.1_consultarMaterial_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarMaterial`.

---

### 2. Consultar Detalhe do Material
Serviço que permite consultar os dados das descrições dos itens de materias.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/2_consultarMaterialDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `idCompra` | Texto | **Sim** | Código identificador da compra. |
| `codigoItemCatalogo` | Inteiro | Não | Código do item do material. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pesquisa-preco/2_consultarMaterialDetalhe?pagina=1&idCompra=98108305000252023&codigoItemCatalogo=446573`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "98108305000252023",
            "idItemCompra": 3845064,
            "numeroItemCompra": 1,
            "codigoItemCatalogo": 446573,
            "objetoCompra": "Objeto: Pregão Eletrônico -  É o REGISTRO DE PREÇOS para futuras e eventuais contratações de fornecimento de forma parcelado, de peças diversas para manutenção de veículos, destinados a Prefeitura Municipal de Francisco Santos   PI, Secretaria Municipal de Saúde, Secretaria Municipal de Educação e Secretaria Municipal de Assistência Social.",
            "descricaoDetalhadaItem": "ACESSÓRIOS / EQUIPAMENTOS OFICINA MANUTENÇÃO, TIPO CARRO ESTEIRA, MATERIAL AÇO"
        }...
```
</details>

---

### 2.1 Consultar Detalhe do Material (CSV)
Versão do endpoint de detalhe em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/2.1_consultarMaterialDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarMaterialDetalhe`.

---

### 3. Consultar Serviço
Serviço que permite consultar os dados de preços praticados na contração de serviços pelo sistema Compras.gov.br.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/3_consultarServico`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `codigoItemCatalogo` | Inteiro | **Sim** | Código do item do serviço (CATSER). |
| `codigoUasg` | Texto | Não | Código da UASG. |
| `estado` | Texto | Não | Sigla da UF. |
| `codigoMunicipio` | Inteiro | Não | Código do município. |
| `dataResultado` | Booleano | Não | Filtro por data do resultado. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pesquisa-preco/3_consultarServico?codigoItemCatalogo=1627&codigoUasg=153063&estado=PA&codigoMunicipio=1501402`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "15306306005992025",
            "idItemCompra": 9416418,
            "forma": "SISPP",
            "modalidade": 6,
            "criterioJulgamento": "0",
            "numeroItemCompra": 3,
            "descricaoItem": "MANUTENCAO / REFORMA PREDIAL",
            "codigoItemCatalogo": 1627,
            "nomeUnidadeMedida": "UNIDADE",
            "siglaUnidadeMedida": "UN",
            "quantidade": 1.00000000,
            "precoUnitario": 1350.00000000,
            "percentualMaiorDesconto": 0E-8,
            "niFornecedor": "63848469000103",
            "nomeFornecedor": "TECNOBEL SERVICOS E EQUIPAMENTOS ELETRONICOS LTDA",
            "codigoUasg": "153063",
            "nomeUasg": "UNIVERSIDADE FEDERAL DO PARA/PA",
            "codigoMunicipio": 1501402,
            "municipio": "BELÉM",
            "estado": "PA",
            "codigoOrgao": 26239,
            "nomeOrgao": "UNIVERSIDADE FEDERAL DO PARA",
            "poder": "E",
            "esfera": "F",
            "dataCompra": "2025-09-09T03:00:00.000+00:00",
            "dataHoraAtualizacaoCompra": "2025-09-11T02:18:21.342087",
            "dataHoraAtualizacaoItem": "2025-09-11T03:23:41.336154",
            "dataResultado": "2025-09-10T03:00:00.000+00:00",
            "dataHoraAtualizacaoUasg": "2025-07-07T15:16:00"
        }...
```
</details>

---

### 3.1 Consultar Serviço (CSV)
Versão do endpoint de serviço em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/3.1_consultarServico_CSV`

**Parâmetros:** Os mesmos do endpoint `3_consultarServico`.

---

### 4. Consultar Detalhe do Serviço
Serviço que permite consultar os dados das descrições dos itens de serviços.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/4_consultarServicoDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `idCompra` | Texto | **Sim** | Código identificador da compra. |
| `codigoItemCatalogo` | Inteiro | Não | Código do item do serviço. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pesquisa-preco/4_consultarServicoDetalhe?idCompra=7001905000472023&codigoItemCatalogo=1627`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "7001905000472023",
            "idItemCompra": 4182566,
            "numeroItemCompra": 1,
            "codigoItemCatalogo": 1627,
            "objetoCompra": "Objeto: Pregão Eletrônico -  Prestação de serviços de manutenções prediais preventivas e corretivas nos prédios de propriedade do Tribunal Regional Eleitoral do Paraná, com regime de dedicação exclusiva de mão de obra.",
            "descricaoDetalhadaItem": "Prestação de serviços de manutenções prediais preventivas e corretivas nos prédios de propriedade do Tribunal Regional Eleitoral do Paraná, com regime de dedicação exclusiva de mão de obra"
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0,
    "dataHoraConsulta": "2025-05-07T17:43:42.913926881",
    "timeZoneAtual": "GMT-03:00"
}
```
</details>

---

### 4.1 Consultar Detalhe do Serviço (CSV)
Versão do endpoint de detalhe de serviço em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pesquisa-preco/4.1_consultarServicoDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `4_consultarServicoDetalhe`.

---

# Módulo PGC

O PGC, no contexto da administração pública brasileira, refere-se ao planejamento e gerenciamento de contratações. Esse plano é uma ferramenta estratégica utilizada por órgãos e entidades do governo para planejar, organizar e controlar suas contratações e aquisições. O objetivo do PGC é otimizar os processos de compras e contratações, garantindo maior eficiência, economicidade e transparência.

### 1. Consultar Itens do Plano de Contratação (Detalhe)
Serviço que permite consultar os dados dos itens do plano de contratação de um órgão.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/1_consultarPgcDetalhe`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `orgao` | Texto | **Sim** | CNPJ do Órgão (sem pontuação). |
| `anoPcaProjetoCompra` | Inteiro | **Sim** | Ano do projeto/plano (ex: 2022). |
| `codigoUasg` | Texto | Não | Código da UASG da contratação. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pgc/1_consultarPgcDetalhe?pagina=1&tamanhoPagina=10&orgao=05457283000119&anoPcaProjetoCompra=2022&codigoUasg=540004`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "codigoUasg": "540004",
            "nomeUasg": "COORDENAÇÃO-GERAL DE RECURSOS LOGÍSTICOS",
            "orgao": "05457283000119",
            "numeroArtefato": 30,
            "anoArtefato": 2021,
            "codigoEstadoArtefato": 9,
            "codigoCategoriaArtefato": 3,
            "descricaoArtefato": "30/2021",
            "codigoTipoArtefato": 5,
            "ordemDfd": null,
            "descricaoObjetoDfd": "Adquirir microcomputadores",
            "nivelPrioridadeDfd": 2,
            "dataPrevistaFormalizacaoDemanda": "2022-12-31T00:00:00",
            "codigoAreaDfd": "21534",
            "tipoItem": "M",
            "itemSustentavel": false,
            "codigoGrupoNaterial": 70,
            "nomeGrupoMaterial": "INFORMÁTICA - EQUIPAMENTOS,  PEÇAS, ACESSÓRIOS E SUPRIMENTOSDE TIC",
            "codigoClasseMaterial": 7010,
            "nomeClasseMaterial": "COMPUTADORES",
            "codigoPdmMaterial": 14176,
            "nomePdmMaterial": "\"MICROCOMPUTADOR\"",
            "codigoSecaoServico": null,
            "nomeSecaoServico": null,
            "codigoDivisaoServico": null,
            "nomeDivisaoServico": null,
            "codigoGrupoServico": null,
            "nomeGrupoServico": null,
            "codigoClasseServico": null,
            "nomeClasseServico": null,
            "codigoSubclasseServico": null,
            "nomeSubclasseServico": null,
            "codigoItemCatalogo": "297280",
            "descricaoItemCatalogo": "\"MICROCOMPUTADOR\", PROCESSADOR: SEMPROM 2200 , MEMÓRIA RAM: 256 MB, DISCO RÍGIDO: HD IDE 40, 7200 RPM GB, DISCO FLEXÍVEL: 1.44 MB, DRIVE CD ROM: 52X , GABINETE: ATX 4 BAIAS , MONITOR: 15 POL, COMPONENTES ADICIONAIS: 2 COOLER , CARACTERÍSTICAS ADICIONAIS: CHIPSET N FORCE2 (ASUS OU SIMILAR), MOUSE , PLACA MÃE: ON-BORD COM 2 PORTAS IDE ATA 133 , TECLADO: ABNT 2 , COMPATIBILIDADE INTERFACE: WINDOWS E LINUX , FONTE ALIMENTAÇÃO: 400 W",
            "siglaUnidadeFornecimento": null,
            "nomeUnidadeFornecimento": null,
            "quantidadeItem": 219,
            "valorUnitarioItem": 5004.65,
            "valorTotalItem": 1096018.35,
            "tituloProjetoCompra": "Adquirir microcomputadores",
            "descricaoProjetoCompra": "Adquirir microcomputadores",
            "anoPcaProjetoCompra": 2022,
            "dataInicioProcessoCompra": "2022-02-10T22:14:53",
            "dataFimProcessoCompra": "2022-08-09T22:14:53",
            "duracaoProcessoCompra": 180,
            "numeroItemPncp": 1,
            "statusContratacaoExecucao": null,
            "dataHoraPublicacaoPncp": "2023-05-20T05:20:57.248023",
            "dataHoraAtualizacaoArtefato": "2022-08-09T22:14:54.263",
            "dataHoraAtualizacaoProjetoCompra": "2022-08-09T22:14:54",
            "dataHoraAtualizacaoDfd": "2023-05-20T05:20:58",
            "dataHoraAtualizacaoItem": "2023-05-20T05:20:57.681263"
        }...
```
</details>

---

### 1.1 Consultar Itens do Plano (CSV)
Versão do endpoint de detalhe que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/1.1_consultarPgcDetalhe_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarPgcDetalhe`.

---

### 2. Consultar Itens por Catálogo (CATMAT/CATSER)
Serviço que permite consultar os dados de itens do planejamento da contratação por código de catmat ou catser.

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pgc/2_consultarPgcDetalheCatalogo?pagina=1&tamanhoPagina=10&anoPcaProjetoCompra=2022&tipo=Material&codigo=7010`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "codigoUasg": "110001",
            "nomeUasg": "SECRETARIA DE ADMINISTRAÇÃO",
            "orgao": "00394411000109",
            "numeroArtefato": 345,
            "anoArtefato": 2022,
            "codigoEstadoArtefato": 9,
            "codigoCategoriaArtefato": 3,
            "descricaoArtefato": "345/2022",
            "codigoTipoArtefato": 5,
            "ordemDfd": null,
            "descricaoObjetoDfd": "MICROCOMPUTADOR, MEMÓRIA RAM SUPERIOR A 8, NÚCLEOS POR PROCESSADOR 5 A 8, ARMAZENAMENTO HDD SEM DISCO HDD, ARMAZENAMENTO SSD 110 A 300, MONITOR 21 A 29, COMPONENTES ADICIONAIS COM TECLADO E MOUSE, SISTEMA OPERACIONAL PROPRIETÁRIO, GARANTIA ON SITE SUPERIOR A 36",
            "nivelPrioridadeDfd": 0,
            "dataPrevistaFormalizacaoDemanda": "2022-06-01T00:00:00",
            "codigoAreaDfd": "22153",
            "tipoItem": "M",
            "itemSustentavel": false,
            "codigoGrupoNaterial": 70,
            "nomeGrupoMaterial": "INFORMÁTICA - EQUIPAMENTOS,  PEÇAS, ACESSÓRIOS E SUPRIMENTOSDE TIC",
            "codigoClasseMaterial": 7010,
            "nomeClasseMaterial": "COMPUTADORES",
            "codigoPdmMaterial": 6661,
            "nomePdmMaterial": "MICROCOMPUTADOR",
            "codigoSecaoServico": null,
            "nomeSecaoServico": null,
            "codigoDivisaoServico": null,
            "nomeDivisaoServico": null,
            "codigoGrupoServico": null,
            "nomeGrupoServico": null,
            "codigoClasseServico": null,
            "nomeClasseServico": null,
            "codigoSubclasseServico": null,
            "nomeSubclasseServico": null,
            "codigoItemCatalogo": "453965",
            "descricaoItemCatalogo": "MICROCOMPUTADOR, MEMÓRIA RAM: SUPERIOR A 8 GB, NÚCLEOS POR PROCESSADOR: 5 A 8 , ARMAZENAMENTO HDD: SEM DISCO HDD GB, ARMAZENAMENTO SSD: 110 A 300 , MONITOR: 21 A 29 POL, COMPONENTES ADICIONAIS: COM TECLADO E MOUSE , SISTEMA OPERACIONAL: PROPRIETÁRIO , GARANTIA ON SITE: SUPERIOR A 36 MESES",
            "siglaUnidadeFornecimento": null,
            "nomeUnidadeFornecimento": null,
            "quantidadeItem": 1065,
            "valorUnitarioItem": 7000,
            "valorTotalItem": 7455000,
            "tituloProjetoCompra": "Aquisição computadores e notebooks",
            "descricaoProjetoCompra": null,
            "anoPcaProjetoCompra": 2022,
            "dataInicioProcessoCompra": "2022-09-19T00:00:00",
            "dataFimProcessoCompra": "2022-12-16T00:00:00",
            "duracaoProcessoCompra": 88,
            "numeroItemPncp": 7,
            "statusContratacaoExecucao": null,
            "dataHoraPublicacaoPncp": "2023-05-19T19:19:51.919936",
            "dataHoraAtualizacaoArtefato": "2022-11-22T11:11:19.189",
            "dataHoraAtualizacaoProjetoCompra": "2022-11-25T16:04:23",
            "dataHoraAtualizacaoDfd": "2023-05-19T19:19:52",
            "dataHoraAtualizacaoItem": "2023-05-19T19:19:52.355192"
        }...
```
</details>

---

### 2.1 Consultar Itens por Catálogo (CSV)
Versão do endpoint de catálogo em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/2.1_consultarPgcDetalheCatalogo_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarPgcDetalheCatalogo`.

---

### 3. Consultar Agregação do Plano (Totais)
Serviço que permite consultar os dados de quantidade total de um item e valor total planejado de do plano de contratação de um órgão.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/3_consultarPgcAgregacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `orgao` | Texto | **Sim** | CNPJ do Órgão (sem pontuação). |
| `ano` | Inteiro | **Sim** | Ano do plano (YYYY). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-pgc/3_consultarPgcAgregacao?pagina=1&orgao=05457283000119&ano=2022`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "orgao": "05457283000119",
            "ano": 2022,
            "poder": "E",
            "esfera": "F",
            "dataHoraPublicacaoPncp": "2023-05-20T05:21:14.511956",
            "dataHoraAtualizacao": "2023-05-20T05:21:14.511956",
            "quantidadeTotalItens": 230,
            "valorTotalEstimado": 219821084.64
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0,
    "dataHoraConsulta": "2023-12-08T10:03:29.897689869",
    "timeZoneAtual": "GMT-03:00",
    "obs": "Os valores disponiveis estão sujeitos a alterações"
}
```
</details>

---

### 3.1 Consultar Agregação do Plano (CSV)
Versão do endpoint de agregação em formato CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-pgc/3_consultarPgcAgregacao_CSV`

**Parâmetros:** Os mesmos do endpoint `3_consultarPgcAgregacao`.

***

# Módulo UASG

UASG é a sigla para Unidade Administrativa de Serviços Gerais, uma denominação utilizada no contexto do SISG, que é o Sistema Integrado de Serviços Gerais. As UASGs são, portanto, unidades operacionais dentro de diversos órgãos e entidades do governo federal que executam atividades de serviços gerais. Estas atividades incluem, entre outras coisas, a contratação de serviços, aquisições de materiais, gestão de contratos, administração de patrimônio e outras funções de suporte administrativo.

### 1. Consultar UASG
Serviço que permite consultar dados de uma Uasg.

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-uasg/1_consultarUasg?codigoUasg=200014&statusUasg=1`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 1.1 Consultar UASG (CSV)
Versão do endpoint de consulta de UASG que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/1.1_consultarUasg_CSV`

**Parâmetros:** Os mesmos do endpoint `1_consultarUasg`.

---

### 2. Consultar Órgão
Serviço que permite consultar os dados dos Órgãos pertencentes ao sistema Compras.gov.br.

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-uasg/2_consultarOrgao?codigoOrgao=26000&statusOrgao=true`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

---

### 2.1 Consultar Órgão (CSV)
Versão do endpoint de consulta de Órgão que retorna os dados formatados em CSV.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-uasg/2.1_consultarOrgao_CSV`

**Parâmetros:** Os mesmos do endpoint `2_consultarOrgao`.

***

# Módulo Legado

Possibilita a obtenção de dados sobre as licitações realizadas pelo Governo Federal de acordo com a Lei 8.666/93. Tradicionalmente, os dados das compras públicas podem ser encontrados no site: https://compras.dados.gov.br/docs/home.html. Por isso, o nome deste módulo é "LEGADO", pois os métodos de consulta utilizam a mesma fonte de dados da tradicional API de Compras.

### 1. Consultar Compras com Licitação
Possibilita a obtenção de dados sobre as Licitações realizadas pelo Governo Federal.

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/1_consultarLicitacao?pagina=1&tamanhoPagina=500&uasg=120632&numero_aviso=942023&modalidade=5&data_publicacao_inicial=2023-12-10&data_publicacao_final=2023-12-15&pertence14133=true`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
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
</details>

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
Possibilita a obtenção de dados sobre os itens de licitações realizadas pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/2_consultarItemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `uasg` | Inteiro | Não | Código da UASG. |
| `numero_aviso` | Inteiro | Não | Número do aviso. |
| `modalidade` | Inteiro | **Sim** | Código da modalidade de licitação. |
| `decreto_7174` | Booleano | Não | Filtro para itens vinculados ao Decreto nº 7.174/2010. |
| `codigo_item_material` | Inteiro | Não | Código do item (Material). |
| `codigo_item_servico` | Inteiro | Não | Código do item (Serviço). |
| `cnpj_fornecedor` | Texto | Não | CNPJ do vencedor. |
| `cpfVencedor` | Texto | Não | CPF do vencedor. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/2_consultarItemLicitacao?modalidade=1`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "id_compra": "25500001000181997",
            "id_compra_item": "2550000100018199700001",
            "numero_licitacao": "255000011819971",
            "numero_item_licitacao": 1,
            "uasg": 255000,
            "criterio_julgamento": "Menor Valor",
            "decreto_7174": false,
            "codigo_item_material": null,
            "nome_material": null,
            "codigo_item_servico": 10022,
            "nome_servico": "TRANSCRICAO DE TEXTO",
            "descricao_item": "",
            "unidade": null,
            "quantidade": "1",
            "valor_estimado": 0,
            "sustentavel": null,
            "cnpj_fornecedor": null,
            "cpfVencedor": null,
            "beneficio": "Nao possui tratamento diferenciado para ME/EPP/COOPERATIVA",
            "dt_alteracao": "2025-04-24T15:51:00"
        }...
```
</details>

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
Possibilita a obtenção de dados sobre os pregões realizados pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/3_consultarPregoes`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `co_orgao` | Inteiro | Não | Código do órgão. |
| `numero` | Inteiro | Não | Número do pregão. |
| `ds_tipo_pregao_compra` | Texto | Não | Tipo de compra (ex: SISRP). |
| `dt_data_edital_inicial` | Texto | **Sim** | Data inicial de disponibilização do edital. |
| `dt_data_edital_final` | Texto | **Sim** | Data final de disponibilização do edital. |
| `pertence14133` | Booleano | Não | Indica se pertence à Lei 14.133/2021. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/3_consultarPregoes?pagina=1&tamanhoPagina=10&co_uasg=10001&dt_data_edital_inicial=2019-01-07&dt_data_edital_final=2019-01-17&pertence14133=false`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "id_compra": "01000105000012019",
            "co_processo": "108.846/2017",
            "co_portaria": "152018",
            "co_uasg": 10001,
            "no_ausg": "CAMARA DOS DEPUTADOS",
            "co_orgao": 1000,
            "no_orgao": "CAMARA DOS DEPUTADOS",
            "numero": 12019,
            "ds_situacao_pregao": "homologado",
            "ds_tipo_pregao": "eletronico",
            "ds_tipo_pregao_compra": "SISRP",
            "tx_objeto": "Objeto: Pregão Eletrônico -  Fornecimento, mediante Sistema de Registro de Preços, ...",
            "valorEstimadoTotal": "313226.15",
            "valorHomologadoTotal": "149929.75",
            "dt_portaria": "2018-06-01T03:00:00.000+00:00",
            "dt_data_edital": "2019-01-07",
            "dt_inicio_proposta": "2019-01-07T12:00:00.000+00:00",
            "dt_fim_proposta": "2019-01-17T12:30:00.000+00:00",
            "dt_alteracao": "2025-03-13T14:44:00",
            "dt_encerramento": "2019-01-25",
            "dt_resultado": "2019-02-06",
            "pertence14133": false
        }...
```
</details>

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
Possibilita a obtenção de dados sobre os itens de pregões realizados pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/4_consultarItensPregoes`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `decreto_7174` | Texto | Não | Filtro decreto 7174 (TRUE/FALSE). |
| `fornecedor_vencedor` | Texto | Não | Nome do fornecedor vencedor. |
| `dt_hom_inicial` | Texto | Não | Data de homologação inicial. |
| `dt_hom_final` | Texto | Não | Data de homologação final. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/4_consultarItensPregoes?dt_hom_inicial=2023-01-01&dt_hom_final=2023-01-10`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "id_compra": "11000105000832022",
            "id_compra_item": "1100010500083202200001",
            "decreto_7174": "FALSE",
            "situacao_item": "homologado",
            "descricao_item": "Prestação de Serviços de Portaria / Recepção",
            "descricao_detalhada_item": "Serviços de recepção e atendimento ao público - 01 Posto de Supervisor de Recepcionista.",
            "margem_preferencial": "FALSE",
            "tratamento_diferenciado": null,
            "quantidade_item": "1",
            "unidade_fornecimento": "UNIDADE",
            "valor_estimado_item": "83841.57",
            "menor_lance": "72900.00",
            "valor_negociado": null,
            "valorHomologadoItem": "72900.00",
            "fornecedor_vencedor": null,
            "no_adjudic": "GUILHERME PAIVA SILVA",
            "no_hom": "MAURILIO COSTA DOS SANTOS",
            "dt_encerramento": "2023-01-06",
            "dt_adjudic": "2023-01-09",
            "dt_hom": "2023-01-09",
            "dt_alteracao": "2025-03-05T17:37:00"
        }...
```
</details>

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
Possibilita a obtenção de dados sobre as compras sem licitação realizadas pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/5_consultarComprasSemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `dt_ano_aviso` | Inteiro | **Sim** | Ano da compra. |
| `nu_aviso_licitacao` | Inteiro | Não | Número da dispensa/inexigibilidade. |
| `co_modalidade_licitacao` | Inteiro | Não | Código da modalidade. |
| `co_orgao` | Texto | Não | Código do órgão. |
| `co_orgao_superior` | Texto | Não | Órgão Superior. |
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `dtDeclaracaoDispensaInicial` | Texto | Não | Data inicial referente ao reconhecimento da compra feita sem licitação |
| `dtDeclaracaoDispensaFinal` | Texto | Não | Data final referente ao reconhecimento da compra feita sem licitação |
| `dtRatificacao` | Texto | Não | Data referente à ratificação da compra feita sem licitação. |
| `dtPublicacao` | Texto | Não | Data referente à publicação da compra feita sem licitação. |
| `pertence14133` | Booleano | Não | Indica se pertence à Lei 14.133/2021. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/5_consultarComprasSemLicitacao?pagina=1&tamanhoPagina=500&dt_ano_aviso=2023&co_orgao=30907&co_uasg=200602`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "20060206000012023",
            "co_orgao": "30907",
            "co_orgao_superior": "30000",
            "co_uasg": 200602,
            "no_ausg": "PENITENCIÁRIA FEDERAL EM MOSSORO - RN",
            "co_modalidade_licitacao": 6,
            "ds_lei": null,
            "nu_processo": "08019.007217/2022",
            "qt_total_item": 3,
            "vr_estimado": 33723.78,
            "nu_aviso_licitacao": 1,
            "ds_objeto_licitacao": "Objeto: Trata-se da aquisição de prestação de serviços continuados de Limpeza e Conservação, ..."
            "ds_fundamento_legal": "Fundamento Legal: Art. 75º, Inciso II da Lei nº 14.133 de 1º/04/2021.",
            "ds_justificativa": "Justificativa: Autorização para Abertura de Procedimento Licitatório (SEI nº 20397081) E Despacho 1707 (SEI nº 20452544) E Despacho 299",
            "no_responsavel_decl_disp": "",
            "no_cargo_resp_decl_disp": "",
            "no_responsavel_ratificacao": "",
            "no_cargo_resp_ratificacao": "",
            "dtDeclaracaoDispensa": null,
            "dtRatificacao": null,
            "dtPublicacao": null,
            "dt_ano_aviso": 2023,
            "dt_alteracao": "2023-01-02",
            "pertence14133": true
        }...
```
</details>

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
Possibilita a obtenção de dados sobre os itens de compra sem licitação realizadas pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/6_consultarCompraItensSemLicitacao`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10).|
| `co_uasg` | Inteiro | Não | Código da UASG. |
| `co_orgao` | Texto | Não | Código do órgão. |
| `dt_ano_aviso_licitacao` | Inteiro | **Sim** | Ano da compra. |
| `co_modalidade_licitacao` | Inteiro | Não | Código da modalidade. |
| `co_conjunto_materiais` | Inteiro | Não | Código do material. |
| `co_servico` | Inteiro | Não | Código do serviço. |
| `nu_cpf_cnpj_fornecedor` | Texto | Não | Número do CNPJ/CPF do fornecedor. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/6_consultarCompraItensSemLicitacao?co_uasg=170133&dt_ano_aviso_licitacao=2023`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "17013306000082023",
            "idCompraItem": "1701330600008202300001",
            "co_uasg": 170133,
            "co_modalidade_licitacao": 6,
            "no_modalidade_licitacao": "Dispensa",
            "nu_aviso_licitacao": 8,
            "dt_ano_aviso_licitacao": 2023,
            "nu_inciso": "02",
            "nu_processo": "10752720014202307",
            "vr_estimado": 15640.66,
            "qt_total_item": 1,
            "ds_objeto_licitacao": "Objeto: Contratação de serviço de instalação e montagem de blindagem acústica nas salas do 21º pavimento do  Edifício situado à Avenida Prestes Maia nº 733, Centro, São Paulo/SP.",
            "ds_fundamento_legal": "Fundamento Legal: Art. 24º, Inciso II da Lei nº 8.666 de 21º/06/1993.",
            "ds_justificativa": "Justificativa: Dispensa de licitação por baixo valor.",
            "nu_cpf_resp_decl_disp": null,
            "nu_cpf_resp_ratificacao": null,
            "nu_cpf_resp_publicacao": null,
            "no_responsavel_decl_disp": "ADEMIR ANTONIO SCHONS",
            "no_cargo_resp_decl_disp": "Chefe Dipol/srrf08",
            "no_responsavel_ratificacao": "",
            "no_cargo_resp_ratificacao": "",
            "nu_item_material": 1,
            "in_material_servico": "servico",
            "co_conjunto_materiais": 0,
            "no_conjunto_materiais": null,
            "co_servico": 1627,
            "no_servico": "MANUTENCAO / REFORMA PREDIAL",
            "ds_detalhada": "Manutenção / reforma predial (Contratação de serviço de instalação e montagem  de blindagem acústica nas salas do 21º pavimento do Edifício situado à Avenida  Prestes Maia nº 733, Centro, São Paulo/SP).",
            "qt_material_alt": 1,
            "no_unidade_medida": "UNIDADE",
            "vr_estimado_item": 15640.66,
            "ds_fabricante": null,
            "no_marca_material": "",
            "in_tipo_fornecedor_vencedor": "PJ",
            "nu_cnpj_vencedor": "28484808000100",
            "nu_cpf_vencedor": null,
            "no_fornecedor_vencedor": "BURTONTEC ENERGIA E CONSTRUCOES LTDA",
            "dt_alteracao": "2024-07-17T11:24:00"
        }...
```
</details>

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
Possibilita a obtenção de dados sobre licitações do tipo RDC realizadas pelo Governo Federal.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-legado/7_consultarRdc`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `data_publicacao_max` | Texto | **Sim** | Data máxima da publicação. |
| `data_publicacao_min` | Texto | **Sim** | Data mínima da publicação. |
| `endereco_entrega_edital` | Texto | Não | Endereço de entrega do edital. |
| `forma_de_realizacao` | Inteiro | Não | Presencial ou Eletrônico. |
| `modalidade` | Inteiro | Não | Código da modalidade. |
| `nome_responsavel` | Texto | Não | Nome do Responsável pela Licitação. |
| `numero_aviso` | Inteiro | Não | Número do Aviso da Licitação. |
| `objeto` | Texto | Não | Objeto da Licitação. |
| `orgao` | Inteiro | Não | Órgão ao qual pertence a UASG da licitação. |
| `situacao_aviso` | Texto | Não | Situação do aviso. |
| `uasg` | Inteiro | Não | Código da UASG. |
| `uf_uasg` | Texto | Não | Unidade Federativa da UASG. |
| `valor_estimado_total_max` | Numero | Não | Valor máximo da soma dos valores estimados dos itens da licitação. |
| `valor_estimado_total_min` | Numero | Não | Valor mínimo da soma dos valores estimados dos itens da licitação. |
| `valor_homologado_total_max` | Numero | Não | Valor máximo da soma dos valores homologados dos itens da licitação. |
| `valor_homologado_total_min` | Numero | Não | Valor mínimo da soma dos valores homologados dos itens da licitação. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-legado/7_consultarRdc?data_publicacao_max=2019-03-01&data_publicacao_min=2019-01-01`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "data_abertura_proposta": "2019-01-29T12:00:00.000+00:00",
            "data_entrega_edital": "2019-01-08T11:00:00.000+00:00",
            "data_entrega_proposta": "2019-01-08T11:00:00.000+00:00",
            "data_publicacao": "2019-01-08",
            "endereco_entrega_edital": "Avenida Brasil, 4365 - Manguinhos - Manguinhos/RJ",
            "forma_de_realizacao_licitacao": "eletronico",
            "funcao_responsavel": "Presidente da Comissão",
            "identificador": "2544459922012019",
            "informacoes_gerais": null,
            "modalidade": 99,
            "nome_responsavel": "FLAVIO ISIDORO DA SILVA",
            "numero_aviso": 22012019,
            "numero_itens": 1,
            "numero_processo": "25386100762201896",
            "objeto": "Obra para adequação civil com finalidad e à instalação de linha de envase Groninger do Centro de Processamento Final de Imunobiológico sCPFI de Bio-Manguinhos.",
            "situacao_aviso": "Publicado",
            "tipo_recurso": "Nacional",
            "uasg": 254445,
            "orgao_uasg": 36201,
            "uf_uasg": "RJ"
        }...
```
</details>

***

# Módulo Contratações (PNCP)

Este módulo oferece acesso a informações sobre os procedimentos de contratação dos órgãos públicos, em conformidade com a legislação vigente (incluindo a Lei nº 14.133/2021). É possível consultar dados desde a abertura do processo de contratação até os resultados de cada item, garantindo transparência e facilitando o monitoramento das aquisições governamentais.

### 1. Consultar Contratações (Lei 14.133/21)
Serviço que permite acessar informações detalhadas sobre contratações realizadas com base na Lei 14.133/2021.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/1_consultarContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados.|
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade do órgão. |
| `dataPublicacaoPncpInicial` | Texto | **Sim** | Data inicial da publicação no PNCP (YYYY-MM-DD). |
| `dataPublicacaoPncpFinal` | Texto | **Sim** | Data final da publicação no PNCP (YYYY-MM-DD). |
| `codigoModalidade` | Inteiro | **Sim** | Código da modalidade da licitação (ex: 5 - Pregão). |
| `unidadeOrgaoCodigoIbge` | Inteiro | Não | Código do IBGE da unidade. |
| `unidadeOrgaoUfSigla` | Texto | Não | Sigla da UF. |
| `dataAualizacaoPncp` | Texto | Não | Data de atualização no PNCP. |
| `amparoLegalCodigoPncp` | Inteiro | Não | Código do amparo legal específico no PNCP. |
| `contratacaoExcluida` | Booleano | Não | Indica se a contratação foi excluída. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratacoes/1_consultarContratacoes_PNCP_14133?pagina=1&tamanhoPagina=10&dataPublicacaoPncpInicial=2024-01-01&dataPublicacaoPncpFinal=2024-12-31&codigoModalidade=5&amparoLegalCodigoPncp=1&contratacaoExcluida=false`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "92501005000292023",
            "numeroControlePNCP": "18715615000160-1-001376/2023",
            "anoCompraPncp": 2023,
            "sequencialCompraPncp": 1376,
            "orgaoEntidadeCnpj": "18715615000160",
            "orgaoSubrogadoCnpj": null,
            "codigoOrgao": 71507,
            "orgaoEntidadeRazaoSocial": "ESTADO DE MINAS GERAIS",
            "orgaoSubrogadoRazaoSocial": null,
            "orgaoEntidadeEsferaId": "E",
            "orgaoSubrogadoEsferaId": null,
            "orgaoEntidadePoderId": "E",
            "orgaoSubrogadoPoderId": null,
            "unidadeOrgaoCodigoUnidade": "925010",
            "unidadeSubrogadaCodigoUnidade": null,
            "unidadeOrgaoNomeUnidade": "CAMARA MUNICIPAL DE UBERLÂNDIA - MG",
            "unidadeSubrogadaNomeUnidade": null,
            "unidadeOrgaoUfSigla": "MG",
            "unidadeSubrogadaUfSigla": null,
            "unidadeOrgaoMunicipioNome": "UBERLÂNDIA",
            "unidade_subrogada_municipio_nome": null,
            "unidadeOrgaoCodigoIbge": 3170206,
            "unidadeSubrogadaCodigoIbge": null,
            "numeroCompra": "00029",
            "modalidadeIdPncp": 6,
            "codigoModalidade": 5,
            "modalidadeNome": "Pregão - Eletrônico",
            "srp": false,
            "modoDisputaIdPncp": 3,
            "codigoModoDisputa": 3,
            "amparoLegalCodigoPncp": 1,
            "amparoLegalNome": "Lei 14.133/2021, Art. 28, I",
            "amparoLegalDescricao": "pregão: modalidade de licitação obrigatória para aquisição de bens e serviços comuns",
            "informacaoComplementar": "ATENÇÃO! Seguir as descrições detalhadas dos itens, marcas e modelos de referência sugeridos pela Câmara, ...",
            "processo": "56",
            "objetoCompra": "Contratação de empresa para fornecimento de equipamento e treinamento para implantação de sistema de áudio e vídeo para o Plenário Homero Santos.",
            "existeResultado": true,
            "orcamentoSigilosoCodigo": 1,
            "orcamentoSigilosoDescricao": "Compra sem sigilo",
            "situacaoCompraIdPncp": 1,
            "situacaoCompraNomePncp": "Divulgada no PNCP",
            "tipoInstrumentoConvocatorioCodigoPncp": 1,
            "tipoInstrumentoConvocatorioNome": "Edital",
            "modoDisputaNomePncp": "Aberto-Fechado",
            "valorTotalEstimado": 0,
            "valorTotalHomologado": 143655,
            "dataInclusaoPncp": "2024-01-15T07:03:38",
            "dataAualizacaoPncp": "2024-01-15T07:03:38",
            "dataPublicacaoPncp": "2024-01-15T07:03:38",
            "dataAberturaPropostaPncp": "2024-01-15T08:00:00",
            "dataEncerramentoPropostaPncp": "2024-01-29T13:30:00",
            "contratacaoExcluida": false
        }...
```
</details>

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
Serviço que oferece acesso aos dados específicos de itens vinculados às contratações regidas pela Lei 14.133/2021.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/2_consultarItensContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade. |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `situacaoCompraItem` | Texto | Não | Situação do item (ex: 4 - Deserto). |
| `materialOuServico` | Texto | Não | `M` - Material ou `S` - Serviço. |
| `codigoClasse` | Inteiro | Não | Código da classe. |
| `codigoGrupo` | Inteiro | Não | Código do Grupo |
| `codItemCatalogo` | Inteiro | Não | Código do Item no Catálogo. |
| `temResultado` | Booleano | Não | Informa se tem resultado (`true`/`false`). |
| `codFornecedor` | Texto | Não | Código do Fornecedor |
| `dataInclusaoPncpInicial` | Texto | **Sim** | Data de Inclusão Inicial no PNCP (YYYY-MM-DD). |
| `dataInclusaoPncpFinal` | Texto | **Sim** | Data de Inclusão Final no PNCP (YYYY-MM-DD). |
| `dataAtualizacaoPncp` | Texto | Não | Data de atualização no PNCP. |
| `bps` | Booleano | Não| Indica se a compra segue as Boas Práticas de Suprimentos (BPS).  |
| `margemPreferenciaNormal` | Booleano | Não | Indica se a compra possui margem de preferência normal conforme a legislação vigente. |
| `codigoNCM` | Texto | Não | Código de NCM - Nomenclatura Comum do Mercosul. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratacoes/2_consultarItensContratacoes_PNCP_14133?pagina=1&tamanhoPagina=10&unidadeOrgaoCodigoUnidade=200350&orgaoEntidadeCnpj=00394494000136&situacaoCompraItem=4&materialOuServico=M&codigoClasse=6510&codItemCatalogo=279727&dataInclusaoPncpInicial=2023-10-01&dataInclusaoPncpFinal=2023-10-01&dataAtualizacaoPncp=2023-10-01`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompra": "20035006000162023",
            "idCompraItem": "2003500600016202300038",
            "idContratacaoPNCP": "00394494000136-1-000602/2023",
            "unidadeOrgaoCodigoUnidade": 200350,
            "orgaoEntidadeCnpj": "00394494000136",
            "numeroItemPncp": 38,
            "numeroItemCompra": 38,
            "numeroGrupo": 0,
            "descricaoResumida": "Algodão",
            "materialOuServico": "M",
            "materialOuServicoNome": "Material",
            "codigoClasse": 6510,
            "codigoGrupo": null,
            "codItemCatalogo": 279727,
            "descricaodetalhada": "Algodão Tipo: Hidrófilo , Apresentação: Em Bolas , Material: Alvejado, Purificado, Isento De Impurezas , Esterilidade: Não Estéril",
            "unidadeMedida": "Embalagem 500 G",
            "orcamentoSigiloso": false,
            "itemCategoriaIdPncp": 3,
            "itemCategoriaNome": "Informática (TIC)",
            "criterioJulgamentoIdPncp": 1,
            "criterioJulgamentoNome": "Menor preço",
            "situacaoCompraItem": "4",
            "situacaoCompraItemNome": "Deserto",
            "tipoBeneficio": "1",
            "tipoBeneficioNome": "Participação exclusiva para ME/EPP",
            "incentivoProdutivoBasico": false,
            "quantidade": 5,
            "valorUnitarioEstimado": 18.56,
            "valorTotal": 92.8,
            "temResultado": null,
            "codFornecedor": null,
            "nomeFornecedor": null,
            "quantidadeResultado": null,
            "valorUnitarioResultado": null,
            "valorTotalResultado": null,
            "dataInclusaoPncp": "2023-10-01T19:16:04",
            "dataAtualizacaoPncp": "2023-10-05T10:00:16",
            "dataResultado": null,
            "margemPreferenciaNormal": false,
            "percentualMargemPreferenciaNormal": null,
            "margemPreferenciaAdicional": false,
            "percentualMargemPreferenciaAdicional": null,
            "codigoNCM": null,
            "descricaoNCM": null
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0
}
```
</details>

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
Serviço que permite consultar os resultados associados aos itens contratados, incluindo detalhes de desempenho e conformidade com a Lei 14.133/2021.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratacoes/3_consultarResultadoItensContratacoes_PNCP_14133`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `unidadeOrgaoCodigoUnidade` | Texto | Não | Código da unidade do órgão. |
| `nifFornecedor` | Texto | Não | CPF/CNPJ do fornecedor. |
| `codigoPais` | Texto | Não | Código do país do fornecedor. |
| `porteFornecedorId` | Inteiro | Não | Identificador do porte do fornecedor. |
| `naturezaJuridicaId` | Texto | Não | Código que identifica a natureza jurídica do fornecedor. |
| `situacaoCompraItemResultadoId` | Inteiro | Não | Identificador da situação do item na compra. |
| `valorUnitarioHomologadoInicial` | Numero | Não | Valor unitário inicial homologado para o item. |
| `valorUnitarioHomologadoFinal` | Numero | Não | Valor unitário final homologado para o item. |
| `valorTotalHomologadoInicial` | Numero | Não | Valor total inicial homologado para o item. |
| `valorTotalHomologadoFinal` | Numero | Não | Valor total final homologado para o item. |
| `dataResultadoPncpInicial` | Texto | **Sim** | Data inicial do resultado no PNCP. |
| `dataResultadoPncpFinal` | Texto | **Sim** | Data final do resultado no PNCP. |
| `aplicacaoMargemPreferencia` | Booleano | Não | Se houve margem de preferência. |
| `aplicacaoBeneficioMeepp` | Booleano | Não | Se houve benefício ME/EPP. |
| `aplicacaoCriterioDesempate` | Booleano | Não | Indica se foi aplicado algum critério de desempate conforme a legislação. |
| `orgaoEntidadeCnpj` | Texto | Não | CNPJ da entidade do órgão. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratacoes/3_consultarResultadoItensContratacoes_PNCP_14133?pagina=1&tamanhoPagina=10&unidadeOrgaoCodigoUnidade=155124&nifFornecedor=28546470000174&dataResultadoPncpInicial=2024-11-01&dataResultadoPncpFinal=2024-11-30&aplicacaoMargemPreferencia=false`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "idCompraItem": "1551240590076202400012",
            "idCompra": "15512405900762024",
            "idContratacaoPNCP": "15126437000143-1-002766/2024",
            "unidadeOrgaoCodigoUnidade": "155124",
            "numeroItemPncp": 12,
            "sequencialResultado": 1,
            "niFornecedor": "28546470000174",
            "tipoPessoa": "PJ",
            "nomeRazaoSocialFornecedor": "SOUZA MED COMERCIO DE MATERIAIS MEDICO-HOSPITALAR LTDA",
            "codigoPais": "BRA",
            "indicadorSubcontratacao": false,
            "ordemClassificacaoSrp": 1,
            "quantidadeHomologada": 300,
            "valorUnitarioHomologado": 13.55,
            "valorTotalHomologado": 4065,
            "percentualDesconto": 0,
            "situacaoCompraItemResultadoId": 1,
            "situacaoCompraItemResultadoNome": "Informado",
            "motivoCancelamento": null,
            "porteFornecedorId": 1,
            "porteFornecedorNome": "ME",
            "naturezaJuridicaNome": "Sociedade Empresária Limitada",
            "naturezaJuridicaId": "2062",
            "dataInclusaoPncp": "2024-11-01T14:23:56",
            "dataAtualizacaoPncp": "2024-11-01T14:23:56",
            "dataCancelamentoPncp": null,
            "dataResultadoPncp": "2024-11-01T00:00:00",
            "aplicacaoMargemPreferencia": false,
            "amparoLegalMargemPreferenciaId": null,
            "amparoLegalMargemPreferenciaNome": null,
            "aplicacaoBeneficioMeepp": false,
            "aplicacaoCriterioDesempate": false,
            "amparoLegalCriterioDesempateId": null,
            "amparoLegalCriterioDesempateNome": null,
            "moedaEstrangeiraId": null,
            "dataCotacaoMoedaEstrangeira": null,
            "valorNominalMoedaEstrangeira": null,
            "paisOrigemProdutoServicoId": null,
            "timezoneCotacaoMoedaEstrangeira": null
        }...
```
</details>

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

As Atas de Registro de Preços (ARP) são documentos que estabelecem condições e quantidades para futuras aquisições de bens e serviços. Por meio deste módulo, obtêm-se detalhes das ARPs vigentes e de suas especificidades, o que facilita o planejamento, a gestão e o monitoramento das compras, contribuindo para maior eficiência e economicidade no uso dos recursos públicos.

### 1. Consultar ARP
Consulta as Atas de Registro de Preços vigentes ou cadastradas, listando informações como número da ata, objeto, órgão gerenciador e período de validade.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/1_consultarARP`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `codigoUnidadeGerenciadora` | Texto | Não | Código da unidade responsável pela ata. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade de compra. |
| `numeroAtaRegistroPreco` | Texto | Não | Número da Ata de Registro de Preço. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data mínima de início da vigência (YYYY-MM-DD). |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data máxima de início da vigência (YYYY-MM-DD). |
| `dataAssinaturaInicial` | Texto | Não | Data inicial da assinatura. |
| `dataAssinaturaFinal` | Texto | Não | Data final da assinatura. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-arp/1_consultarARP?pagina=1&tamanhoPagina=10&codigoUnidadeGerenciadora=160482&numeroAtaRegistroPreco=00044/2023&dataVigenciaInicial=2023-12-22&dataVigenciaFinal=2024-12-22`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "numeroAtaRegistroPreco": "00044/2023",
            "codigoUnidadeGerenciadora": 160482,
            "nomeUnidadeGerenciadora": "COMANDO/1A BRIGADA DE INFANTARIA DE SELVA",
            "codigoOrgao": 52121,
            "nomeOrgao": "COMANDO DO EXERCITO",
            "linkAtaPNCP": "https://pncp.gov.br/app/atas/00394452000103/2023/11760/10",
            "linkCompraPNCP": "https://pncp.gov.br/app/editais/00394452000103/2023/011760",
            "numeroCompra": "00031",
            "anoCompra": "2023",
            "codigoModalidadeCompra": "5",
            "nomeModalidadeCompra": "Pregão",
            "dataAssinatura": "2023-12-19T00:00:00",
            "dataVigenciaInicial": "2023-12-22T00:00:00",
            "dataVigenciaFinal": "2024-12-22T00:00:00",
            "valorTotal": 230075.8,
            "statusAta": "Ativo",
            "objeto": "Futura e eventual aquisição de medicamentos visando atender as necessidades do Posto Médico\r\nde Guarnição de Boa Vista e OM´s vinculadas ao Comando da 1ª Bda Inf Sl.",
            "quantidadeItens": 22,
            "dataHoraAtualizacao": "2023-12-22T12:18:12",
            "dataHoraInclusao": "2023-12-22T12:18:10",
            "dataHoraExclusao": null,
            "ataExcluido": false,
            "numeroControlePncpAta": "00394452000103-1-011760/2023-000010",
            "numeroControlePncpCompra": "00394452000103-1-011760/2023",
            "idCompra": "16048205000312023"
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0
}
```
</details>

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
| `pagina` | Inteiro | Não | Paginação dos resultados (Padrão: 1). |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página (Padrão: 10). |
| `codigoUnidadeGerenciadora` | Texto | Não | Código da unidade responsável pela ata. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade de compra. |
| `numeroAtaRegistroPreco` | Texto | Não | Número da Ata. |
| `dataVigenciaFinalMin` | Texto | **Sim** | Data mínima do fim da vigência. |
| `dataVigenciaFinalMax` | Texto | **Sim** | Data máxima do fim da vigência. |
| `dataAssinaturaInicial` | Texto | Não | Data inicial da assinatura. |
| `dataAssinaturaFinal` | Texto | Não | Data final da assinatura. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-arp/1.2_consultarARP_FimVigencia?pagina=1&tamanhoPagina=10&codigoUnidadeGerenciadora=194008&codigoModalidadeCompra=05&numeroAtaRegistroPreco=00014%2F2023&dataVigenciaFinalMin=2025-01-01&dataVigenciaFinalMax=2025-01-31&dataAssinaturaInicial=2024-01-01&dataAssinaturaFinal=2025-01-01`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "numeroAtaRegistroPreco": "00014/2023",
            "codigoUnidadeGerenciadora": "194008",
            "nomeUnidadeGerenciadora": "COORDENACAO REGIONAL DO RIO NEGRO/AM",
            "codigoOrgao": 30202,
            "nomeOrgao": "FUNDACAO NACIONAL DOS POVOS INDIGENAS",
            "linkAtaPNCP": "https://pncp.gov.br/app/atas/00059311000126/2023/385/33",
            "linkCompraPNCP": "https://pncp.gov.br/app/editais/00059311000126/2023/000385",
            "numeroCompra": "00002",
            "anoCompra": "2023",
            "codigoModalidadeCompra": "05",
            "nomeModalidadeCompra": "Pregão",
            "dataAssinatura": "2024-01-23T00:00:00",
            "dataVigenciaInicial": "2024-01-24",
            "dataVigenciaFinal": "2025-01-24",
            "valorTotal": 221700.00000000,
            "statusAta": "Ata de Registro de Preços",
            "objeto": "Registro de preços para a eventual aquisição de materiais diversos, ...",
            "quantidadeItens": 3,
            "dataHoraAtualizacao": "2024-01-23T09:38:10",
            "dataHoraInclusao": "2023-12-06T16:34:24",
            "dataHoraExclusao": null,
            "ataExcluido": false,
            "numeroControlePncpAta": "00059311000126-1-000385/2023-000033",
            "numeroControlePncpCompra": "00059311000126-1-000385/2023",
            "idCompra": "19400805000022023"
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0
}
```
</details>

---

### 2. Consultar Item da ARP
Retorna a lista de itens associados a uma ARP, incluindo descrição, quantidades registradas e condições de fornecimento.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/2_consultarARPItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `codigoUnidadeGerenciadora` | Texto | Não | Código da unidade responsável pela ata. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade da compra. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data mínima de início da vigência. |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data máxima de início da vigência. |
| `dataAssinaturaInicial` | Texto | Não | Data inicial da assinatura. |
| `dataAssinaturaFinal` | Texto | Não | Data final da assinatura. |
| `numeroItem` | Texto | Não | Número do item na ata. |
| `codigoItem` | Inteiro | Não | Código do item (material/serviço). |
| `tipoItem` | Texto | Não | Tipo do item (M - Material / S - Serviço). |
| `niFornecedor` | Texto | Não | CNPJ/CPF do fornecedor. |
| `codigoPdm` | Inteiro | Não | Código do PDM (Padrão Descritivo de Materiais). |
| `numeroCompra` | Texto | Não | Número da compra. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-arp/2_consultarARPItem?dataVigenciaInicial=2023-06-08&dataVigenciaFinal=2024-06-08&numeroItem=00074&codigoItem=243008`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "numeroAtaRegistroPreco": "00013/2023",
            "codigoUnidadeGerenciadora": 160426,
            "numeroCompra": "00002",
            "anoCompra": "2023",
            "codigoModalidadeCompra": "5",
            "dataAssinatura": "2023-12-05T00:00:00",
            "dataVigenciaInicial": "2024-01-04T00:00:00",
            "dataVigenciaFinal": "2024-01-05T00:00:00",
            "numeroItem": "00074",
            "codigoItem": 243008,
            "descricaoItem": "TAÇA, MATERIAL VIDRO TRANSPARENTE INCOLOR, ALTURA 14,20 CM, DIÂMETRO 6,90 CM, CAPACIDADE 181 ML, USO VINHO BRANCO",
            "tipoItem": null,
            "quantidadeHomologadaItem": 132,
            "classificacaoFornecedor": "001",
            "niFornecedor": "41465151000100",
            "nomeRazaoSocialFornecedor": "GIOVANI LOS",
            "quantidadeHomologadaVencedor": 132,
            "valorUnitario": 7.22,
            "valorTotal": 2084.28,
            "maximoAdesao": 264,
            "nomeUnidadeGerenciadora": "DEPOSITO DE SUBSISTENCIA SANTO ANGELO",
            "nomeModalidadeCompra": "Pregão",
            "idCompra": "16042605000022023",
            "numeroControlePncpCompra": "00394452000103-1-012499/2023",
            "dataHoraInclusao": "2024-01-03T11:10:51",
            "dataHoraAtualizacao": "2024-01-03T11:10:51",
            "quantidadeEmpenhada": 0,
            "percentualMaiorDesconto": 0,
            "situacaoSicaf": "1",
            "dataHoraExclusao": null,
            "itemExcluido": false,
            "numeroControlePncpAta": "00394452000103-1-012499/2023-000016",
            "codigoPdm": null,
            "nomePdm": null
        }...
```
</details>

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

---

### 3. Consultar Unidades do Item
Serviço que permite consultar os dados das unidades participantes e saldos de um item específico de uma Ata de Registro de Preços.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/3_consultarUnidadesItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Texto | **Sim** | Código da unidade gerenciadora. |
| `numeroItem` | Texto | **Sim** | Número do item na ata. |
| `dataAtualizacao` | Texto | Não | Data da atualização. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-arp/3_consultarUnidadesItem?pagina=<integer>&tamanhoPagina=<integer>&numeroAta=<string>&unidadeGerenciadora=<string>&numeroItem=<string>&dataAtualizacao=<string>`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
  "resultado": [
    {
      "srk_ft_arp_item_unidade": 0,
      "numeroAta": "string",
      "unidadeGerenciadora": "string",
      "numeroItem": "string",
      "codigoPdm": "string",
      "descricaoItem": "string",
      "fornecedor": "string",
      "quantidadeRegistrada": 0,
      "saldoAdesoes": 0,
      "saldoRemanejamentoEmpenho": 0,
      "qtdLimiteAdesao": 0,
      "qtdLimiteInformadoCompra": 0,
      "aceitaAdesao": true,
      "dataHoraInclusao": "2026-01-21T13:11:04.860Z",
      "dataHoraAtualizacao": "2026-01-21T13:11:04.860Z",
      "dataHoraExclusao": "2026-01-21T13:11:04.860Z"
    }
  ],
  "totalRegistros": 0,
  "totalPaginas": 0,
  "paginasRestantes": 0
}
```
</details>

---

### 4. Consultar Empenhos e Saldo do Item
Serviço que permite consultar os saldos e quantidades empenhadas de um item em uma Ata de Registro de Preços.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/4_consultarEmpenhosSaldoItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Texto | **Sim** | Código da unidade gerenciadora. |
| `dataAtualizacao` | Texto | Não | Data da atualização. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-arp/4_consultarEmpenhosSaldoItem?pagina=<integer>&tamanhoPagina=<integer>&numeroAta=<string>&unidadeGerenciadora=<string>&dataAtualizacao=<striing>`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
  "resultado": [
    {
      "numeroItem": "string",
      "unidade": "string",
      "tipo": "string",
      "quantidadeRegistrada": 0,
      "quantidadeEmpenhada": 0,
      "saldoEmpenho": 0,
      "dataHoraInclusao": "2026-01-20T12:14:52.989Z",
      "dataHoraAtualizacao": "2026-01-20T12:14:52.990Z"
    }
  ],
  "totalRegistros": 0,
  "totalPaginas": 0,
  "paginasRestantes": 0
}
```
</details>

---

### 5. Consultar Adesões do Item
Serviço que permite consultar as adesões realizadas (caronas) a um item específico de
uma Ata de Registro de Preços.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-arp/5_consultarAdesoesItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `numeroAta` | Texto | **Sim** | Número da Ata de Registro de Preços. |
| `unidadeGerenciadora` | Texto | **Sim** | Código da unidade gerenciadora. |
| `numeroItem` | Texto | **Sim** | Número do item. |
| `unidade` | Texto | Não | Código da unidade aderente. |
| `dataAtualizacao` | Texto | Não | Data da atualização. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-material/1_consultarGrupoMaterial?codigoGrupo=16`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
  "resultado": [
    {
      "numeroAta": "string",
      "unidadeGerenciadora": "string",
      "unidadeNaoParticipante": "string",
      "dataAprovacaoAnalise": "2026-01-20T12:22:06.105Z",
      "quantidadeAprovadaAdesao": 1073741824
    }
  ],
  "totalRegistros": 0,
  "totalPaginas": 0,
  "paginasRestantes": 0
}
```
</details>

***

# Módulo Contratos

Reúne dados referentes aos contratos firmados no âmbito público, abrangendo informações como objeto, valor, prazo de vigência e partes envolvidas. Este módulo permite acompanhar a execução contratual, promovendo maior transparência e possibilitando o controle efetivo das obrigações estabelecidas entre órgãos governamentais e fornecedores.

### 1. Consultar Contratos
Retorna um conjunto de contratos registrados, incluindo dados como número do contrato, objeto, vigência e órgãos participantes.

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
| `codigoUnidadeRealizadoraCompra` | Texto | Não | Código da UG que realizou a compra. |
| `numeroContrato` | Texto | Não | Número do contrato. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade de compra. |
| `codigoTipo` | Inteiro | Não | Código do tipo de contrato. |
| `codigoCategoria` | Inteiro | Não | Código da categoria do contrato. |
| `niFornecedor` | Texto | Não | CPF/CNPJ do fornecedor. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data inicial mínima da vigência (YYYY-MM-DD). |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data inicial máxima da vigência (YYYY-MM-DD). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratos/1_consultarContratos?pagina=1&tamanhoPagina=10&codigoOrgao=99537&codigoUnidadeGestora=110161&codigoUnidadeGestoraOrigemContrato=926403&codigoTipo=99&codigoCategoria=60&dataVigenciaInicialMin=2023-07-06&dataVigenciaInicialMax=2023-12-31`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "codigoOrgao": 99537,
            "nomeOrgao": "PMSP - SUBPREFEITURA SAPOPEMBA",
            "codigoUnidadeGestora": 110161,
            "nomeUnidadeGestora": "SUPERINTENDENCIA REG. DE ADMIN. DA 1ª REGIAO",
            "codigoUnidadeGestoraOrigemContrato": 926403,
            "nomeUnidadeGestoraOrigemContrato": "PMSP - SUBPREFEITURA DE SAPOPEMBA",
            "receitaDespesa": "D",
            "numeroContrato": "2023NE053456",
            "codigoUnidadeRealizadoraCompra": 926403,
            "nomeUnidadeRealizadoraCompra": "PMSP - SUBPREFEITURA DE SAPOPEMBA",
            "numeroCompra": "00006/2023",
            "codigoModalidadeCompra": "6",
            "nomeModalidadeCompra": "Dispensa",
            "codigoUnidadeRequisitante": 926403,
            "nomeUnidadeRequisitante": "PMSP - SUBPREFEITURA DE SAPOPEMBA",
            "codigoTipo": 99,
            "nomeTipo": "Empenho",
            "codigoCategoria": 60,
            "nomeCategoria": "Compras",
            "codigoSubcategoria": null,
            "nomeSubcategoria": null,
            "niFornecedor": "46051880000126",
            "nomeRazaoSocialFornecedor": "FB MULTI NEGOCIOS LTDA",
            "processo": "6061.2023/0000600-2",
            "objeto": "LAGE EM CONCRETO  ARMADO PARA BOCA DE LOBO.",
            "informacoesComplementares": "LAJE EM CONCRETO ARAMDO PARA BOCA DE LOBO.",
            "dataVigenciaInicial": "2023-08-28T00:00:00",
            "dataVigenciaFinal": "2023-08-28T00:00:00",
            "valorGlobal": 16315,
            "numeroParcelas": 1,
            "valorParcela": 16315,
            "valorAcumulado": 16315,
            "totalDespesasAcessorias": null,
            "dataHoraInclusao": "2024-07-30T14:18:14",
            "numeroControlePncpContrato": "05546795000151-2-000140/2023",
            "idCompra": "92640306000002023",
            "dataHoraExclusao": null,
            "contratoExcluido": false
        }...
```
</details>

---

### 1.1 Consultar Contratos por ID
Busca os dados detalhados de um contrato específico utilizando seu identificador único no PNCP.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/1.1_consultarContratos_Id`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `numeroControlePncpContrato` | Texto | **Sim** | Identificador único do contrato (25 dígitos). |

---

### 1.2 Consultar Contratos por Fim de Vigência
Permite filtrar contratos cujo fim de vigência ocorra dentro de um intervalo de datas específico.

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/1.2_consultarContratos_FimVigencia`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `codigoOrgao` | Texto | Não | Código do órgão. |
| `codigoUnidadeGestora` | Texto | Não | Código da unidade gestora. |
| `codigoUnidadeGestoraOrigemContrato` | Texto | Não | Código da Unidade Gerenciadora de origem do contrato. |
| `codigoUnidadeRealizadoraCompra` | Texto | Não | Código da Unidade Gerenciadora que realizou a compra. |
| `numeroContrato` | Texto | Não | Número do contrato. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade. |
| `codigoTipo` | Texto | Não | Código do tipo de contrato. |
| `codigoCategoria` | Texto | Não | Código da categoria do contrato. |
| `niFornecedor` | Texto | Não | CNPJ/CPF do fornecedor. |
| `dataVigenciaFinalMin` | Texto | **Sim** | Data mínima do fim da vigência (YYYY-MM-DD). |
| `dataVigenciaFinalMax` | Texto | **Sim** | Data máxima do fim da vigência (YYYY-MM-DD). |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratos/1.2_consultarContratos_FimVigencia?pagina=1&tamanhoPagina=10&codigoOrgao=95559&codigoUnidadeGestora=180183&codigoUnidadeGestoraOrigemContrato=180183&codigoUnidadeRealizadoraCompra=180183&codigoModalidadeCompra=05&codigoTipo=99&codigoCategoria=60&niFornecedor=44092021000150&dataVigenciaFinalMin=2025-01-01&dataVigenciaFinalMax=2025-01-31`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```
{
    "resultado": [
        {
            "codigoOrgao": "95559",
            "nomeOrgao": "ESP-SECRETARIA DA SEGURANCA PUBLICA          ",
            "codigoUnidadeGestora": "180183",
            "nomeUnidadeGestora": "ESP-DIRETORIA  TEC. INFORMACAO E COMUNICACAO",
            "codigoUnidadeGestoraOrigemContrato": "180183",
            "nomeUnidadeGestoraOrigemContrato": "ESP-DIRETORIA  TEC. INFORMACAO E COMUNICACAO",
            "receitaDespesa": "D",
            "numeroContrato": "2025NE000017",
            "codigoUnidadeRealizadoraCompra": "180183",
            "nomeUnidadeRealizadoraCompra": "ESP-DIRETORIA  TEC. INFORMACAO E COMUNICACAO",
            "numeroCompra": "90006/2024",
            "codigoModalidadeCompra": "05",
            "nomeModalidadeCompra": "Pregão",
            "codigoTipo": "99",
            "nomeTipo": "Empenho",
            "codigoCategoria": "60",
            "nomeCategoria": "Compras",
            "codigoSubcategoria": null,
            "nomeSubcategoria": null,
            "niFornecedor": "44092021000150",
            "nomeRazaoSocialFornecedor": "A LOJA PRODUTOS DESCARTAVEIS LTDA",
            "processo": "057.00165126/2024-31",
            "objeto": "MATERIAS DE HIGIENICO",
            "informacoesComplementares": "",
            "dataVigenciaInicial": "2025-01-28T00:00:00",
            "dataVigenciaFinal": "2025-01-29T00:00:00",
            "valorGlobal": 3694.50000000,
            "numeroParcelas": 1,
            "valorParcela": 3694.50000000,
            "valorAcumulado": 3694.50000000,
            "totalDespesasAcessorias": null,
            "dataHoraInclusao": "2025-06-18T15:27:09",
            "numeroControlePncpContrato": null,
            "idCompra": "18018305900062024",
            "dataHoraExclusao": null,
            "contratoExcluido": false,
            "unidadesRequisitantes": null
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 0,
    "paginasRestantes": 1
}
```
</details>

---

### 2. Consultar Item de Contratos
Lista ou detalha os itens vinculados a cada contrato, exibindo quantidades, valores e eventuais atualizações contratuais (aditivos, por exemplo).

*   **Método:** `GET`
*   **URL:** `{{baseUrl}}/modulo-contratos/2_consultarContratosItem`

**Parâmetros:**

| Chave | Tipo | Obrigatório | Descrição |
| :--- | :--- | :--- | :--- |
| `pagina` | Inteiro | Não | Paginação dos resultados. |
| `tamanhoPagina` | Inteiro | Não | Limite de registros por página. |
| `codigoOrgao` | Inteiro | Não | Código do órgão. |
| `codigoUnidadeGestora` | Inteiro | Não | Código da unidade gestora. |
| `codigoUnidadeGestoraOrigemContrato` | Texto | Não | Código da Unidade Gerenciadora de origem do contrato. |
| `codigoUnidadeRealizadoraCompra` | Texto | Não | Código da Unidade Gerenciadora que realizou a compra. |
| `numeroContrato` | Texto | Não | Número do contrato. |
| `codigoModalidadeCompra` | Texto | Não | Código da modalidade. |
| `tipoItem` | Texto | Não | Tipo do item (Material/Serviço). |
| `codigoItem` | Inteiro | Não | Código do item (CATMAT/CATSER). |
| `niFornecedor` | Texto | Não | CNPJ/CPF do fornecedor. |
| `dataVigenciaInicialMin` | Texto | **Sim** | Data inicial mínima da vigência. |
| `dataVigenciaInicialMax` | Texto | **Sim** | Data inicial máxima da vigência. |

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-contratos/2_consultarContratosItem?pagina=1&tamanhoPagina=10&codigoOrgao=22000&codigoUnidadeGestora=110161&codigoUnidadeGestoraOrigemContrato=130016&codigoUnidadeRealizadoraCompra=130016&codigoItem=409245&dataVigenciaInicialMin=2021-10-27&dataVigenciaInicialMax=2022-01-24`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "codigoOrgao": 22000,
            "codigoUnidadeGestora": 110161,
            "codigoUnidadeGestoraOrigemContrato": 130016,
            "codigoUnidadeRealizadoraCompra": 130016,
            "codigoModalidadeCompra": "5",
            "numeroContrato": "00062/2021",
            "niFornecedor": "30479645000110",
            "nomeRazaoSocialFornecedor": "AMR SOLUCOES LABORATORIAIS LTDA",
            "processo": "21002.000967/2020-01",
            "dataVigenciaInicial": "2021-10-27T00:00:00",
            "dataVigenciaFinal": "2022-01-24T00:00:00",
            "valorGlobal": 20078,
            "tipoItem": null,
            "codigoItem": 409245,
            "descricaoIitem": "BALÃO LABORATÓRIO",
            "quantidadeItem": 100,
            "valorUnitarioItem": 89,
            "valorTotalItem": 8900,
            "dataHoraInclusao": "2021-10-28T08:06:53",
            "numeroControlePncpContrato": null,
            "idCompra": "13001605000052021",
            "dataHoraExclusaoContrato": null,
            "contratoExcluido": false,
            "nomeOrgao": "MINIST. DA AGRICUL.,PECUARIA E ABASTECIMENTO",
            "nomeUnidadeGestora": "SUPERINTENDENCIA REG. DE ADMIN. DA 1ª REGIAO",
            "nomeUnidadeGestoraOrigemContrato": "LABORATORIO FEDERAL DE DEFESA AGROPECUARIA/PE",
            "nomeUnidadeRealizadoraCompra": "LABORATORIO FEDERAL DE DEFESA AGROPECUARIA/PE",
            "nomeModalidadeCompra": "Pregão",
            "numeroCompra": "00005/2021",
            "dataHoraExclusaoItem": null,
            "contratoItemExcluido": false,
            "numeroItem": "00004"
        },
        {
            "codigoOrgao": 22000,
            "codigoUnidadeGestora": 110161,
            "codigoUnidadeGestoraOrigemContrato": 130016,
            "codigoUnidadeRealizadoraCompra": 130016,
            "codigoModalidadeCompra": "5",
            "numeroContrato": "00022/2022",
            "niFornecedor": "30479645000110",
            "nomeRazaoSocialFornecedor": "AMR SOLUCOES LABORATORIAIS LTDA",
            "processo": "21002.000967/2020-01",
            "dataVigenciaInicial": "2022-01-21T00:00:00",
            "dataVigenciaFinal": "2022-04-20T00:00:00",
            "valorGlobal": 18159,
            "tipoItem": null,
            "codigoItem": 409245,
            "descricaoIitem": "BALÃO LABORATÓRIO",
            "quantidadeItem": 50,
            "valorUnitarioItem": 89,
            "valorTotalItem": 4450,
            "dataHoraInclusao": "2022-01-24T15:20:26",
            "numeroControlePncpContrato": null,
            "idCompra": "13001605000052021",
            "dataHoraExclusaoContrato": null,
            "contratoExcluido": false,
            "nomeOrgao": "MINIST. DA AGRICUL.,PECUARIA E ABASTECIMENTO",
            "nomeUnidadeGestora": "SUPERINTENDENCIA REG. DE ADMIN. DA 1ª REGIAO",
            "nomeUnidadeGestoraOrigemContrato": "LABORATORIO FEDERAL DE DEFESA AGROPECUARIA/PE",
            "nomeUnidadeRealizadoraCompra": "LABORATORIO FEDERAL DE DEFESA AGROPECUARIA/PE",
            "nomeModalidadeCompra": "Pregão",
            "numeroCompra": "00005/2021",
            "dataHoraExclusaoItem": null,
            "contratoItemExcluido": false,
            "numeroItem": "00004"
        }
    ],
    "totalRegistros": 2,
    "totalPaginas": 1,
    "paginasRestantes": 0
}
```
</details>

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

Reúne informações cadastrais de fornecedores que atuam com a Administração Pública, incluindo dados como razão social, CNPJ ou CPF, natureza jurídica, porte da empresa, atividade econômica (CNAE) e habilitação para licitar. Este módulo facilita a identificação, análise e acompanhamento dos fornecedores registrados nos sistemas governamentais.

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-fornecedor/1_consultarFornecedor?cnpj=00001172000180&codigoCnae=5822101&ativo=True`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
    "resultado": [
        {
            "ativo": true,
            "cnpj": "00001172000180",
            "cpf": null,
            "habilitadoLicitar": true,
            "codigoCnae": 5822101,
            "nomeCnae": "EDIÇÃO INTEGRADA À IMPRESSÃO DE JORNAIS DIÁRIOS",
            "nomeMunicipio": "BRASÍLIA",
            "naturezaJuridicaId": 48,
            "naturezaJuridicaNome": "SOCIEDADE ANÔNIMA FECHADA",
            "porteEmpresaId": 5,
            "porteEmpresaNome": "DEMAIS",
            "nomeRazaoSocialFornecedor": "SA CORREIO BRAZILIENSE",
            "ufSigla": "DF"
        }
    ],
    "totalRegistros": 1,
    "totalPaginas": 1,
    "paginasRestantes": 0
}
```
</details>

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

**Exemplo de Requisição:**

**URL:** `https://dadosabertos.compras.gov.br/modulo-ocds/1_releases?page=<integer>&offsset=<integer>&buyerID=<string>&releaseStartDate=<string>&releaseEndDate=<string>`

<details>
<summary><b>🔎 Clique para ver a Resposta da requisição</b></summary>
   
```json
{
  "publisherDTO": {
    "name": "Ministério da Gestão e da Inovação",
    "uri": "https://www.gov.br/mgi"
  },
  "releases": [
    {
      "ocid": "ocds-76916x-00000000",
      "buyer": {
        "id": "BR-CNPJ-00000000",
        "name": "Órgão Exemplo"
      },
      "tender": {
        "id": "123456",
        "title": "Aquisição de Material de Escritório",
        "status": "complete"
      },
      "awards": [
        {
          "id": "award-1",
          "status": "active",
          "suppliers": [
            {
              "name": "Empresa Vencedora LTDA"
            }
          ]
        }
      ],
      "parties": [
        {
          "id": "BR-CNPJ-00000000",
          "name": "Órgão Exemplo",
          "roles": ["buyer"]
        },
        {
          "id": "BR-CNPJ-11111111",
          "name": "Empresa Vencedora LTDA",
          "roles": ["supplier"]
        }
      ]
    }
  ]
}...
```
</details>
