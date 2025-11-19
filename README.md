# Plano de Experimento - Scoping e Planejamento
## Identiticação Básica, Contexto e Problema

# 1. Identificação básica 

### 1.1 Títutlo do experimento
Impacto do uso de ferramentas de análise estática na identificação de vulnerabilidades em projetos Node.js open source

### 1.2 Código / Id

``EXP-TCC-2025-ANALISE-ESTATICA-NODE``

### 1.3 Versão do documento

- **Versão Atual:** v1.2

### 1.4 Datas

**Data de criação:** 17/11/2025 | 
**Ultima atualização:** 19/11/2025

### 1.5 Autores

- **Autor:** Gustavo Menezes Barbosa  
 - **Curso / área:** Engenharia de Software  
  - **Instituição:** PUC Minas  
  - **E-mail:** `gustavo.barbosa.1386677@sga.pucminas.br`  

### 1.6 Responsável principal

- **Responsavel principal (PI):** Gustavo Menezes Barbosa

### 1.7 Projeto / Produto

Este experimento está relacionado à proposta de Trabalho de Conclusão de Curso (TCC) na área de **Qualidade de Software e Engenharia de Software Empírica**, com foco em:

- Avaliação do **uso de ferramentas de análise estática** (por exemplo, CodeQL, SonarQube ou ferramentas similares)  
- Aplicadas em **projetos Node.js open source hospedados em repositórios públicos (como GitHub)**  
- Para investigar o impacto dessas ferramentas na **identificação de vulnerabilidades** e **problemas de segurança** em código.

---

## 2. Contexto do problema

### 2.1 Descrição do problema / oportunidade

Projetos de software, espceialmente em ambientes colaborativos e open ource ,estão cada vez mais expostos a riscos de **vulnerabilidades de segurança** devido a:

- Crescente complexidade das aplicações;
- Uso intensivo de bibliotecas de terceiros;
- Pressão por entregas rápidas.

Ferramentas de **análise estática de código** (como CodeQL, SonarQube e outras) prometem ajudar a **identificar vulnerabilidades e defeitos mais cedo** no ciclo de desenvolvimento, sem necessidade de executar o sistema. No entanto, na prática, ainda existem dúvidas, como por exemplo:

- Em que medida essas ferramentas realmente **encontram vulnerabilidades relevantes** em projetos reais?
- Elas trazem **benefícios mensuráveis** em relação a um cenário sem uso de análise estática?
- Qual é o **tipo de vulnerabilidade** mais frequentemente detectado?
- Há impacto em termos de **quantidade de alertas** gerados e **custo de triagem**?

Diante disso, surge a **oportunidade** de planejar um experimento controlado que:

- Compare projetos com e sem uso de ferramentas de análise estática,  
  **ou**
- Compare diferentes ferramentas entre si,  
para avaliar seu impacto na identificação de vulnerabilidades em projetos Node.js open source.

O problema central pode ser resumido como:

> **Problema:** Não está claro, com base em evidências empíricas, qual é o impacto prático do uso de ferramentas de análise estática na identificação de vulnerabilidades de segurança em projetos Node.js open source, em comparação com um cenário sem essas ferramentas (ou entre diferentes ferramentas).  

Esse problema é relevante tanto para:

- **Desenvolvedores e mantenedores**, que precisam decidir se vale a pena incluir essas ferramentas na rotina de desenvolvimento;
- **Organizações**, que precisam justificar investimentos em ferramentas, infraestrutura e treinamento;
- **Comunidade acadêmica**, que busca dados empíricos para fundamentar recomendações de boas práticas.

### 2.2 Contexto organizacional e técnico

o experimento será planejado considerando o seguinte contexto:

- **Tipo de organização / ambiente:**
  - Contexto acadêmico (disciplina de Laboratório de Experimentação de Software).
  - Possível extensão para projetos reais em organizações que desenvolvem software web.
- **Domínio de aplicação:**
  - Projetos Node.js, com foco em aplicações web e APIs RESTful.
- **Ambiente técnico:**
  - Hospedagem dos repositórios em plataformas como GitHub.
  - Ferramentas de análise estática como:
    - CodeQL (consultas para detecção de vulnerabilidades);
    - SonarQube ou ferramentas similares para análise de qualidade e segurança.
- **Processo de desenvolvimento:**
  - Repositórios com histórico de commits, issues e pull requests;
  - Possível uso de **CI/CD** (GitHub Actions ou outra ferramenta) para automatizar a execução da análise estática.
- **Ferramentas complementares:**
  - Linguagens e tecnologias:
    - Node.js / JavaScript;
  - Scripts e ferramentas para coleta de dados:
    - Scripts em Python ou JavaScript para coletar métricas das ferramentas de análise;
    - Planilhas ou bancos de dados para armazenamento e análise dos resultados.

No cenário futuro do TCC, esse experimento poderá ser:

- Executado usando um conjunto de projetos selecionados a partir de critérios claros (por exemplo número mínimo de estrelas);  
- Integrado ao pipeline de desenvolvimento de uma organização.

### 2.3 Trabalhos e evidências prévias

Algumas evidências e trabalhos prévios que motivam este experimento incluem:

- **Experiências internas (disciplina / laboratório):**
  - Atividades práticas realizadas na disciplina envolvendo ferramentas de análise de código (por exemplo, uso de CodeQL, SonarQube ou ferramentas similares em repositórios de exemplo).
  - Observação empírica de que essas ferramentas geram um número significativo de alertas, mas nem sempre está claro quais são realmente relevantes do ponto de vista de segurança.

- **Evidências externas (literatura e prática de mercado):**
  - Estudos na área de **Engenharia de Software Empírica** que mostram que ferramentas de análise estática podem:
    - Detectar vulnerabilidades de forma antecipada;
    - Apoiar revisões de código;
    - Ajudar a padronizar critérios de qualidade.
  - Relatos de organizações que adotam análise estática em pipelines de CI/CD como parte de uma estratégia de **DevSecOps**.
  - Pesquisas e relatórios de segurança que mencionam:
    - A importância de automatizar a detecção de vulnerabilidades;
    - Limitações, como falsos positivos, curva de aprendizado e esforço de configuração.

Apesar dessas evidências, ainda há **lacunas específicas**, como:

- Falta de dados focados em determinados **ecosistemas tecnológicos** (por exemplo, Node.js);
- Comparações sistemáticas sobre **quantidade e tipo de vulnerabilidades encontradas** com e sem uso dessas ferramentas.

Essas lacunas motivam o planejamento de um experimento mais estruturado, que possa ser evoluído e executado no TCC.

### 2.4 Referencial teórico e empírico essencial

Para fundamentar o experimento, serão considerados pelo menos três eixos principais de referencial:

1. **Qualidade de Software e Manutenibilidade**
   - Conceitos de qualidade interna (código limpo, legibilidade, acoplamento, complexidade, etc.);
   - Relação entre qualidade interna e ocorrência de defeitos e vulnerabilidades.

2. **Engenharia de Software Empírica e Experimentos Controlados**
   - Conceitos básicos de:
     - Experimentos em Engenharia de Software;
     - Hipóteses nula e alternativa;
     - Variáveis independentes (por exemplo, uso de ferramenta X ou Y) e dependentes (por exemplo, número de vulnerabilidades identificadas, tipo de vulnerabilidade, taxa de falsos positivos);
     - Testes de hipóteses para comparar grupos ou tratamentos.
   - Boas práticas de desenho experimental:
     - Definição clara de população e amostra;
     - Procedimentos de coleta e análise de dados;
     - Cuidados com ameaças à validade (interna, externa, de construção e de conclusão).

3. **Segurança de Software e Análise Estática**
   - Conceitos básicos de vulnerabilidades em aplicações web (por exemplo, injeções, XSS, problemas de autenticação/autorização, uso inseguro de dependências);
   - Definição e funcionamento de **análise estática de código**:
     - Detecção de problemas sem executar o programa;
     - Uso de regras, consultas e modelos de fluxo de dados;
   - Estudos anteriores que:
     - Avaliam ferramentas de análise estática;
     - Discutem vantagens (por exemplo, cobertura, automação) e limitações (por exemplo, falsos positivos, dificuldade de configuração).

Esse referencial teórico e empírico servirá de base para:

- Formular a **hipótese nula** e a **hipótese alternativa** do experimento (que serão detalhadas em entregas futuras do trabalho);  
- Escolher as **métricas** a serem coletadas (por exemplo, número de vulnerabilidades encontradas, tipos de alerta, esforço de triagem);  
- Selecionar e justificar o **teste de hipóteses** mais adequado para comparar os resultados dos grupos analisados.

---

# 3. Objetivos e Questões (GQM)

## 3.1 Objetivos Geral 
**Analisar** o impacto do uso de ferramentas de análise estática (CodeQL e SonarQube)  
**com o propósito de** avaliar sua eficácia na identificação de vulnerabilidades  
**sob a perspectiva** de desenvolvedores, equipes de qualidade e gestores  
**no contexto** de projetos Node.js open source hospedados no GitHub.

---

## 3.2

**O1.** Comparar a quantidade e o tipo de vulnerabilidades detectadas entre CodeQL e SonarQube.  
**O2.** Avaliar o custo de triagem (tempo/esforço) dos alertas gerados pelas ferramentas.  
**O3.** Analisar a taxa de falsos positivos produzidos pelas ferramentas.  
**O4.** Avaliar o impacto da análise estática na qualidade geral do código (métricas internas).

## 3.3 Questões de Pesquisa (Por Objetivo)

### **01 - Comparar vulnerabilidades encontradas**

- **Q1.1:** Qual ferramenta encontra mais vulnerabilidades totais?
- **Q1.2:** Qual ferramenta encontra mais vulnerabilidades críticas ou altas?
- **Q1.3:** As ferramentas detectam os mesmos tipos de vulnerabilidades?

--- 

###  **O2 – Custo de triagem**

- **Q2.1:** Quanto tempo é gasto para revisar e classificar os alertas?
- **Q2.2:** Quantos alertas exigem intervenção manual?
- **Q2.3:** A curva de aprendizado da ferramenta impacta o tempo de triagem?

---

### **O3 – Falsos positivos**

- **Q3.1:** Qual ferramenta gera mais falsos positivos?
- **Q3.2:** Quais categorias apresentam mais falsos positivos?
- **Q3.3:** O nível de severidade influencia a taxa de falsos positivos?

---

### **O4 – Impacto na qualidade interna**

- **Q4.1:** Há redução de complexidade ciclomática após uso da ferramenta?
- **Q4.2:** O número de code smells diminui após a análise?
- **Q4.3:** A densidade de defeitos tende a diminuir com a aplicação recorrente das ferramentas?

---

### 3.4 Métricas Associadas

| Objetivo            | Pergunta            | Métrica             | Descrição             |
|---------------------|---------------------|---------------------|-----------------------|
| O1 | Q1.1 | M1 – Nº total de vulnerabilidades | Contagem total de vulnerabilidades detectadas |
| O1 | Q1.2 | M2 – Nº de vulnerabilidades críticas/altas | Quantidade de vulnerabilidades de severidade crítica/alta |
| O1 | Q1.3 | M3 – Diversidade de tipos detectados | Número de categorias diferentes detectadas por ferramenta |
| O2 | Q2.1 | M4 – Tempo de triagem (min) | Tempo gasto para revisar e classificar alertas |
| O2 | Q2.2 | M5 – Nº de alertas que exigem intervenção | Contagem de alertas marcados como “revisar manualmente” |
| O2 | Q2.3 | M6 – Tempo de aprendizado | Tempo para aprender a usar a ferramenta no nível básico |
| O3 | Q3.1 | M7 – Taxa de falsos positivos (%) | Falsos positivos ÷ alertas totais |
| O3 | Q3.2 | M8 – Falsos positivos por categoria | Contagem por tipo de vulnerabilidade |
| O3 | Q3.3 | M9 – Falsos positivos por severidade | Contagem por nível (alta, média, baixa) |
| O4 | Q4.1 | M10 – Variação da complexidade ciclomática | Diferença antes/depois da análise |
| O4 | Q4.2 | M11 – Nº de code smells | Contagem de problemas de código |
| O4 | Q4.3 | M12 – Densidade de defeitos | Defeitos ÷ LOC (linhas de código) |

---

## 3.5 Tabela Geral das Métricas

| Métrica | Descrição | Unidade |
|---------|-----------|---------|
| M1 | Nº total de vulnerabilidades identificadas pela ferramenta | contagem |
| M2 | Nº de vulnerabilidades críticas ou altas | contagem |
| M3 | Diversidade de tipos de vulnerabilidade detectados | nº de categorias |
| M4 | Tempo total requerido para triagem de alertas | minutos |
| M5 | Nº de alertas que exigem intervenção manual | contagem |
| M6 | Tempo estimado para aprendizado básico da ferramenta | horas |
| M7 | Proporção de falsos positivos sobre alertas totais | % |
| M8 | Contagem de falsos positivos por categoria | contagem |
| M9 | Falsos positivos por severidade | contagem |
| M10 | Variação da complexidade ciclomática média | pontos de complexidade |
| M11 | Contagem de code smells detectados | contagem |
| M12 | Densidade de defeitos por mil linhas de código | defeitos por KLOC |

---

# 4. Escopo e Contexto do Experimento
