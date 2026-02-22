```markdown
# 🔢 Dados Anonimizados

## 📋 O que são dados anonimizados?

### Definição legal (Art. 5º, III da LGPD)
"Dado anonimizado: dado relativo a titular que não possa ser identificado, considerando a utilização de meios técnicos razoáveis e disponíveis na ocasião de seu tratamento"

### Características principais
- **Não permitem identificar** o titular direta ou indiretamente
- **Não são considerados dados pessoais** para fins da LGPD
- **Podem ser utilizados livremente** (desde que realmente anônimos)
- **Risco de reidentificação** deve ser considerado e mitigado
- **Responsabilidade** de quem realiza a anonimização

### Importância no setor público
- Permite **compartilhamento** de dados para pesquisa
- Viabiliza **transparência** sem expor cidadãos
- Contribui para **políticas públicas** baseadas em evidências
- **Incentiva inovação** com dados governamentais

### Processo de anonimização
```
Dados pessoais (protegidos pela LGPD)
       ↓
[Processo de anonimização]
       ↓
Dados anonimizados (fora do escopo da LGPD)
       ↓
Podem ser compartilhados, publicados, utilizados para pesquisa
```

## 🔬 Técnicas de anonimização

### 1. Supressão (Remoção)
Remoção completa de identificadores diretos que possam identificar o titular.

**Como funciona:**
- Elimina campos como nome, CPF, RG, matrícula
- Remove informações únicas ou muito específicas

**Exemplo:**
| Antes | Depois |
|-------|--------|
| João Silva, CPF 123.456.789-00 | [Removido] |
| Maria Oliveira, RG 12.345.678 | [Removido] |
| Pedro Santos, matrícula 2023001 | [Removido] |

**Vantagens:** Simples de implementar, eficaz para identificadores diretos
**Desvantagens:** Pode perder informação útil, não protege contra identificadores indiretos

### 2. Generalização
Substituição de valores específicos por categorias mais amplas.

**Como funciona:**
- Transforma idade exata em faixa etária
- Converte endereço completo em bairro ou região
- Agrupa profissões em categorias

**Exemplo:**
| Atributo | Antes | Depois |
|----------|-------|--------|
| **Idade** | 42 anos | 40-49 anos |
| **CEP** | 70040-010 | 70000-000 (região) |
| **Profissão** | Auditor fiscal | Servidor público |
| **Renda** | R$ 8.542,00 | R$ 8.000 - R$ 9.000 |
| **Data de nascimento** | 15/03/1982 | Março/1982 ou 1980-1985 |

**Vantagens:** Mantém utilidade analítica, protege contra identificação
**Desvantagens:** Perde precisão, requer definição de categorias adequadas

### 3. Perturbação (Adição de ruído)
Inserção de pequenas variações aleatórias nos dados numéricos.

**Como funciona:**
- Adiciona ou subtrai pequenos valores
- Mantém tendências estatísticas
- Impede identificação exata

**Exemplo:**
| Antes | Depois |
|-------|--------|
| Renda: R$ 5.432,00 | R$ 5.400,00 (-32) |
| Altura: 1,75m | 1,76m (+0,01) |
| Peso: 70,5 kg | 70,2 kg (-0,3) |
| Temperatura: 36,5°C | 36,6°C (+0,1) |

**Vantagens:** Preserva propriedades estatísticas, difícil de reverter
**Desvantagens:** Não adequado para dados categóricos, requer cálculo cuidadoso

### 4. Agregação
Apresentação de dados em grupo, não individualmente.

**Como funciona:**
- Agrupa registros individuais
- Apresenta estatísticas do grupo
- Elimina dados individuais

**Exemplo:**
| Individual | Agregado |
|------------|----------|
| João: 35 anos | Faixa etária 30-39: 45 pessoas |
| Maria: 38 anos | Média de idade: 36,5 anos |
| Pedro: 42 anos | Total de pessoas: 120 |
| Ana: 31 anos | Percentual por gênero: 52% feminino |

**Vantagens:** Alta proteção, útil para estatísticas públicas
**Desvantagens:** Perde dados individuais, não permite análises granulares

### 5. K-anonimato
Garantia que cada registro é indistinguível de pelo menos k-1 outros registros.

**Como funciona:**
- Cada combinação de atributos aparece pelo menos k vezes
- Quanto maior o k, maior a proteção
- Identificadores são generalizados até atingir o k desejado

**Exemplo com k=3:**
| Grupo | Idade | CEP | Profissão |
|-------|-------|-----|-----------|
| Grupo A | 30-39 | 70000-*** | Servidor |
| Grupo A | 30-39 | 70000-*** | Servidor |
| Grupo A | 30-39 | 70000-*** | Servidor |
| Grupo B | 40-49 | 71000-*** | Professor |
| Grupo B | 40-49 | 71000-*** | Professor |
| Grupo B | 40-49 | 71000-*** | Professor |

**Vantagens:** Proteção comprovada matematicamente, padrão internacional
**Desvantagens:** Complexo de implementar, pode perder muita informação

### 6. L-diversidade (Avançado)
Evolução do k-anonimato que garante diversidade de valores sensíveis.

**Como funciona:**
- Além de k registros iguais, garante l valores diferentes para atributos sensíveis
- Protege contra ataques de homogeneidade

**Exemplo:**
```
Sem l-diversidade (problema):
Grupo | Idade | CEP    | Doença
A     | 30-39 | 70000-* | Câncer
A     | 30-39 | 70000-* | Câncer
A     | 30-39 | 70000-* | Câncer

Com l-diversidade (l=3):
Grupo | Idade | CEP    | Doença
A     | 30-39 | 70000-* | Câncer
A     | 30-39 | 70000-* | Diabetes
A     | 30-39 | 70000-* | Hipertensão
```

## ⚠️ Diferença: Anonimização vs Pseudonimização

### Pseudonimização
- Substituição de identificadores por códigos ou pseudônimos
- **Permite reidentificação** com informação adicional (chave)
- **Ainda é dado pessoal** (sujeito à LGPD)
- Técnica recomendada para segurança, mas não remove da lei

### Comparativo detalhado

| Aspecto | Anonimização | Pseudonimização |
|---------|--------------|-----------------|
| **Reversível** | Não (irreversível) | Sim (com chave) |
| **É dado pessoal?** | Não | Sim |
| **Sujeito à LGPD?** | Não | Sim |
| **Risco principal** | Reidentificação | Quebra da chave |
| **Exemplo** | Estatísticas agregadas | ID numérico em pesquisa |
| **Onde usar** | Dados públicos, pesquisas | Bancos de dados operacionais |
| **Segurança** | Alta (se bem feito) | Média (dependente da chave) |

### Exemplo de pseudonimização
```
Prontuário original:
Paciente: João Silva, CPF 123.456.789-00
Data nasc: 15/03/1982, Diagnóstico: Hipertensão

Após pseudonimização:
ID: PAC-98765, Diagnóstico: Hipertensão
Data nasc: 15/03/1982

Chave de decodificação (armazenada separadamente):
PAC-98765 → João Silva, CPF 123.456.789-00
```

### Quando usar cada técnica

| Cenário | Técnica recomendada |
|---------|---------------------|
| **Pesquisa científica** | Anonimização (se possível) ou pseudonimização |
| **Base de dados operacional** | Pseudonimização com acesso restrito |
| **Publicação de dados abertos** | Anonimização obrigatória |
| **Compartilhamento entre órgãos** | Anonimização ou pseudonimização com acordo |
| **Análise estatística interna** | Pseudonimização |

## 🎯 Aplicações no setor público

### Onde usar dados anonimizados

1. **Estatísticas públicas**
   - Censos demográficos (IBGE)
   - Indicadores de saúde (DATASUS)
   - Dados educacionais (Censo Escolar)
   - Estatísticas econômicas

2. **Pesquisas acadêmicas**
   - Estudos epidemiológicos
   - Análises socioeconômicas
   - Avaliação de políticas públicas
   - Pesquisas em ciências sociais

3. **Transparência ativa**
   - Dados abertos (dados.gov.br)
   - Portais de transparência
   - Prestação de contas
   - Controle social

4. **Desenvolvimento de políticas**
   - Planejamento urbano
   - Alocação de recursos
   - Identificação de necessidades
   - Avaliação de impacto

5. **Inovação e tecnologia**
   - Desenvolvimento de aplicativos cívicos
   - Hackathons de dados públicos
   - Soluções baseadas em evidências
   - Startups de impacto social

### Exemplos práticos detalhados

#### Exemplo 1: Dados de saúde (DATASUS)
```markdown
Cenário: Hospital público quer compartilhar dados de internações para pesquisa

Antes (dados pessoais - NÃO COMPARTILHAR):
Paciente: Maria Oliveira, CPF 987.654.321-00
Internação: 10/05/2024, Hospital das Clínicas
Diagnóstico: Diabetes tipo 2, CID10 E11
Médico: Dr. Roberto Alves, CRM 12345
Endereço: Rua das Flores, 123, apto 45

Depois (dados anonimizados - PODE COMPARTILHAR):
ID anonimizado: PAC-98765
Internação: Maio/2024, Região Centro-Oeste
Diagnóstico: Doença crônica não transmissível
Faixa etária: 50-59 anos
Sexo: Feminino
[Médico e endereço removidos]
```

#### Exemplo 2: Dados educacionais (Censo Escolar)
```markdown
Cenário: Secretaria de Educação quer publicar dados de desempenho escolar

Antes (dados pessoais):
Aluno: João Pereira, matrícula 2023001234
Escola: EMEF Professor Silva, 5º ano
Notas: Matemática 8,5, Português 7,0
Nome da mãe: Ana Pereira
Endereço: Rua da Escola, 456

Depois (dados anonimizados):
Aluno: [anonimizado]
Escola: Escola pública municipal, 5º ano
Média da turma: 7,8
Taxa de aprovação: 92%
Distribuição de notas por faixa: 0-5: 8%, 5-7: 25%, 7-9: 45%, 9-10: 22%
[Dados individuais e endereço removidos]
```

#### Exemplo 3: Dados de mobilidade urbana
```markdown
Cenário: Prefeitura quer planejar melhorias no transporte público

Antes (dados individuais - bilhetagem eletrônica):
Usuário: Carlos Santos, CPF 456.789.123-00
Cartão: 1234-5678-9012-3456
Trajeto: 08:15 - Linha 101 (Casa → Trabalho)
17:45 - Linha 101 (Trabalho → Casa)
Recarga: R$ 50,00 em 05/05/2024

Depois (dados anonimizados - análise de fluxo):
Hora: 08:00-09:00, Linha 101, Sentido Bairro-Centro: 234 passageiros
Hora: 17:00-18:00, Linha 101, Sentido Centro-Bairro: 289 passageiros
Ponto mais movimentado: Terminal Central (1.234 embarques/dia)
Tempo médio de viagem: 45 minutos
[Dados individuais e forma de pagamento removidos]
```

#### Exemplo 4: Dados de programas sociais
```markdown
Cenário: Ministério quer avaliar impacto do Bolsa Família

Antes (dados cadastrais):
Beneficiário: Maria da Silva, NIS 1234567890
Endereço: Rua Projetada, 789, Comunidade São João
Composição familiar: 4 pessoas (2 adultos, 2 crianças)
Renda declarada: R$ 350,00
Benefício: R$ 600,00

Depois (dados anonimizados para pesquisa):
Região: Nordeste, Zona urbana
Composição familiar média: 3,8 pessoas
Renda média declarada: R$ 380,00
Benefício médio: R$ 620,00
Perfil: 78% chefiado por mulheres
[Dados individuais e localização exata removidos]
```

## ⚖️ Cuidados legais e riscos

### Risco de reidentificação
Dados aparentemente anônimos podem permitir identificação quando combinados com outras bases.

**Exemplos clássicos de reidentificação:**

1. **Estudo de Latanya Sweeney (2000)**
   - 87% da população americana pode ser identificada com (CEP + data de nascimento + sexo)
   - O então governador de Massachusetts foi identificado em dados "anônimos" de saúde

2. **Netflix Prize (2006)**
   - Pesquisadores reidentificaram usuários cruzando dados "anônimos" do Netflix com IMDb
   - Mesmo sem nomes, padrões de avaliação identificavam pessoas

3. **Dados de táxi em Nova York (2014)**
   - Dados de corridas foram reidentificados cruzando com fotos de paparazzi
   - Celebridades tiveram trajetos expostos

### Fatores que aumentam risco de reidentificação

| Fator | Descrição | Exemplo |
|-------|-----------|---------|
| **Pouca generalização** | Dados muito precisos | CEP completo, idade exata |
| **Combinação de atributos** | Vários campos juntos | Profissão + bairro + idade |
| **Dados raros** | Valores incomuns | Doença rara, profissão específica |
| **Bases externas disponíveis** | Outros dados públicos | Redes sociais, cadastros |
| **Série temporal** | Múltiplas medições | Histórico de localização |

### Boas práticas para evitar reidentificação

1. **Avaliar risco residual**
   - Considerar outras bases de dados disponíveis publicamente
   - Analisar combinações possíveis de atributos
   - Testar com amostra antes de publicar

2. **Documentar processo**
   - Técnica utilizada e parâmetros aplicados
   - Decisões sobre níveis de generalização
   - Riscos identificados e mitigados

3. **Revisar periodicamente**
   - Novas técnicas podem permitir reidentificação
   - Novas bases de dados podem ser publicadas
   - Atualizar anonimização conforme necessário

4. **Adotar camadas de proteção**
   - Combinar múltiplas técnicas
   - Quanto mais sensível o dado, mais proteção
   - Considerar acesso controlado mesmo para anonimizados

### Termo de responsabilidade
Para acesso a dados anonimizados, considerar:

```markdown
TERMO DE RESPONSABILIDADE PARA USO DE DADOS ANONIMIZADOS

O usuário declara que:
1. Não tentará reidentificar os titulares dos dados
2. Não cruzará os dados com outras bases para fins de identificação
3. Utilizará os dados apenas para a finalidade declarada
4. Comunicará imediatamente se identificar algum indivíduo acidentalmente
5. Responsabiliza-se por eventuais danos decorrentes de reidentificação

Ciência: __________________________
Data: ___/___/___
```

## 📋 Processo de anonimização passo a passo

### Fase 1: Planejamento

1. **Identificar finalidade do uso**
   - Para que os dados serão utilizados?
   - Qual nível de detalhe é necessário?
   - Quem serão os usuários dos dados?

2. **Mapear dados originais**
   - Listar todos os campos da base
   - Identificar identificadores diretos (nome, CPF, matrícula)
   - Identificar identificadores indiretos (data, local, cargo)
   - Classificar dados sensíveis

3. **Definir técnica adequada**
   - Qual técnica melhor atende à finalidade?
   - Combinar múltiplas técnicas se necessário
   - Definir parâmetros (k para k-anonimato, níveis de generalização)

### Fase 2: Execução

1. **Remover identificadores diretos**
   - Eliminar campos como nome, CPF, RG
   - Substituir por IDs internos se necessário (pseudonimização)

2. **Generalizar identificadores indiretos**
   - Transformar datas em meses ou anos
   - Converter CEP em região ou bairro
   - Agrupar idades em faixas etárias

3. **Aplicar técnicas adicionais**
   - Adicionar ruído em dados numéricos (se aplicável)
   - Garantir k-anonimato
   - Verificar l-diversidade para dados sensíveis

4. **Verificar qualidade**
   - Testar risco de reidentificação
   - Validar se mantém utilidade para finalidade
   - Ajustar parâmetros se necessário

### Fase 3: Documentação e controle

1. **Documentar processo**
   - Técnicas e parâmetros utilizados
   - Decisões tomadas
   - Riscos residuais identificados

2. **Estabelecer controles**
   - Quem terá acesso aos dados anonimizados?
   - Haverá termos de responsabilidade?
   - Como será feito o controle de acesso?

3. **Revisão periódica**
   - Agenda de revisão (anual ou semestral)
   - Acompanhar novas técnicas e bases de dados
   - Atualizar anonimização se necessário

## ✅ Checklist completo para anonimização

### Antes de anonimizar
- [ ] Finalidade do uso está claramente definida?
- [ ] Todos os identificadores diretos foram mapeados?
- [ ] Todos os identificadores indiretos foram mapeados?
- [ ] Dados sensíveis foram identificados?
- [ ] Técnica mais adequada foi selecionada?
- [ ] Parâmetros foram definidos (k, níveis de generalização)?

### Durante a anonimização
- [ ] Identificadores diretos foram removidos?
- [ ] Identificadores indiretos foram generalizados?
- [ ] Generalização mantém utilidade para finalidade?
- [ ] K-anonimato foi verificado (se aplicável)?
- [ ] L-diversidade foi verificada (se aplicável)?
- [ ] Ruído foi adicionado adequadamente (se aplicável)?
- [ ] Agregação foi feita corretamente (se aplicável)?

### Após a anonimização
- [ ] Teste de reidentificação foi realizado?
- [ ] Risco residual é aceitável?
- [ ] Processo foi documentado?
- [ ] Versão original está armazenada com segurança?
- [ ] Controles de acesso estão definidos?
- [ ] Termos de uso foram preparados?

### Para publicação/compartilhamento
- [ ] Finalidade está clara para os usuários?
- [ ] Termo de responsabilidade será assinado?
- [ ] Há contato para reportar problemas?
- [ ] Data de revisão foi definida?
- [ ] Responsável pela revisão foi designado?

## 📊 Exemplo completo passo a passo

### Cenário: Base de pacientes de um hospital

**Dados originais (parcial):**
| ID | Nome | CPF | Idade | Cidade | Diagnóstico | Data |
|----|------|-----|-------|--------|-------------|------|
| 1 | Ana Silva | 123.456.789-00 | 35 | São Paulo | Hipertensão | 10/03/2024 |
| 2 | Carlos Lima | 987.654.321-00 | 42 | Guarulhos | Diabetes | 12/03/2024 |
| 3 | Maria Souza | 456.789.123-00 | 28 | São Paulo | Asma | 15/03/2024 |
| 4 | Pedro Santos | 789.123.456-00 | 51 | Osasco | Hipertensão | 18/03/2024 |
| 5 | Ana Costa | 321.654.987-00 | 39 | São Paulo | Diabetes | 20/03/2024 |

### Passo 1: Identificar campos

| Campo | Tipo | Ação |
|-------|------|------|
| ID | Interno | Manter (pseudonimização) |
| Nome | Identificador direto | Remover |
| CPF | Identificador direto | Remover |
| Idade | Identificador indireto | Generalizar |
| Cidade | Identificador indireto | Generalizar |
| Diagnóstico | Dado sensível | Categorizar |
| Data | Identificador indireto | Generalizar |

### Passo 2: Aplicar técnicas

**Generalização:**
- Idade → Faixa etária (30-39, 40-49, 50-59)
- Cidade → Região (Capital, Grande SP, Interior)
- Data → Mês/Ano

**Categorização de diagnóstico:**
- Hipertensão, Diabetes → Doença crônica
- Asma → Doença respiratória

### Passo 3: Resultado anonimizado

| ID | Faixa etária | Região | Diagnóstico | Mês |
|----|--------------|--------|-------------|-----|
| 1 | 30-39 | Capital | Crônica | Mar/24 |
| 2 | 40-49 | Grande SP | Crônica | Mar/24 |
| 3 | 20-29 | Capital | Respiratória | Mar/24 |
| 4 | 50-59 | Grande SP | Crônica | Mar/24 |
| 5 | 30-39 | Capital | Crônica | Mar/24 |

### Passo 4: Verificar k-anonimato (k=2)

| Grupo | Faixa etária | Região | Diagnóstico | Contagem |
|-------|--------------|--------|-------------|----------|
| A | 30-39 | Capital | Crônica | 2 (OK) |
| B | 40-49 | Grande SP | Crônica | 1 (risco) |
| C | 20-29 | Capital | Respiratória | 1 (risco) |
| D | 50-59 | Grande SP | Crônica | 1 (risco) |

### Passo 5: Ajustar para garantir k=2

Nova generalização:
- Unificar "Grande SP" e "Capital" em "Região Metropolitana"
- Agrupar faixas etárias adjacentes

**Resultado final:**
| ID | Faixa etária | Região | Diagnóstico | Mês |
|----|--------------|--------|-------------|-----|
| 1 | 30-49 | RM SP | Crônica | Mar/24 |
| 2 | 30-49 | RM SP | Crônica | Mar/24 |
| 3 | 20-39 | RM SP | Respiratória | Mar/24 |
| 4 | 40-59 | RM SP | Crônica | Mar/24 |
| 5 | 30-49 | RM SP | Crônica | Mar/24 |

Verificação final (k=2):
- Grupo Crônica 30-49 RM SP: 3 registros ✓
- Grupo Respiratória 20-39 RM SP: 1 registro (risco)
- Grupo Crônica 40-59 RM SP: 1 registro (risco)

### Passo 6: Considerar l-diversidade

Para os grupos com 1 registro, considerar se diagnóstico é muito sensível. Se sim, pode ser necessário agregação ainda maior ou não publicar esses registros.

## 📚 Legislação e normas relacionadas

### LGPD (Lei 13.709/2018)
- **Art. 5º, III:** Define dado anonimizado
- **Art. 12:** Diz que dados anonimizados não são considerados pessoais
- **Art. 12, §2º:** Estabelece que se houver esforço razoável para reidentificar, volta a ser pessoal

### Marco Civil da Internet (Lei 12.965/2014)
- **Art. 7º:** Direitos dos usuários, incluindo privacidade
- **Art. 11:** Guarda de registros

### Decretos e normas
- **Decreto 8.777/2016:** Política de Dados Abertos
- **Decreto 10.046/2019:** Compartilhamento de dados no governo

## 🎓 Glossário

| Termo | Definição |
|-------|-----------|
| **Anonimização** | Processo irreversível de tornar dados não identificáveis |
| **Pseudonimização** | Substituição por código, mas com possibilidade de reversão |
| **Reidentificação** | Processo de identificar um indivíduo em dados anônimos |
| **K-anonimato** | Garantia que cada registro é igual a k-1 outros |
| **L-diversidade** | Garantia de diversidade em valores sensíveis |
| **Identificador direto** | Campo que identifica unicamente (nome, CPF) |
| **Identificador indireto** | Campo que em combinação pode identificar (idade, CEP) |
| **Dado sensível** | Dado com proteção especial (saúde, religião) |

## 📌 Pontos-chave para servidores

### Lembre-se sempre:
1. ✅ **Dados anonimizados NÃO são dados pessoais**
2. ⚠️ **Mas precisam ser realmente anônimos**
3. 🔍 **Risco de reidentificação deve ser avaliado**
4. 📝 **Documente todo o processo**
5. 🔄 **Revise periodicamente**
6. 📊 **Use técnica adequada à finalidade**
7. 🔒 **Proteja a base original com dados pessoais**

### Erros comuns a evitar:
❌ Achar que remover nome é suficiente
❌ Publicar dados sem testar reidentificação
❌ Usar pseudonimização achando que é anonimização
❌ Ignorar identificadores indiretos
❌ Não documentar o processo

**[⬆ Voltar ao topo](#)**
```

Este arquivo está **completo e unificado**, com:
- ✅ Definição legal e conceitos
- ✅ Todas as técnicas de anonimização detalhadas
- ✅ Comparativo com pseudonimização
- ✅ Exemplos práticos no setor público
- ✅ Riscos e cuidados legais
- ✅ Processo passo a passo
- ✅ Checklist completo
- ✅ Exemplo prático detalhado
- ✅ Legislação e glossário
