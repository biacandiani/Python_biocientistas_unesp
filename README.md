# 🧬 Introdução à Programação Python para Biocientistas

Bem-vindos ao repositório da disciplina de introdução à programação em Python, voltada para a pós-graduação em Ciências Farmacêuticas (FCF/UNESP). 

Este material foi desenvolvido para demonstrar como a programação pode ser uma ferramenta indispensável no dia a dia do biocientista, facilitando análises de dados, automação de tarefas e modelagem de bioprocessos.

## 📚 Conteúdo da Aula 01

Neste primeiro módulo, focamos na ambientação e nos conceitos básicos da linguagem, sempre com aplicações voltadas para a biotecnologia:

* **O Ecossistema Python na Ciência:** Mostra a potencialidade das bibliotecas como Biopython, Pandas e NumPy.
* **O Ambiente Google Colab:** Como utilizar a ferramenta como um verdadeiro Caderno de Laboratório Eletrônico (inserção de textos em Markdown, equações em LaTeX e imagens).
* **Fundamentos da Linguagem:**
  * Operações matemáticas básicas e variáveis.
  * Operadores lógicos (aplicados ao controle de parâmetros em biorreatores).
  * Manipulação de Strings e *slicing*.
  * Formatação moderna de textos (f-strings) para relatórios experimentais.
* **Exercícios Práticos:**

## 📚 Conteúdo da Aula 02

* **Aplicação Prática:** Calculadora de Índice de Massa Corporal (IMC) com classificação automática do indivíduo (Abaixo do peso, normal, sobrepeso, etc).

**Laços de Repetição (*Loops*)**
* Uso da estrutura `while` para repetições baseadas em condições (ex: contagem regressiva de um foguete).
* Uso da estrutura `for` com a função `range()` para iterar sobre listas de dados.
* Conceitos fundamentais de **contadores** e **acumuladores** (ex: cálculo do fatorial de um número).
* Como interromper repetições infinitas ou baseadas em gatilhos utilizando o comando `break`.

### Desafio Prático: Simulador de Crescimento Microbiano
No fim do notebook, consolidamos o aprendizado com um desafio aplicado à Engenharia de Bioprocessos. O aluno deve interagir com um algoritmo que estima o crescimento exponencial de uma cultura celular, calculando quantas gerações são necessárias para que um inóculo inicial atinja uma população alvo específica.

## 📚 Conteúdo da Aula 03 -Funções, NumPy e Matplotlib para Biocientistas

Nesta terceira aula, avançamos para a automação de cálculos e a visualização de dados científicos, saindo do Python básico e entrando no ecossistema de bibliotecas essenciais para a engenharia e as ciências biológicas.

### 📌 Tópicos Abordados

*   **Funções (Automatizando Cálculos Repetitivos):**
    *   Conceito de encapsulamento: como criar "máquinas" que recebem parâmetros, processam dados e retornam resultados (`return`).
    *   Aplicações práticas: funções genéricas para cálculos de dimensionamento (volumes de reatores cilíndricos) e propriedades geométricas complexas (análise de esferas).
    *   Uso de *docstrings* para documentação de código e formatação avançada de *strings* (ex: exibição correta de expoentes e símbolos como $m^2$ e $\pm$).

*   **Introdução ao NumPy (O Motor Numérico):**
    *   O conceito de bibliotecas e a limitação das listas nativas do Python para matemática.
    *   `np.array()`: Transformação de dados brutos (ex: triplicatas de laboratório) em vetores matemáticos de alto desempenho.
    *   **Geração de Dados:** Uso de `np.linspace()` para criar eixos contínuos para modelos teóricos e `np.arange()` para simular cronogramas de amostragem por passos.
    *   **Estatística de Bancada:** Tratamento rápido de dados experimentais utilizando `np.mean()` (média) e `np.std()` (desvio padrão).

*   **Visualização de Dados com Matplotlib:**
    *   **Gráficos 2D Clássicos (`plot`):** Construção passo a passo de cinéticas de crescimento celular (tempo vs. densidade óptica), adicionando rótulos, títulos e grades.
    *   **Abordagem Orientada a Objetos (`fig, ax`):** O padrão ouro para plotar múltiplas curvas no mesmo eixo e criar gráficos com qualidade de artigo científico.
    *   **Histogramas (`hist`):** Análise estatística e distribuição de frequências, com exemplo prático modelando a curva de distribuição normal (Gaussiana) da estatura populacional.
    *   **Gráficos 3D (`plot_surface`):** Criação de superfícies tridimensionais complexas utilizando `np.meshgrid`, simulando, por exemplo, o efeito combinado da Temperatura e do pH na atividade enzimática.

## 📚 Conteúdo da Aula 04 - Regressão e Ajuste de Curvas

Nesta quarta aula, o foco é a modelagem matemática de dados experimentais, utilizando ferramentas estatísticas e de otimização (SciPy, NumPy e Scikit-Learn) para extrair parâmetros cinéticos e biológicos:

*   **Regressão Linear Simples (`scipy.stats.linregress`):**
    *   Construção de uma curva de calibração padrão (Concentração vs. Absorbância).
    *   Simulação de dados com adição de ruído via `np.random.normal`.
    *   Obtenção da inclinação (slope), intercepto e coeficiente de determinação ($R^2$).
*   **Ajuste de Curvas Não-Lineares (`scipy.optimize.curve_fit`):**
    *   **Crescimento Microbiano:** Ajuste de dados a um modelo exponencial para estimar a concentração inicial ($Cx_0$) e a taxa específica de crescimento ($\mu$).
    *   **Cinética Enzimática:** Aplicação do modelo de Michaelis-Menten para estimar os parâmetros cinéticos de Velocidade Máxima ($V_{max}$) e a Constante de Michaelis ($K_m$) a partir da concentração de substrato.
*   **Ajuste Polinomial (`np.polyfit`):**
    *   Análise de curvas dose-resposta (efeito da concentração de um nutriente na taxa de crescimento).
    *   Uso de polinômios de grau 2 (parábolas) para modelar comportamentos ótimos e de toxicidade.
*   **Avaliação e Visualização de Modelos:**
    *   Cálculo de métricas de qualidade de ajuste com a função `r2_score`.
    *   Construção de gráficos sobrepondo dados experimentais brutos (dispersão) com curvas suaves matemáticas.
    *   
 ## 📚 Conteúdo da Aula 05 - Análise Estatística, Modelagem e Exportação de Dados

Nesta aula prática, consolidamos a integração entre tratamento estatístico rigoroso, modelagem matemática e estruturação de relatórios:

*   **Importação e Exportação de Dados com Pandas:**
    *   Carregamento de dados experimentais diretamente de planilhas (`pd.read_excel`).
    *   Criação de DataFrames para estruturar os resultados calculados e exportação automatizada para Excel (`pd.ExcelWriter`).
*   **Tratamento Estatístico Aplicado:**
    *   Cálculo de dispersão de réplicas analíticas (desvio padrão amostral e médias).
    *   Determinação do Intervalo de Confiança de 95% utilizando a distribuição t de Student (`scipy.stats.t.interval`).
*   **Modelagem Avançada e Desafio Prático ($k_La$):**
    *   Ajuste linear pelo método dos mínimos quadrados com validação do coeficiente de determinação ($R^2$).
    *   **Desafio Biotecnológico:** Otimização não-linear utilizando `curve_fit` para determinar os parâmetros da equação empírica do coeficiente volumétrico de transferência de oxigênio ($k_L a = a \cdot N^b$) em função da rotação de um biorreator.
    *   Análise crítica dos parâmetros ajustados frente à literatura de engenharia de bioprocessos.
*   **Visualização de Incertezas:**
    *   Criação de gráficos com qualidade de publicação, incluindo sombreamento para limites de confiança (`fill_between`) e aplicação de barras de erro representativas (`errorbar`).
## 📂 Arquivos de Apoio (Download Obrigatório)
Para executar os códigos desta aula, você precisará baixar as planilhas abaixo que contêm os dados brutos:
* 🔗 [media_desvio_dados.xlsx](./media_desvio_dados.xlsx) - *Dados para a prática de Regressão Linear.*
* 🔗 [dados_kla.xlsx](./dados_kla.xlsx) - *Dados experimentais para o Desafio Prático.*

## 🚀 Como acessar e executar as aulas

Não é necessário instalar nenhum software no seu computador para acompanhar esta disciplina. Utilizaremos o **Google Colaboratory**, que roda o código Python diretamente na nuvem pelo seu navegador.

Para abrir a Aula 01 e executar os códigos, basta clicar no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](Capítulo_01_Introdução_ao_Python.ipynb)

Para abrir a Aula 02 e executar os códigos, basta clicar no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](Aula_02_Python_Introdução.ipynb)

Para abrir a Aula 03 e executar os códigos, basta clicar no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](Aula_03_Introdução_ao_Python_para_biocientistas.ipynb)

Para abrir a Aula 04 e executar os códigos, basta clicar no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](Aula_04_Ajuste_de_Curvas.ipynb)

Para abrir a Aula 05 e executar os códigos, basta clicar no botão abaixo:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](Aula_05_importando_dados_ajuste.ipynb)


> **Nota para os alunos:** Após abrir o arquivo no Colab, lembre-se de clicar em `Arquivo > Salvar uma cópia no Drive` para que você possa fazer suas próprias anotações e resolver os exercícios propostos sem perder o seu progresso.

## 🛠️ Pré-requisitos

* Uma conta Google (Gmail ou e-mail institucional associado ao Google).
* Acesso à internet e um navegador atualizado.
* Curiosidade e vontade de aprender a integrar ciência de dados à pesquisa biológica!

## 📖 Referências e Materiais de Apoio

Para aprofundar os conhecimentos em programação científica, análise de dados e modelagem de bioprocessos, recomendamos os seguintes recursos:

### 🐍 Documentação Oficial das Ferramentas
* **Python Software Foundation:** [Documentação Oficial do Python](https://docs.python.org/3/) — Guia completo da linguagem.
* **NumPy:** [NumPy Documentation](https://numpy.org/doc/) — Referência essencial para computação numérica e manipulação de arrays.
* **SciPy:** [SciPy Reference Guide](https://docs.scipy.org/doc/scipy/) — Manuais de otimização (`curve_fit`), estatística (`linregress`) e métodos científicos.
* **Matplotlib:** [Matplotlib Tutorials](https://matplotlib.org/stable/tutorials/index.html) — Guia de visualização de dados e plotagem de gráficos em 2D e 3D.

### 🧬 Programação Aplicada à Biologia e Engenharia
* **Jones, P. (2015).** *Python for Biologists: A complete programming course for beginners*.
* **Langtangen, H. P. (2016).** *A Primer on Scientific Programming with Python*. Springer (Excelente para modelagem matemática aplicada à engenharia).

### ⚙️ Cinética Enzimática e Bioprocessos (Modelos Matemáticos)
* **Doran, P. M. (2013).** *Bioprocess Engineering Principles*. Academic Press (Referência clássica para modelagem de crescimento microbiano e equações de Monod/Michaelis-Menten).
* **Shuler, M. L., & Kargi, F. (2002).** *Bioprocess Engineering: Basic Concepts* (2nd Edition). Prentice Hall.

---
**Professor Responsável:** Marcel Otavio Cerri  
**Departamento:** Engenharia de Bioprocessos e Biotecnologia  
**Instituição:** UNESP - Universidade Estadual Paulista (Campus Araraquara)
**Contato:** marcel.cerri@unesp.br
