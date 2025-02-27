Este repositório contém um notebook Python que implementa uma análise avançada de intervenções para ansiedade utilizando SHAP (SHapley Additive exPlanations) para quantificar a importância de diferentes características na predição dos níveis de ansiedade pós-intervenção.

## Visão Geral

O notebook adapta uma estrutura de Mixture of Experts (MoE) para integrar valores SHAP, permitindo uma compreensão granular dos fatores que impulsionam o sucesso de intervenções para ansiedade. Este método possibilita identificar quais características (como grupo de tratamento e nível de ansiedade pré-intervenção) contribuem mais significativamente para os resultados observados após a intervenção.

## Fluxo de Trabalho

1. **Carregamento e Validação de Dados**
   - Carregamento de dados sintéticos de intervenção para ansiedade
   - Validação rigorosa da estrutura, conteúdo e tipos de dados
   - Tratamento adequado de possíveis erros durante o processo

2. **Cálculo de Valores SHAP**
   - Computação de valores SHAP para avaliar a importância das características
   - Explicações detalhadas e tratamento de erros durante o cálculo
   - Visualização dos resultados de valores SHAP

3. **Visualização de Dados**
   - Geração de gráficos KDE (Kernel Density Estimation)
   - Criação de gráficos Violin Plot para distribuição por grupos
   - Implementação de gráficos de Coordenadas Paralelas
   - Desenvolvimento de Hipergrafos para análise de relacionamentos
   - Tratamento detalhado de erros de visualização

4. **Resumo Estatístico**
   - Realização de análise bootstrap para robustez estatística
   - Geração de estatísticas descritivas
   - Validação de resultados estatísticos

5. **Relatório de Insights via LLMs**
   - Síntese de descobertas utilizando múltiplos modelos (Grok, Claude, Grok-Enhanced)
   - Ênfase em insights baseados nos valores SHAP
   - Validação das saídas dos LLMs e tratamento de erros potenciais

## Componentes Técnicos

### Bibliotecas Principais
- `pandas`: Manipulação e processamento de dados
- `matplotlib` e `seaborn`: Visualização de dados
- `shap`: Cálculo e visualização de valores SHAP
- `scikit-learn`: Modelagem preditiva (RandomForestRegressor)
- `plotly`: Visualizações interativas avançadas
- `networkx`: Criação e visualização de grafos/hipergrafos
- `scipy`: Análises estatísticas (bootstrap)

### Componente de IA Reinforcement Learning
O notebook inclui uma implementação simplificada de um agente DDQN (Double Deep Q-Network) como demonstração de caso de uso potencial para otimização adaptativa de intervenções.

### Processamento de Dados
- Codificação one-hot de variáveis categóricas
- Escalonamento de características numéricas
- Validação extensiva de dados de entrada

### Visualizações Avançadas
- Gráficos SHAP para interpretabilidade do modelo
- Visualizações KDE para distribuições
- Violin plots para comparações entre grupos
- Coordenadas Paralelas para visualização multidimensional
- Hipergrafos para análise de relacionamentos complexos

### Análise Estatística
- Bootstrap para estimativas de intervalos de confiança
- Estatísticas descritivas detalhadas
- Quantificação de efeitos de intervenção

## Uso

1. Execute o notebook em um ambiente Python com as dependências instaladas
2. Os resultados serão salvos no diretório especificado em `OUTPUT_PATH`
3. As visualizações geradas incluem gráficos SHAP, KDE, Violin, Coordenadas Paralelas e Hipergrafos
4. Um relatório de insights consolidado será gerado combinando análises de múltiplos modelos LLM

## Notas de Implementação

- O notebook inclui tratamento abrangente de erros para robustez
- Cores neon são utilizadas para melhorar a visualização em fundo escuro
- A constante `BOOTSTRAP_RESAMPLES` controla o número de reamostragens para análise estatística
- Para ambientes Google Colab, o notebook detecta automaticamente e adapta os caminhos

## Autor

Hélio Craveiro Pessoa Júnior
