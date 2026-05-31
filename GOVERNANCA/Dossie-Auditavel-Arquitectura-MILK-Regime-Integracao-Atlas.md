# Dossiê Auditável da Arquitectura MILK
## Regime de Integração no Atlas Vivo

**Versão:** 1.1  
**Data:** Maio 2026  
**Estatuto:** Documento de Governança Interna — Acesso Público Controlado  
**Licença:** EUPL-1.2  
**Responsabilidade:** Associação MILK

---

## 1. Enquadramento e Propósito

Este dossiê constitui o instrumento auditável da arquitectura de dados, governança e integração do sistema MILK no contexto do Atlas Vivo. Serve finalidades múltiplas e complementares:

- **Auditoria técnica**: rastreabilidade dos componentes, dependências e fluxos de dados
- **Auditoria jurídica**: conformidade com RGPD, EUPL e legislação portuguesa aplicável
- **Auditoria financeira**: verificação de elegibilidade perante financiadores públicos e privados
- **Auditoria semântica**: alinhamento com ontologias e padrões de interoperabilidade reconhecidos
- **Auditoria política**: compatibilidade com princípios de cultura pública, acesso aberto e soberania digital
- **Auditoria económica**: viabilidade, sustentabilidade e propósito não lucrativo

O documento é concebido para ser utilizável perante:

- Financiadores públicos nacionais (DGArtes, Fundação para a Ciência e a Tecnologia, COMPETE 2030)
- Programas europeus (Creative Europe, Horizon Europe, ERDF via Portugal 2030)
- Auditores jurídicos e fiscais
- Parceiros académicos e científicos
- Instituições públicas municipais e nacionais
- Plataformas de dados culturais europeus (Europeana, OpenAIRE)

---

## 2. Identidade Institucional

| Atributo | Valor |
|---|---|
| **Entidade** | Associação MILK |
| **Forma jurídica** | Associação sem fins lucrativos (art. 157.º e ss. Código Civil português) |
| **Finalidade estatutária** | Promoção, investigação e mediação de património cultural intangível |
| **Regime fiscal** | Isento de IRC para actividades de interesse geral (CIRC art. 10.º) |
| **Enquadramento RGPD** | Responsável pelo tratamento de dados; DPO designado ou em designação |
| **Licença de código** | European Union Public Licence v1.2 (EUPL-1.2) |
| **Princípios de dados** | FAIR (Findable, Accessible, Interoperable, Reusable) |

---

## 3. Arquitectura Técnica do Sistema MILK

### 3.1 Componentes Principais

O sistema MILK é composto por camadas funcionais distintas com interfaces definidas:

```
┌─────────────────────────────────────────────────┐
│ CAMADA DE APRESENTAÇÃO                          │
│ Interface pública (HTML/CSS/JS)                 │
│ Atlas Vivo (Google Maps API + Leaflet)          │
│ Painel de gestão interna                        │
└─────────────────────────────────────────────────┘
                        ↑
┌─────────────────────────────────────────────────┐
│ CAMADA LÓGICA (Google Apps Script)              │
│ Orquestrador de processos                       │
│ Controladores de fluxo de dados                 │
│ Gestores de consentimento e acesso              │
└─────────────────────────────────────────────────┘
                        ↑
┌─────────────────────────────────────────────────┐
│ CAMADA DE DADOS (Google Workspace)              │
│ Google Sheets (base de dados operacional)       │
│ Google Drive (repositório documental)           │
│ Google Forms (recolha de dados primários)       │
└─────────────────────────────────────────────────┘
```

### 3.2 Dependências Externas

| Serviço | Finalidade | Tratamento de dados | Jurisdição |
|---|---|---|---|
| Google Workspace | Armazenamento e lógica | Dados da organização | UE (RGPD) |
| Google Maps API | Visualização geoespacial | Dados públicos | UE (RGPD) |
| GitHub (milkivc) | Versionamento de código e documentação | Dados públicos | UE/EUA |
| Leaflet.js | Cartografia alternativa | Local, sem transferência | N/A |

---

## 4. Auditoria Semântica e Interoperabilidade

### 4.1 Padrões Adoptados

O sistema MILK alinha-se com os seguintes padrões internacionais de interoperabilidade semântica para património cultural:

| Padrão | Descrição | Aplicação no MILK |
|---|---|---|
| **CIDOC-CRM** (ISO 21127:2014) | Ontologia de referência para património cultural | Estrutura semântica dos registos de dispositivos e territórios |
| **Dublin Core (DC)** | Metadados mínimos de descrição de recursos | Metadados de cada dispositivo metodológico |
| **FAIR Principles** | Findable, Accessible, Interoperable, Reusable | Princípio orientador de toda a arquitectura de dados |
| **Europeana Data Model (EDM)** | Modelo de dados da Europeana | Compatibilidade para futura interligação com Europeana |
| **Schema.org** | Vocabulário semântico para web | Marcadores de dados estruturados nas páginas públicas |
| **GeoJSON / WGS84** | Padrão geoespacial | Coordenadas de todos os registos territoriais |
| **SKOS** | Sistemas de organização de conhecimento | Vocabulários controlados para classificação de dispositivos |

### 4.2 Política de Terminologia Inclusiva

O vocabulário utilizado em todos os repositórios e sistemas MILK obedece a uma **política de terminologia inclusiva de aplicação obrigatória e permanente**. Esta política aplica-se sem excepções a todos os campos públicos, metadados, títulos de dispositivos, nomes de personagens, ficheiros e documentação.

**Princípios da política:**

- Nenhum termo pode afectar, estigmatizar ou ferir qualquer minoria — étnica, física, cultural, de saúde mental, de género ou de origem
- Nenhum símbolo, denominação ou representação pode reproduzir hierarquias coloniais, capacitistas ou discriminatórias
- A autodesignação das comunidades prevalece sempre sobre denominações externas
- Quando um termo é identificado como inadequado, é removido de imediato de todos os ficheiros e substituído de forma retroactiva
- A revisão terminológica é contínua, não pontual

**Processo de revisão:**

1. Identificação do termo inadequado (por membro da equipa, comunidade ou parceiro)
2. Remoção imediata do ficheiro e substituição por denominação adequada
3. Registo no audit trail com data, justificação e termo substituto
4. Actualização do GLOSSARIO.md com entrada da substituição
5. Comunicação à equipa para garantir consistência em novos documentos

**Referências de validação terminológica:**

- Getty Art & Architecture Thesaurus (AAT)
- UNESCO Thesaurus
- DGPC — Vocabulário do Património Cultural Imaterial
- Convenção da UNESCO para o PCI (2003)
- Recomendações do Conselho da Europa sobre linguagem inclusiva
- ONU — Terminologia de Direitos Humanos

### 4.3 Registo de Entidades com Correspondência Dublin Core

Cada dispositivo metodológico do catálogo operacional MILK carrega os seguintes metadados mínimos conforme Dublin Core:

```
dc:title         → Nome do dispositivo
dc:description   → Descrição funcional
dc:type          → Tipo de dispositivo (Oficina / Activação / Ritual / Arquivo / etc.)
dc:subject       → Categoria (Comunitário / Patrimonial / Folclore Vivo / etc.)
dc:creator       → Associação MILK
dc:publisher     → Associação MILK
dc:date          → Data de criação / última revisão
dc:rights        → EUPL-1.2
dc:language      → pt-PT
dc:identifier    → URI único (a atribuir por dispositivo)
dc:coverage      → Território de aplicação (Georreferenciado em WGS84)
dc:relation      → Ligações a outros dispositivos e recursos externos
```

---

## 5. Auditoria Jurídica e de Conformidade

### 5.1 Regulamento Geral de Protecção de Dados (RGPD)

| Aspecto | Regime MILK |
|---|---|
| **Base jurídica do tratamento** | Consentimento explícito (art. 6.º, n.º1, al. a) e interesse legítimo (al. f)) |
| **Dados sensíveis** | Dados étnicos ou culturais tratados com protecção reforçada (art. 9.º) |
| **Direitos dos titulares** | Acesso, rectificação, apagamento, portabilidade garantidos |
| **Transferências internacionais** | Limitadas a países com decisão de adequação (Google: cláusulas-tipo aprovadas) |
| **Prazos de conservação** | Definidos por categoria de dado; máximo de 5 anos sem reconfirmação |
| **Privacy by design** | Arquitectura concebida com separação de camadas pública/privada |

### 5.2 Licença EUPL-1.2

Todo o código produzido pela Associação MILK é disponibilizado sob **European Union Public Licence v1.2 (EUPL-1.2)**:

- Licença de código aberto reconhecida pela Comissão Europeia
- Compatível com GPL v2, LGPL, MPL, OSL, CeCILL
- Permite uso, modificação e redistribuição com manutenção da mesma licença
- Aplica-se a código fonte, scripts e conteúdo estruturado
- Exclui conteúdo editorial protegido por direito de autor das comunidades colaborantes

### 5.3 Direitos de Autor e Património Intangível

- Narrativas, relatos e expressões culturais recolhidas pertencem às comunidades de origem
- A MILK actua como curadora e mediadora, não como proprietária dos conteúdos
- Todos os colaboradores assinam termos de cedição de direitos ou de uso licenciado
- O regime de atribuição segue as normas da Convenção da UNESCO para o Património Cultural Imaterial (2003)

---

## 6. Auditoria Financeira e Elegibilidade

### 6.1 Fontes de Financiamento Compatíveis

| Programa | Tipo | Elegibilidade MILK | Mecanismo de acesso |
|---|---|---|---|
| **DGArtes — Apoios Quadrienais** | Subvenção pública nacional | Elegível (associação cultural) | Concurso público anual |
| **Creative Europe — Culture strand** | Programa europeu | Elegível (entidade cultural sem fins lucrativos) | Chamadas abertas CE |
| **Horizon Europe — Cluster 2** | Investigação e Inovação | Elegível com parceiro académico | Consórcio mínimo 3 países |
| **Portugal 2030 (FEDER/FSE+)** | Fundos estruturais europeus | Elegível (inclusão social, cultura, digitalização) | Candid. via AG regional |
| **Fundação Calouste Gulbenkian** | Mecenato / Filantropia | Elegível | Candidatura directa |
| **Caixa Cultura (CGD)** | Financiamento bancário cultural | Elegível (projectos de qualidade inequívoca) | Concurso público |
| **IRS Consignação 1%** | Contributo fiscal c/ destino | Elegível (entidade cultural inscrita) | Registo na AT |
| **EEA Grants — Programa Cultura** | Cooperação Noruega/Is./Liech. | Elegível com contrapartida nacional | Entidade gestora PT |

### 6.2 Critérios de Elegibilidade Transversais

Para aceder à maioria dos financiamentos acima listados, o sistema MILK demonstra:

- **Não-lucratividade**: estatutos e contas públicas verificáveis
- **Impacto mensurável**: indicadores de alcance, participação e devolução cultural
- **Inovação metodológica**: dispositivos originais, documentados e replicáveis
- **Inclusão e acessibilidade**: adaptabilidade dos dispositivos a populações diversas
- **Georreferenciação**: impacto territorial verificável por número de freguesias e municípios
- **Abertura e transparência**: código aberto, dados públicos, relatórios auditáveis
- **Parceria institucional**: capacidade de articular com autarquias, museus, universidades

### 6.3 Modelo de Sustentabilidade Económica

O modelo MILK não assenta em lucratividade mas em **sustentabilidade por diversificação de receitas**:

```
Receitas públicas       → Subvenções DGArtes, municípios, programas europeus
Receitas de prestação   → Programas em escolas, museus, SESC, CCDR
Receitas editoriais     → Publicações, kits, baralhos, colecções
Receitas de formação    → Formação de mediadores e equipas institucionais
Receitas de mecenato    → Gulbenkian, CGD, fundações privadas
Contributo cívico       → IRS consignação 1%
```

---

## 7. Auditoria Política e de Alinhamento Estratégico

### 7.1 Alinhamento com Políticas Públicas Nacionais

| Política | Instrumento | Alinhamento MILK |
|---|---|---|
| Política Cultural Nacional | Programa de Governo / Lei de Bases da Cultura | Promoção de património intangível e acesso |
| Agenda Digital Portugal | Portugal Digital 2030 | Digitalização de memória cultural |
| Política de Inclusão | ENEAS / Plano Nacional de Inclusão | Dispositivos acessíveis e intergeração |
| Cidades Inteligentes | SAMA2030 / Smart Cities | Atlas Vivo como infra-estrutura de dados |
| Conv. UNESCO PCI (2003) | Ratificada por Portugal | Princípios de registo e salvaguarda de PCI |

### 7.2 Alinhamento com Políticas Europeias

| Política | Instrumento | Alinhamento MILK |
|---|---|---|
| Estratégia Cultural Europeia | Agenda Europeia para a Cultura 2019 | Acesso, diversidade, inovação cultural |
| Agenda Digital Europeia | Digital Decade 2030 | Dados culturais abertos e interoperáveis |
| New European Bauhaus | Comissão Europeia | Estética, sustentabilidade, inclusão |
| Data Governance Act | Regulamento (UE) 2022/868 | Governança de dados culturais de interesse geral |
| AI Act | Regulamento (UE) 2024/1689 | Uso responsável de IA em contexto cultural |

### 7.3 Princípios de Cultura Pública Adoptados

- **Princípio de não extracção**: a MILK não extrai nem musealifica comunidades — devolve e activa
- **Princípio de co-autoria**: as comunidades são co-autoras dos dispositivos, não objectos de estudo
- **Princípio de reciprocidade**: toda a recolha tem devolução pública concreta ao território
- **Princípio de transparência**: dados, metodologias e resultados são públicos e auditáveis
- **Princípio de autonomia**: as comunidades podem retirar o seu consentimento a qualquer momento
- **Princípio de não discriminação**: nenhum símbolo, personagem ou denominação pode afectar qualquer minoria

---

## 8. Regime de Integração no Atlas Vivo

### 8.1 Camadas de Dados do Atlas Vivo

O Atlas Vivo opera com quatro camadas de dados com níveis de acesso diferenciados:

| Camada | Conteúdo | Acesso | Responsabilidade |
|---|---|---|---|
| **Camada pública** | Dispositivos, pontos de memória, actividades abertas | Público geral | MILK |
| **Camada comunitária** | Registos de participação, relatos, arquivos | Membros e parceiros | MILK + comunidade |
| **Camada institucional** | Acordos, protocolos, relatórios de impacto | Parceiros institucionais | MILK |
| **Camada de governança** | Auditoria, conformidade, dados sensíveis | Equipa MILK + auditores | MILK |

### 8.2 Fluxo de Integração de um Dispositivo no Atlas

```
[1] Criação da ficha metodológica (GitHub / catálogo operacional)
      ↓
[2] Revisão semântica e terminológica (política de inclusão obrigatória)
      ↓
[3] Atribuição de metadados Dublin Core + georreferenciação (WGS84)
      ↓
[4] Classificação CIDOC-CRM se aplicável
      ↓
[5] Validação interna (equipa MILK)
      ↓
[6] Integração no Atlas Vivo (Google Sheets → Apps Script → Mapa)
      ↓
[7] Publicação na camada adequada (pública / comunitária / institucional)
      ↓
[8] Registo de audit trail (data, autor, versão, alterações)
```

### 8.3 Campos Obrigatórios por Registo no Atlas

| Campo | Tipo | Obrigatório | Fonte de dados |
|---|---|---|---|
| ID único | String (UUID) | Sim | Gerado automaticamente |
| Título | String | Sim | Ficha metodológica |
| Categoria | Vocabulário controlado | Sim | Taxonomia MILK |
| Território | Nome + GeoJSON | Sim | Georreferenciação |
| Freguesia | Código DSGOT | Sim | CAOP / DGTERRITÓRIO |
| Data de criação | ISO 8601 | Sim | Automático |
| Última revisão | ISO 8601 | Sim | Automático |
| Autor/equipa | ID de membro | Sim | Registo de equipa |
| Camada de acesso | Enum (pública/comunitária/...) | Sim | Decisão editorial |
| Estado | Enum (rascunho/activo/arquivado) | Sim | Fluxo editorial |
| Consentimento | Booleano + data | Se dados pessoais | Formulário MILK |

---

## 9. Rastreabilidade e Audit Trail

Todo o sistema MILK mantém um **registo de audit trail** contínuo:

- **Versionamento de documentação**: GitHub (histórico de commits público)
- **Versionamento de dados**: Google Sheets com histórico de alterações activado
- **Registo de consentimentos**: formulário com data, versão do documento e canal
- **Registo de acesso a dados sensíveis**: log interno com identidade e justificação
- **Registo de decisões editoriais**: ficheiro de govern de cada publicação
- **Registo de substituições terminológicas**: data, termo removido, termo substituto, justificação

O audit trail é mantido por um mínimo de 5 anos e é acessível a auditores designados mediante pedido fundamentado.

---

## 10. Glossário de Termos Institucionais

| Termo MILK | Definição institucional |
|---|---|
| **Dispositivo** | Unidade metodológica activável, com formato definido e devolução pública |
| **Activação** | Acto de colocar um dispositivo em funcionamento num território e com uma comunidade |
| **Devolução** | Entrega de resultado concreto à comunidade participante, no território |
| **Território** | Espaço geográfico definido por unidade administrativa e memória cultural |
| **Mediador** | Profissional formado para activar dispositivos MILK com ética e competência |
| **Património intangível** | Expressões vivas de cultura: práticas, narrativas, saberes, rituais (Conv. UNESCO 2003) |
| **Atlas Vivo** | Sistema de visualização geoespacial da memória cultural por território |
| **Folclore Vivo** | Universo de personagens e figuras da imaginação popular lusitana, activados metodologicamente |
| **Audit trail** | Registo cronológico e verificável de todas as alterações a dados e decisões |
| **Catálogo operacional** | Repositório GitHub de todas as fichas metodológicas MILK |
| **Guardião das Profundezas** | Figura ancestral do subsolo, sem atributos físicos definidos — forma determinada pela comunidade |

---

## 11. Declaração de Conformidade

Este dossiê constitui a declaração formal da Associação MILK de que:

1. O sistema MILK foi concebido com princípios de privacidade, abertura e responsabilidade
2. A arquitectura é auditável, documentada e versão-controlada
3. Os dados das comunidades são tratados com base jurídica válida e consentimento informado
4. Os dispositivos metodológicos são originais, replicáveis e de impacto mensurável
5. A organização é elegível para financiamento público europeu e nacional
6. O vocabulário utilizado é revisto, inclusivo e alinhado com thesauri internacionais
7. Nenhum termo, símbolo ou denominação que afecte qualquer minoria é utilizado em qualquer campo público ou de interoperabilidade
8. A revisão terminológica é contínua, retroactiva e registada em audit trail
9. A interoperabilidade com plataformas europeias de património cultural é um objectivo estratégico

---

*Associação MILK — Licença EUPL-1.2 — Versão 1.1 — Maio 2026*
