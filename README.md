# TelecomX2

*📊* Relatório de Análise de Evasão de Clientes

🔍 1. Preparação dos Dados

Coluna customerID foi removida por não contribuir para a análise.
Valores como "No internet service" foram agrupados como "No" para simplificar variáveis binárias.
Aplicado one-hot encoding para variáveis categóricas, evitando o dummy trap.

🧹 2. Tratamento de Dados

Linhas com valores nulos nas colunas Contas_Diarias e account.Charges.Total foram removidas.
Dados numéricos foram normalizados com StandardScaler.

📈 3. Seleção de Variáveis

Utilizada correlação com a variável alvo Churn_Yes para selecionar variáveis com correlação ≥ 0.2.
Análise de multicolinearidade com VIF (Variance Inflation Factor) para remover variáveis redundantes.

🤖 4. Modelagem Preditiva

Modelos utilizados:
Regressão Logística
Random Forest
Dados foram balanceados com SMOTE para lidar com desbalanceamento da classe Churn.

📊 5. Avaliação dos Modelos

Métricas utilizadas:
Acurácia
ROC AUC
Matriz de Confusão
Relatório de Classificação

🌟 6. Principais Fatores que Influenciam a Evasão
Com base na importância das variáveis do modelo Random Forest, os fatores mais relevantes (esperados) incluem:

Tipo de contrato (account.Contract)

Cobertura de segurança online (internet.OnlineSecurity)

Cobertura de suporte técnico (internet.TechSupport)

Faturamento mensal (account.Charges.Total)

Serviços de streaming (internet.StreamingTV, internet.StreamingMovies)

Método de pagamento (account.PaymentMethod)

Serviço de backup (internet.OnlineBackup)

Presença de dependentes (customer.Dependents)

Faturamento sem papel (account.PaperlessBilling)

Serviço de proteção de dispositivos (internet.DeviceProtection)

💡 Estratégias de Retenção Propostas
Com base nos fatores identificados:

1. Melhoria nos Planos de Contrato
Incentivar contratos de longo prazo com benefícios exclusivos.
2. Investimento em Serviços de Valor Agregado
Oferecer segurança online, suporte técnico e backup como parte dos pacotes.
3. Transparência e Flexibilidade no Faturamento
Reduzir surpresas no faturamento e oferecer opções de pagamento mais acessíveis.
4. Segmentação de Clientes
Criar campanhas específicas para clientes com dependentes ou que usam serviços de streaming.
5. Monitoramento Proativo
Identificar clientes com alto risco de evasão e oferecer suporte personalizado.

