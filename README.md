## Rodrigo Campos

**Engenharia e análise de dados aplicadas ao fiscal e tributário.**

Trabalho na rotina fiscal e contábil de um escritório com mais de 300 empresas clientes: Simples Nacional, MEI, obrigações acessórias, notas fiscais. Uso isso para construir sistemas de dados que respondem perguntas reais de negócio, e que rodam sozinhos, com testes e CI.

- Pipelines de dados em Python, SQL, dbt e DuckDB/PostgreSQL, com testes de qualidade que barram a publicação quando o dado vem errado
- Automação fiscal em produção: emissão de NFS-e em lote com certificado digital A1
- Modelos preditivos avaliados pelo impacto financeiro, não só pela métrica
- Formado em Análise e Desenvolvimento de Sistemas

São Paulo · aberto a oportunidades em Engenharia e Análise de Dados · [LinkedIn](https://www.linkedin.com/in/rodrigo-aparecido-397a0b154/) · [rodrigoapcampos92@gmail.com](mailto:rodrigoapcampos92@gmail.com)

---

### Projetos em destaque

#### [Radar de Empresas BR](https://github.com/RodrigoAp727/radar-de-empresas) · [dashboard](https://rodrigoap727.github.io/radar-de-empresas/)

Pipeline mensal sobre a base pública do CNPJ da Receita Federal: 73 milhões de estabelecimentos, processados com Python, DuckDB e dbt (bronze → silver → gold), agendados no GitHub Actions e publicados num dashboard aberto.

- **Achado:** 464 mil "fechamentos voluntários" num único dia (31/12/2024) eram CNPJs de campanha eleitoral. Sem esse filtro, os fechamentos do último ano pareceriam estáveis (-1%), quando na verdade subiram 16%.
- A Receita declarou 1,7 milhão de empresas inaptas entre maio e agosto de 2026, um movimento que não aparece em quem conta só as baixas.
- Os testes de qualidade pegaram uma empresa duplicada na origem e barraram a publicação. A regra de dígito verificador já cobre o CNPJ alfanumérico (IN RFB 2.229/2024).

`Python` `DuckDB` `dbt` `GitHub Actions` `Evidence`

#### [Automação de NFS-e (Nota Paulistana)](https://github.com/RodrigoAp727/automacao-nfse-sp)

Emissão de NFS-e em lote no webservice SOAP da Prefeitura de São Paulo, cada prestador com o próprio certificado ICP-Brasil A1. Construído para um escritório de contabilidade real com quase 300 clientes ativos.

- Especificação oficial incompleta: o WSDL só é acessível via mTLS, então validei cada suposição contra os XSDs oficiais e o servidor de produção.
- Bugs reais encontrados e cobertos por testes de regressão: namespace que quebrava a canonicalização da assinatura, SOAP 1.2 não documentado, identidade do certificado diferente do CNPJ do cliente (erro 1100).

`Python` `XML-DSig` `SOAP` `lxml` `Flask` `pytest`

#### [Previsão de cancelamento de cartões](https://github.com/RodrigoAp727/previsao-cancelamento-cartoes)

Quem vai cancelar, por quê e quanto vale agir antes. Modelo de gradient boosting (ROC-AUC 0,993) e simulação financeira da campanha de retenção: contatando 19% da base, alcança 96% dos cancelamentos, com lucro estimado 3,2 vezes maior que o de uma regra simples. Entrega uma fila de clientes em risco, com os motivos de cada alerta.

`Python` `scikit-learn` `pytest` `GitHub Actions`

#### [Smart Retail Analytics](https://github.com/RodrigoAp727/smart-retail-analytics)

Pipeline ETL de vendas com modelo estrela em PostgreSQL, histórico SCD Tipo 2 e upsert idempotente, que permite reprocessar e fazer backfill sem duplicar dados. Containerizado, testado e com CI.

`Python` `PostgreSQL` `Docker` `pytest`

---

### Outros projetos

- [DataSentinel](https://github.com/RodrigoAp727/datasentinel-analytics-pipeline): monitoramento de qualidade de dados com detecção de anomalias, relatórios executivos e alertas.
- [Análise financeira de e-commerce](https://github.com/RodrigoAp727/Analise-Financeira-Ecommerce): ETL, previsão de receita e simulador de impacto em margem sobre a base da Olist.
- [FutPass](https://github.com/RodrigoAp727/FutPass_App): sistema de gestão de escolinhas de futebol em produção, com Node.js e MongoDB.

---

### Stack

- **Dados:** Python · SQL · dbt · DuckDB · PostgreSQL · Pandas · scikit-learn · Power BI
- **Engenharia:** GitHub Actions · Docker · pytest · ruff · Git
- **Aplicações:** Flask · Node.js · React
