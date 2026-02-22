# 🌐 Dados Públicos

## 📋 O que são dados públicos?

### Definição
Dados públicos são informações que podem ser acessadas por qualquer cidadão, sem restrição, conforme previsto na **Lei de Acesso à Informação (LAI - Lei 12.527/2011)**.

### Características
- **Acesso universal:** Qualquer pessoa pode consultar, independentemente de justificativa
- **Transparência:** Instrumento fundamental para controle social
- **Publicidade:** Regra, sigilo é exceção (Art. 3º da LAI)
- **Interesse público:** Informações de relevância para a sociedade
- **Gratuidade:** Salvo custos de reprodução (Art. 12 da LAI)

### Onde encontrar dados públicos
| Local | Descrição | Exemplos |
|-------|-----------|----------|
| **Portais de transparência** | Sites oficiais com informações orçamentárias | Portal da Transparência da União |
| **Diários oficiais** | Publicações oficiais dos atos administrativos | DOU, Diários estaduais e municipais |
| **Dados abertos** | Plataformas com dados em formatos acessíveis | dados.gov.br |
| **SIC** | Serviço de Informação ao Cidadão | Atendimento presencial ou online |
| **Transparência ativa** | Informações disponibilizadas independentemente de solicitação | Quadro de servidores, licitações |

## 🔍 Limites entre transparência e proteção

### Tensão entre LAI e LGPD

| Lei | Princípio | Objetivo | Aplicação |
|-----|-----------|----------|-----------|
| **LAI** | Transparência | Garantir acesso à informação | Regra: publicidade |
| **LGPD** | Privacidade | Proteger dados pessoais | Regra: proteção |

### Como conciliar?

**Regra geral:**
- Dados **pessoais** devem ser protegidos (LGPD)
- Dados **públicos** devem ser acessíveis (LAI)
- Quando um dado pessoal está em documento público, deve-se avaliar:

### Matriz de decisão

| O dado é... | Relevante para interesse público? | Deve ser publicado? |
|-------------|-----------------------------------|---------------------|
| Pessoal | Sim | Sim, com proteção (tarja) |
| Pessoal | Não | Não (negar acesso) |
| Sensível | Sim | Avaliar caso a caso |
| Sensível | Não | Não (negar acesso) |
| Não pessoal | Sim | Sim, integralmente |
| Não pessoal | Não | Sim (transparência) |

### Princípios para equilíbrio

1. **Finalidade:** Para que o dado está sendo solicitado?
2. **Necessidade:** O dado pessoal é essencial para a informação?
3. **Proporcionalidade:** O benefício público supera o risco à privacidade?
4. **Minimização:** Compartilhar apenas o necessário
5. **Transparência:** Informar ao cidadão como seus dados serão usados

## ⚖️ Tratamento de dados pessoais em documentos públicos

### Quando um dado pessoal se torna público?

#### 1. Por previsão legal
- **Publicação em diário oficial:** Nomeações, exonerações, aposentadorias
- **Dados de agentes públicos:** Remuneração, cargo, lotação (Art. 11 da LAI)
- **Informações exigidas por lei:** Declarações de bens (quando exigido)

#### 2. Por interesse público
- **Dados de licitações e contratos:** Nome de empresas, valores, objetos
- **Prestação de contas:** Despesas, viagens, diárias
- **Informações ambientais:** Áreas de risco, licenciamento
- **Dados epidemiológicos:** Estatísticas de saúde (anonimizadas)

#### 3. Pelo próprio titular
- **Manifestações públicas:** Audiências, consultas públicas
- **Participação em conselhos:** Membros de conselhos municipais
- **Uso de redes sociais oficiais:** Comentários em páginas governamentais

### O que NÃO deve ser público?

| Tipo de dado | Exemplo | Fundamento Legal |
|--------------|---------|------------------|
| **Dados íntimos** | Saúde, vida sexual, orientação política | Art. 31 da LAI |
| **Dados sensíveis** | Religião, filiação sindical, biometria | LGPD, Art. 11 |
| **Segurança pessoal** | Endereço residencial, telefone pessoal | Art. 31, §1º da LAI |
| **Investigações** | Inquéritos sigilosos, processos sob segredo | Leis processuais |
| **Dados de menores** | Informações de crianças e adolescentes | ECA, Art. 17 |

## 🏛️ Transparência ativa vs passiva

### Transparência ativa
Órgãos públicos disponibilizam informações independentemente de solicitação.

**Obrigações legais (Art. 8º da LAI):**
- Portal da transparência com interface acessível
- Informações atualizadas no máximo anualmente
- Dados em formatos abertos e estruturados

**Conteúdo mínimo obrigatório:**
| Informação | Exemplo | Cuidados com LGPD |
|------------|---------|-------------------|
| Estrutura organizacional | Organograma | Sem dados pessoais |
| Servidores | Cargos, lotação | Remuneração é pública |
| Despesas | Empenhos, pagamentos | Ocultar dados de fornecedores pessoas físicas |
| Licitações | Editais, contratos | Proteger dados de participantes |
| Programas | Ações governamentais | Sem dados de beneficiários |

**Cuidados com LGPD na transparência ativa:**
- ✅ Publicar remuneração de servidores (é pública)
- ❌ Não publicar endereço residencial de servidores
- ✅ Publicar nome de empresas contratadas
- ❌ Proteger CPF de fornecedores pessoas físicas
- ✅ Publicar dados agregados de beneficiários
- ❌ Não publicar dados individuais de beneficiários

### Transparência passiva
Informações fornecidas mediante solicitação do cidadão (SIC).

**Fluxo do atendimento:**
Cidadão solicita informação
↓

Órgão recebe e registra pedido
↓

Analisa conteúdo do documento
↓
┌────────────────────────────────────┐
│ Contém dados pessoais? │
├────────────┬───────────────────────┤
│ SIM │ NÃO │
└─────┬──────┴───────────┬───────────┘
↓ ↓
4a. Aplica técnica 4b. Fornece
de proteção documento
↓ ↓

Fornece informação ao cidadão

text

**Prazos legais:**
- **Resposta imediata:** Quando possível
- **Prazo regular:** 20 dias (prorrogáveis por mais 10)
- **Recurso:** 10 dias para cada instância

## 🔒 Técnicas de proteção para transparência passiva

### 1. Tarja (Ocultação)
Ocultar dados pessoais não relevantes para a solicitação.

**Exemplo:**
Documento original:
Nome: João Silva, CPF: 123.456.789-00, RG: 12.345.678
Endereço: Rua das Flores, 123, apto 45, São Paulo - SP
Telefone: (11) 98765-4321
Informação solicitada: Valor do contrato

Documento fornecido:
Nome: João Silva [dados pessoais ocultados]
Valor do contrato: R$ 50.000,00

text

### 2. Versão parcial
Fornecer apenas as partes do documento que não contêm dados pessoais.

**Exemplo:**
Processo com 100 páginas:

Páginas 1-50: Informações administrativas

Páginas 51-60: Dados pessoais de servidores

Páginas 61-100: Informações orçamentárias

Fornecido: Páginas 1-50 e 61-100 (dados pessoais excluídos)

text

### 3. Anonimização
Remover identificadores que permitam associar a informação a uma pessoa.

**Exemplo:**
Antes:
O servidor João Silva, matrícula 12345, recebeu diária de R$ 500,00

Depois:
Servidor [anonimizado] recebeu diária de R$ 500,00

text

### 4. Agregação
Fornecer dados em formato agregado, não individual.

**Exemplo:**
Individual (NÃO FORNECER):

Maria: R$ 5.000,00

José: R$ 8.000,00

Ana: R$ 6.500,00

Agregado (FORNECER):
Média salarial do setor: R$ 6.500,00
Total de servidores: 3
Faixa salarial: R$ 5.000 a R$ 8.000

text

## 📋 Orientações para servidores

### Ao publicar informações (transparência ativa)

**Antes de publicar:**
- [ ] Verificar se a informação é realmente pública por lei
- [ ] Identificar dados pessoais no documento
- [ ] Avaliar se cada dado pessoal é necessário para transparência
- [ ] Proteger ou ocultar dados desnecessários
- [ ] Revisar o documento antes da publicação

**Checklist de verificação:**

□ A informação tem previsão legal para publicação?
□ Há dados pessoais que podem ser ocultados?
□ Dados sensíveis estão protegidos?
□ O formato é acessível (PDF, HTML, CSV)?
□ A informação está atualizada?

### Ao atender pedidos de informação (SIC)
Passo a passo:

Receber o pedido formalmente

Registrar no sistema de protocolo

Analisar se a informação existe e está disponível

Identificar dados pessoais no documento

Aplicar técnica de proteção adequada

Fornecer a informação ao cidadão

Arquivar o atendimento

Frases padrão para negativa:

"A informação contém dados pessoais protegidos pela LGPD"

"O acesso está restrito por [fundamento legal]"

"Fornecemos a versão com dados pessoais ocultados"

"O documento contém dados sensíveis sem relevância pública"

### Ao receber dados do cidadão
Cuidados na coleta:

Informar a finalidade da coleta

Coletar apenas dados estritamente necessários

Obter consentimento quando exigido

Proteger dados sensíveis com cuidado especial

Garantir segurança no armazenamento

Registro de consentimento:

markdown
Declaro que fui informado sobre a finalidade da coleta de meus dados:
- Dados coletados: [listar]
- Finalidade: [descrever]
- Compartilhamento: [informar com quem será compartilhado]
- Prazo de guarda: [informar período]

Assinatura: __________________________

##⚖️ Fundamentação legal

### LAI (Lei 12.527/2011)
Art. 3º: A transparência é regra, o sigilo é exceção.

Art. 7º: Qualquer interessado pode solicitar informação.

Art. 10: Não é necessário justificar o pedido.

Art. 31: Dados pessoais terão acesso restrito por 100 anos.

Art. 31, §1º: Informações pessoais podem ser divulgadas quando:

Relevantes para interesse público

Previstas em lei

Autorizadas pelo titular

### LGPD (Lei 13.709/2018)
Art. 23: Órgãos públicos devem:

Indicar finalidade do tratamento

Dar publicidade às hipóteses legais

Fornecer informações de forma transparente

Designar encarregado (DPO)

Art. 24: Empresas públicas e de economia mista sujeitas à LGPD.

Art. 25: Dados devem ser mantidos em formato interoperável.

### Marco Civil da Internet (Lei 12.965/2014)
Art. 7º: Direitos dos usuários, incluindo privacidade.

Art. 11: Guarda de registros por 6 meses.

## 📊 Exemplos práticos detalhados

  Exemplo 1: Pedido de acesso a contrato
Cenário: Cidadão solicita cópia do contrato de prestação de serviços

Documento original:

text
CONTRATO Nº 001/2024

CONTRATANTE: Prefeitura Municipal
CONTRATADO: João Carlos Oliveira, CPF 123.456.789-00,
            RG 12.345.678, residente na Rua das Flores, 123,
            telefone (11) 98765-4321

OBJETO: Prestação de serviços de consultoria
VALOR: R$ 50.000,00
PRAZO: 12 meses
Análise:

Contratado é pessoa física (dados pessoais)

Objeto e valor são públicos

Endereço e telefone não são relevantes

Documento fornecido:

text
CONTRATO Nº 001/2024

CONTRATANTE: Prefeitura Municipal
CONTRATADO: João Carlos Oliveira [dados pessoais protegidos]

OBJETO: Prestação de serviços de consultoria
VALOR: R$ 50.000,00
PRAZO: 12 meses
  Exemplo 2: Pedido de lista de servidores
Cenário: Cidadão solicita relação de servidores da secretaria

Base de dados original:

Nome	CPF	Cargo	Salário	Endereço	Telefone
Ana Silva	123.456.789-00	Analista	R$ 8.500	Rua A, 123	91234-5678
José Santos	987.654.321-00	Técnico	R$ 5.200	Rua B, 456	97654-3210
Análise:

Nome, cargo e salário são públicos (STF, 2022)

CPF, endereço e telefone são pessoais

Documento fornecido:

Nome	Cargo	Salário
Ana Silva	Analista	R$ 8.500
José Santos	Técnico	R$ 5.200

  Exemplo 3: Pedido de dados de beneficiários
Cenário: Pesquisador solicita dados de beneficiários do Bolsa Família para estudo

Base original:

NIS	Nome	CPF	Renda	Benefício	Cidade
123456	Maria Souza	456.789.123-00	R$ 350	R$ 600	São Paulo
789012	João Pereira	321.654.987-00	R$ 420	R$ 400	Guarulhos
Análise:

Pesquisa tem finalidade acadêmica legítima

Dados individuais não são necessários

Anonimização é suficiente

Documento fornecido:

ID	Faixa renda	Benefício médio	Região
001	Até ½ SM	R$ 500	Capital
002	Até ½ SM	R$ 500	Grande SP

  Exemplo 4: Publicação de diárias no portal
Cenário: Portal da transparência publica diárias de servidores

Registro original:

text
Servidor: Carlos Alberto, CPF 789.123.456-00
Cargo: Assessor, matrícula 54321
Destino: Brasília - DF
Período: 10 a 12/05/2024
Valor diária: R$ 1.200,00
Motivo: Reunião no Ministério
Publicação adequada:

text
Servidor: Carlos Alberto
Cargo: Assessor
Destino: Brasília - DF
Período: 10 a 12/05/2024
Valor diária: R$ 1.200,00
Motivo: Reunião no Ministério
[Dados pessoais (CPF, matrícula) não publicados]

## ✅ Matriz de decisão rápida

### Para cada dado, pergunte:
Pergunta	Se SIM	Se NÃO
É público por lei?	Publicar	Avaliar próxima
É necessário para transparência?	Publicar com proteção	Não publicar
É dado sensível?	Proteção especial	Avaliar próxima
Pode ser anonimizado?	Anonimizar e publicar	Não publicar
Há consentimento do titular?	Publicar	Não publicar

### Exemplos de classificação:
Informação	Classificação	Ação
Nome de servidor	Público	Publicar
Remuneração de servidor	Público	Publicar
CPF de servidor	Pessoal	Não publicar
Endereço de servidor	Pessoal	Não publicar
Atestado médico	Sensível	Proteção especial
Nome de fornecedor (PF)	Pessoal	Publicar com cautela
CPF de fornecedor (PF)	Pessoal	Não publicar
Dados de licitação	Público	Publicar integral

## 📌 Pontos-chave para servidores
Lembre-se sempre:
Regra geral: Publicidade é a regra, sigilo é exceção

Dados pessoais: Proteger sempre que possível

Interesse público: Avaliar relevância antes de publicar

Técnicas de proteção: Tarja, anonimização, agregação

Fundamentação: Toda negativa deve ser motivada

Erros comuns a evitar:
❌ Publicar CPF de servidores no portal
❌ Fornecer lista de beneficiários com dados pessoais
❌ Negar acesso a informação pública sem fundamento
❌ Deixar de atender pedido no prazo
❌ Publicar dados sensíveis sem necessidade

Boas práticas:
✅ Quando em dúvida, consulte a assessoria jurídica
✅ Mantenha registro de todos os pedidos e respostas
✅ Treine a equipe do SIC periodicamente
✅ Atualize o portal com informações corretas
✅ Use linguagem clara e acessível

## 📚 Legislação e normas relacionadas

### Leis federais
Lei 12.527/2011 (LAI): Lei de Acesso à Informação

Lei 13.709/2018 (LGPD): Lei Geral de Proteção de Dados

Lei 12.965/2014 (Marco Civil): Direitos na internet

Lei 8.429/1992 (Improbidade): Sanções para agentes públicos

Decretos
Decreto 7.724/2012: Regulamenta a LAI

Decreto 8.777/2016: Política de Dados Abertos

Decreto 10.046/2019: Compartilhamento de dados

Orientações da CGU
Guia de Transparência Ativa

Manual do SIC

Orientações sobre LGPD e LAI

## 🔍 Glossário
Termo	Definição
Transparência ativa	Informações disponibilizadas independentemente de solicitação
Transparência passiva	Informações fornecidas mediante pedido
SIC	Serviço de Informação ao Cidadão
Dados abertos	Dados em formato acessível e reutilizável
Tarja	Ocultação de dados pessoais em documentos
Interesse público	Relevância para a sociedade
Dado pessoal	Informação relacionada a pessoa identificada ou identificável
Dado sensível	Dado com proteção especial (saúde, religião, política)
⬆ Voltar ao topo

text

## ✅ **Arquivo pronto!**

Este arquivo `dados-publicos.md` está completo com:
- 📌 Definição de dados públicos
- 🔍 Limites entre LAI e LGPD
- ⚖️ Tratamento de dados pessoais
- 🏛️ Transparência ativa e passiva
- 🔒 Técnicas de proteção
- 📋 Orientações para servidores
- 📊 Exemplos práticos
- ✅ Matrizes de decisão
- 📚 Legislação e glossário
