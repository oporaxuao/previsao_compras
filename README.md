🛒 Previsão de Compra Web: Otimização de Campanhas de Marketing
📖 Sobre o Projeto
Neste projeto de Data Science, o objetivo é resolver um problema real e recorrente no varejo: a ineficiência nos gastos com campanhas de marketing. Quando promoções e comunicações são enviadas para toda a base de clientes indiscriminadamente, o Retorno sobre Investimento (ROI) cai e os clientes ficam insatisfeitos com o excesso de ofertas irrelevantes.

A solução desenvolvida foi a criação de um modelo preditivo de classificação binária capaz de identificar com alta precisão o perfil do cliente e prever se ele realizará uma compra no canal web (WebPurchases = 1 ou 0). Isso permite que a empresa direcione os esforços de marketing apenas para o público com real propensão de conversão.

O projeto abrange a construção de um pipeline de dados completo: desde a Análise Exploratória (EDA) e Feature Engineering, passando pela modelagem com algoritmos avançados de Machine Learning, até a tradução das métricas técnicas em recomendações práticas de negócio.

🛠️ Tecnologias e Ferramentas Utilizadas
Linguagem: Python

Manipulação e Limpeza de Dados: Pandas, NumPy

Visualização de Dados e Storytelling: Matplotlib, Seaborn

Machine Learning & Modelagem Preditiva: Scikit-Learn, XGBoost, Random Forest

Métricas de Avaliação: F1-Score, AUC-ROC, Matriz de Confusão, Feature Importance

📊 Principais Insights (EDA)
Durante a exploração dos dados, descobrimos padrões cruciais sobre o comportamento dos consumidores:

Renda e Gasto: Clientes que compram online possuem uma renda mediana significativamente maior (US$ 64.006 contra US$ 36.640 dos não-compradores).

O Poder dos Vinhos: Os gastos com vinhos representam cerca de 55% do gasto total médio da base, tornando-se o produto âncora para estratégias de upselling.

Impacto Familiar: Ter filhos em casa reduz drasticamente a propensão de compra online (a taxa cai de 68.4% em clientes sem filhos para cerca de 23.9% em clientes com dois filhos).

Recência: O tempo decorrido desde a última compra não se mostrou um discriminador forte entre os grupos, indicando que o volume e o padrão financeiro de gastos ditam a conversão mais do que o timing.

🤖 Modelagem e Resultados
Foram treinados, avaliados e comparados dois modelos baseados em Ensemble (árvores de decisão): Random Forest e XGBoost.

O XGBoost apresentou a melhor performance, demonstrando excelente capacidade de identificar os compradores reais sem gerar um volume excessivo de falsos positivos para a equipe de marketing.

Métricas do Modelo Vencedor (XGBoost no conjunto de teste):

F1-Score: 0.9322

AUC-ROC: 0.9791

Acurácia: 92.86%

Taxa de Captura: O modelo identificou corretamente 96.9% dos compradores reais.

💡 Recomendações de Negócio
A partir da análise de Feature Importance (onde Gasto Total e Gasto em Vinhos foram os fatores mais determinantes), as seguintes ações táticas foram sugeridas:

Campanha Premium de Vinhos: Focar nos clientes com alto score no modelo e sem filhos em casa, maximizando a taxa de conversão e o ticket médio.

Retenção com Descontos: Direcionar ofertas específicas para clientes com score médio e com filhos, visando evitar o churn motivado por mudança nas prioridades de consumo da família.

Migração para o Digital: Realizar testes A/B com clientes que possuem alto volume de compras em lojas físicas, oferecendo incentivos exclusivos para a primeira compra na web.

🚀 Próximos Passos
Otimização avançada de hiperparâmetros utilizando bibliotecas como GridSearchCV ou Optuna.

Avaliação de técnicas de geração de dados sintéticos (como SMOTE) caso o comportamento da base mude e se torne mais desbalanceado com o tempo.

Deploy do modelo através de uma API (por exemplo, usando FastAPI) para realizar o scoring dos clientes em tempo real.
