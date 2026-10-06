# Estatística para Pesquisadores

Site estático de **47 calculadoras estatísticas** que rodam **100% no navegador**, sem login e sem envio dos dados. Interface em português (pt-BR), com separador decimal configurável (vírgula por padrão), saída em **Markdown** pronta para colar em relatórios, e, em cada página, fórmula, exemplo prático, instruções para execução em R (via Google Colab), quando usar e referências bibliográficas.

## Créditos e Bibliografia de Referência

A fundamentação teórica, exemplos práticos e sintaxe de códigos em R foram referenciados a partir do livro:

> [**Louzada, F., Ferreira, P. H., & Ramos, P. L. (2026).** *Estatística Básica com Suporte Computacional*. São Carlos: Edição dos Autores. ISBN 978-65-02-13968-4.](https://cemeai.icmc.usp.br/pesquisadores-brasileiros-lancam-livro-gratuito-de-estatistica-basica-com-suporte-computacional-em-portugues-e-espanhol/)

O material original do livro encontra-se disponível no diretório `bibliografia/Livro-Estatistica-Basica-R-Portugues.pdf`.

## Suporte à Linguagem R e Google Colab

Cada calculadora do site conta com uma seção dedicada contendo a instrução em R para replicação exata do cálculo.

Para facilitar o uso por pesquisadores e leigos, o site disponibiliza um tutorial passo-a-passo na página [`instrucoes-r-colab.html`](instrucoes-r-colab.html) ensinando como utilizar o **Google Colab** gratuitamente na nuvem para rodar R via integração com `%load_ext rpy2.ipython` e `%%R`.

## Como usar / hospedar

Por ser um site estático, basta abrir `index.html` em qualquer navegador moderno ou publicar a pasta do repositório em provedores de hospedagem estática (como GitHub Pages, Vercel ou Netlify). Não há tempo de compilação (*build*) nem dependências externas em tempo de execução.

## Estrutura do Repositório

```
index.html                 página inicial (resumos das categorias e links)
instrucoes-r-colab.html    tutorial passo-a-passo para uso do R no Google Colab
<slug>.html                páginas das calculadoras estatísticas
css/estilo.css             estilização (tema claro, bege + verde-escuro, sidebar)
js/utils.js                funções de parsing, separador decimal e formatação
js/stats.js                núcleo de cálculos estatísticos em JavaScript puro
js/stats_extra.js          módulos extras (regressão logística, Cronbach, epi 2x2)
js/calculators.js          registro e definição dos campos e saídas das calculadoras
js/app.js                  mecanismo de UI (sidebar, montagem dinâmica e Markdown)
bibliografia/              livro de referência em PDF e artigos metodológicos
```

## Cobertura (grupos)

- **Estatística Descritiva (15):** Média Aritmética, Média Geométrica e Harmônica, Mediana, Moda, Desvio Padrão, Variância, Quartis, Amplitude, Coeficiente de Variação, Assimetria e Curtose, Tabela de Frequências, Histograma, Boxplot, Correlação de Pearson, Tamanho do Efeito.
- **Probabilidade (8):** Distribuição Normal, Distribuição Binomial, Distribuição de Poisson, Distribuição t de Student, Distribuição Qui-Quadrado, Distribuição F de Snedecor, Tabela Normal (Z), Gerador de Números Aleatórios.
- **Inferência (16):** Intervalo de Confiança para a Média, Tamanho de Amostra, Teste t (1 Amostra), Teste t (2 Amostras), Teste t Pareado, Qui-Quadrado, ANOVA (1 Fator), Regressão Linear Simples, Regressão Logística, Teste de Normalidade, Teste F de Homocedasticidade, Teste Exato de Fisher, Testes Z para Proporções, Tamanho do Efeito, Correlação de Spearman.
- **Não Paramétricos (7):** Teste de Wilcoxon, Teste de Mann-Whitney, Teste de Kruskal-Wallis, Teste de Friedman, Correlação de Spearman, Qui-Quadrado, Teste Exato de Fisher.
- **Multivariada (5):** Matriz de Correlação, Análise de Componentes Principais (PCA), Regressão Múltipla, Regressão Linear Simples, Alfa de Cronbach.
- **Outras Ferramentas (6):** Epidemiologia 2x2, Alfa de Cronbach, Gerador de Números Aleatórios, Tabela Normal (Z), Conversor de Dados, Teste de Normalidade.

## Ressalvas e Transparência

- **Cálculo local:** Todos os cálculos são processados 100% no navegador do usuário via JavaScript. Nenhum dado é enviado para servidores externos.
- **Finalidade educacional e de pesquisa:** Ferramenta desenvolvida para apoio ao ensino e à pesquisa acadêmica. Para tomada de decisões críticas, recomenda-se a conferência dos resultados com softwares estatísticos oficiais (como R).
