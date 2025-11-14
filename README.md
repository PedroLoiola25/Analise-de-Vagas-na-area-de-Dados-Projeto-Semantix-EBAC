# Análise de Habilidades no Mercado de Dados

Este projeto foi desenvolvido como parte da parceria EBAC x Semantix, com o objetivo de aplicar as etapas de um projeto real de Análise de Dados, desde a coleta e limpeza até a visualização final no Looker Studio.

O tema escolhido é o **mercado de trabalho na área de dados**. Um assunto que, além de atual, faz parte da minha própria jornada de transição de carreira.

---

## 1. Dissertação sobre o Problema

Durante minha transição de carreira para a área de Análise de Dados, notei uma dificuldade muito comum entre iniciantes: saber **quais habilidades realmente importam** para conseguir uma vaga.

Ao pesquisar vagas no LinkedIn, Indeed e Glassdoor, percebi que cada anúncio usa uma linguagem diferente, lista ferramentas variadas e destaca competências de formas pouco padronizadas. Isso dificulta muito saber por onde começar a estudar ou o que priorizar na preparação.

Por isso, decidi realizar este projeto: reunir dados reais de vagas da área, identificar as hard skills e soft skills mais citadas e consolidar tudo em um painel visual simples, direto e útil para quem está entrando nesse mercado — inclusive eu.

Além disso, por ser meu primeiro projeto de análise de dados, pude perceber como a qualidade e a estrutura das bases influenciam no que é possível analisar. As fontes públicas nem sempre trazem informações completas ou padronizadas, e esse entendimento foi essencial para mim.

---

## 2. Fontes de Dados Utilizadas

Foram utilizadas bases públicas e uma API aberta, sempre respeitando os termos de uso das plataformas:

| Fonte | Descrição | Método de Coleta |
|-------|------------|------------------|
| Kaggle – *Job Postings on LinkedIn for Data Roles* | Dataset com descrições de vagas da área de dados. | Download (CSV) |
| Glassdoor Jobs Dataset | Contém cargos, empresas, salários e descrições. | Download direto (CSV) |
| Indeed Job Postings Dataset (2024) | Vagas de tecnologia com detalhes textuais. | Download direto (CSV) |
| RapidAPI – *JSearch API* | Retorna vagas em tempo real, com descrições e requisitos. | Coleta via `requests` em Python |

Cada fonte possui estrutura diferente. Por isso, foi necessário um processo de padronização antes da análise.

---

## 3. Limpeza e Unificação dos Dados

O principal objetivo da limpeza foi transformar vários datasets diferentes em **uma única tabela padronizada**, com as seguintes colunas:

title | company | employment_type | description | location | date_posted | salary | link | source


As etapas incluíram:

- renomear colunas para um padrão único;
- remover duplicatas entre bases diferentes;
- criar a coluna `source` para indicar a origem de cada registro;
- tratar valores ausentes (como tipo de emprego e salário);
- unificar tudo em um único DataFrame.

**Resultado final:**  
> **5.167 registros** consolidados e prontos para análise.

---

## 4. Análise Exploratória (EDA)

A análise foi feita em Python usando Pandas, Regex, Matplotlib e Seaborn, respondendo perguntas essenciais para entender as tendências do mercado.

---

### a) Quais são os cargos mais comuns?

| Cargo | Quantidade |
|-------|-------------|
| Data Analyst | 404 |
| Data Scientist | 352 |
| Data Engineer | 323 |
| Senior Data Scientist | 93 |
| Machine Learning Engineer | 68 |

---

### b) Quais são as hard skills mais pedidas?

| Skill | Frequência |
|--------|-------------|
| Python | 2769 |
| SQL | 2645 |
| Machine Learning | 1749 |
| Statistics | 1592 |
| R | 1524 |
| Tableau | 949 |
| Power BI | 417 |

---

### c) Quais são as soft skills mais valorizadas?

| Soft Skill | Frequência |
|-------------|------------|
| Comunicação | 2903 |
| Criatividade | 1812 |
| Liderança | 1548 |
| Colaboração | 1430 |
| Resolução de Problemas | 1315 |
| Adaptabilidade | 1013 |

---

## 5. Relatório de Insights

Principais conclusões:

- O mercado de dados é amplo e diversificado.  
- Python e SQL dominam praticamente todas as descrições.  
- Machine Learning e Estatística aparecem com grande relevância.  
- Soft skills como Comunicação, Criatividade e Liderança são essenciais.  
- Empresas buscam profissionais capazes de interpretar e explicar dados.

---

## 6. Visualização de Dados (Looker Studio)

O dashboard foi construído no **Looker Studio**, com gráficos organizados por tema:

- Cargos mais ofertados  
- Hard skills mais pedidas  
- Soft skills mais mencionadas  
- Empresas que mais contratam  
- Tabela filtrável  
- Comparação entre fontes  

**Dashboard completo:**  
https://lookerstudio.google.com/reporting/36dc484a-ee74-4caa-b858-1bfd3724ac66

---

## 7. Conclusão

Este projeto me permitiu colocar em prática todo o processo de análise de dados — desde a coleta até a apresentação final.

Aprendi muito sobre padronização e sobre como a qualidade das bases impacta diretamente nos resultados.  
Esse trabalho representa meu **primeiro passo oficial na área de dados**, e espero que também ajude outras pessoas que estão começando.

---

## 8. Tecnologias Utilizadas

- Python (Pandas, NumPy, Seaborn, Matplotlib, Regex)  
- Google Colab  
- Looker Studio  
- RapidAPI – JSearch  
- Datasets do Kaggle  
- GitHub  

---

## Autor

**Pedro Loiola**  
📍 Palmas – TO  
🎯 Em transição de carreira para Análise de Dados  
🔗 www.linkedin.com/in/pedro-loiola-246938309
