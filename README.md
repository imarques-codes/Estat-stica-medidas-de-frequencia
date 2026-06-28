## Sobre o projeto

Este projeto apresenta um estudo prático de **Estatística Descritiva com Python**, utilizando dados de e-commerce e colaboradores para aplicar conceitos fundamentais de análise de dados.

O notebook trabalha com **distribuições de frequência**, **tabelas de contingência**, **medidas de tendência central**, **medidas separatrizes** e **medidas de dispersão**, utilizando bibliotecas como **Pandas**, **Matplotlib**, **Seaborn** e **NumPy**.

O projeto foi desenvolvido em ambiente de notebook, com foco em aprendizado, interpretação estatística e visualização de dados.

---

## Objetivo

O objetivo principal é aplicar conceitos estatísticos em bases reais/simuladas para resumir, comparar e interpretar dados de negócio.

O projeto busca responder perguntas como:

- Como identificar e diferenciar variáveis qualitativas e quantitativas?
- Como construir distribuições de frequência absoluta e relativa?
- Como cruzar variáveis categóricas usando tabelas de contingência?
- Como calcular média, mediana e moda?
- Quando a mediana pode representar melhor os dados do que a média?
- Como usar quartis, decis e percentis para segmentar dados?
- Como interpretar histogramas, boxplots e violinplots?
- Como analisar variações salariais usando desvio médio absoluto, variância e desvio padrão?

---

## Como funciona o projeto

O notebook segue um fluxo de análise estatística dividido em etapas.

### 1. Entendimento dos dados

Nesta etapa, o projeto importa os pacotes necessários e realiza a leitura dos dados de vendas de e-commerce.

A base é carregada diretamente de um repositório público:

```python
import pandas as pd

url = 'https://raw.githubusercontent.com/alura-cursos/Estatisticas-Python-frequencias-medidas/refs/heads/main/dados/vendas_ecommerce.csv'
df = pd.read_csv(url)
```

São analisados aspectos como:

- Dimensão da base;
- Tipos de dados;
- Informações gerais do DataFrame;
- Variáveis qualitativas e quantitativas;
- Variáveis nominais, ordinais, discretas e contínuas.

---

### 2. Manipulação de variáveis qualitativas

O projeto transforma a variável de avaliação dos clientes em uma categoria ordinal, utilizando uma escala de satisfação.

Exemplo de classificação:

```text
1 = Péssimo
2 = Ruim
3 = Regular
4 = Bom
5 = Ótimo
```

Essa transformação facilita a análise das avaliações de clientes e a construção de gráficos mais interpretáveis.

---

### 3. Distribuição de frequências

São criadas distribuições de frequência para entender a quantidade e a proporção de avaliações dos clientes.

Nesta etapa são calculadas:

- Frequência absoluta;
- Frequência relativa;
- Porcentagem por categoria;
- Distribuição visual das avaliações.

Também são utilizados gráficos de barras para comunicar os resultados.

---

### 4. Tabelas de contingência

O projeto utiliza tabelas de contingência para cruzar variáveis categóricas, como avaliação dos clientes e região.

Com isso, é possível analisar:

- Avaliações positivas por região;
- Avaliações negativas por região;
- Diferenças relevantes entre grupos;
- Possíveis regiões que demandam ações específicas.

---

### 5. Análise do perfil dos clientes

São realizados cruzamentos entre variáveis de clientes, como sexo biológico, região e valor total de compra.

Um dos objetivos é entender o comportamento de compra e identificar diferenças de ticket médio entre grupos.

---

### 6. Medidas de tendência central

O projeto aplica medidas de tendência central para resumir variáveis numéricas.

São trabalhados conceitos como:

- Média;
- Mediana;
- Moda;
- Comparação entre média, mediana e moda;
- Interpretação da assimetria dos dados.

Exemplos analisados:

- Tempo médio de entrega por categoria de produto;
- Vendas de eletrônicos na região Nordeste;
- Quantidade mais frequente de livros vendidos;
- Relação entre avaliação e tempo de entrega.

---

### 7. Análise de colaboradores

A segunda base utilizada no projeto contém informações de colaboradores:

```python
url = 'https://raw.githubusercontent.com/alura-cursos/Estatisticas-Python-frequencias-medidas/refs/heads/main/dados/colaboradores.csv'
colaboradores = pd.read_csv(url)
```

Essa base é usada para análises estatísticas envolvendo remuneração, idade, cargo e sexo biológico.

---

### 8. Histogramas e regra de Sturges

O projeto utiliza a **Regra de Sturges** para definir a quantidade adequada de classes em histogramas.

A fórmula aplicada é:

```text
k = 1 + (10 / 3) * log10(n)
```

Com isso, são criadas faixas salariais e tabelas de frequência para analisar a distribuição de remuneração dos colaboradores.

---

### 9. Medidas separatrizes

São calculados quartis e percentis para analisar a distribuição dos salários.

O projeto utiliza:

- Primeiro quartil;
- Segundo quartil;
- Terceiro quartil;
- Percentil 99;
- Classificação de colaboradores por faixa etária.

Essas medidas ajudam a identificar posições relativas dentro da distribuição dos dados.

---

### 10. Boxplot e análise de distribuição

O notebook utiliza boxplots para analisar a distribuição salarial geral e também por sexo biológico.

A análise inclui:

- Mediana;
- Quartis;
- Intervalo interquartil;
- Possíveis outliers;
- Comparação entre grupos.

---

### 11. Medidas de dispersão

Na etapa final, o projeto analisa a variação dos dados usando medidas de dispersão.

São calculados:

- Desvio médio absoluto;
- Variância;
- Desvio padrão;
- Comparação da dispersão salarial entre cargos;
- Visualização com boxplot e violinplot.

---

## Tecnologias utilizadas

- Python
- Jupyter Notebook
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## Estrutura do repositório

```text
python-statistics-frequency-measures/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── python_statistics_frequency_measures.ipynb
│
├── data/
│   └── .gitkeep
│
└── img/
    └── .gitkeep
```

---

## Bases de dados

O projeto utiliza duas bases carregadas diretamente de URLs públicas:

```text
vendas_ecommerce.csv
colaboradores.csv
```

As bases são usadas para fins educacionais e práticos, permitindo aplicar conceitos estatísticos em contextos de negócio, como vendas, avaliações de clientes e remuneração de colaboradores.

---

## Como executar no Google Colab

1. Acesse o notebook do projeto.
2. Abra no Google Colab.
3. Execute as células na ordem.
4. As bases de dados são carregadas automaticamente pelas URLs presentes no notebook.
5. Analise as tabelas, gráficos e interpretações geradas.

Depois que o projeto estiver no GitHub, você poderá abrir diretamente no Colab usando um link neste formato:

```text
https://colab.research.google.com/github/imarques-codes/python-statistics-frequency-measures/blob/main/notebooks/python_statistics_frequency_measures.ipynb
```

---

## Como executar localmente

Clone o repositório:

```bash
git clone https://github.com/imarques-codes/python-statistics-frequency-measures.git
```

Acesse a pasta do projeto:

```bash
cd python-statistics-frequency-measures
```

Crie um ambiente virtual:

```bash
python -m venv .venv
```

Ative o ambiente virtual:

```bash
# Windows
.venv\Scripts\activate
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Abra o notebook:

```bash
jupyter notebook notebooks/python_statistics_frequency_measures.ipynb
```

---

## Principais aprendizados

Este projeto fortalece conhecimentos práticos em:

- Estatística descritiva aplicada com Python;
- Manipulação de dados com Pandas;
- Classificação de variáveis estatísticas;
- Criação de tabelas de frequência;
- Análise de frequência absoluta e relativa;
- Uso de tabelas de contingência;
- Cálculo de média, mediana e moda;
- Uso de quartis, decis e percentis;
- Análise de dispersão com variância e desvio padrão;
- Visualização de dados com Matplotlib e Seaborn;
- Interpretação de histogramas, boxplots e violinplots;
- Organização de notebook para portfólio no GitHub.

---

## Possíveis melhorias futuras

- Criar uma seção final com os principais insights do projeto;
- Padronizar os gráficos com títulos, legendas e paleta visual única;
- Exportar gráficos para a pasta `img/`;
- Adicionar comentários executivos após cada análise;
- Criar uma versão resumida do notebook para apresentação;
- Transformar as análises em um dashboard interativo;
- Criar uma versão em inglês do README.

---

## Autor

**Igor Henrique Marques dos Santos**

- LinkedIn: [linkedin.com/in/igorhmarques](https://www.linkedin.com/in/igorhmarques/)
- GitHub: [github.com/imarques-codes](https://github.com/imarques-codes)
- E-mail: [igorhmsantos@gmail.com](mailto:igorhmsantos@gmail.com)

---

## Status do projeto

Projeto concluído como estudo prático de **Estatística Descritiva com Python**, frequências, medidas de tendência central, separatrizes e dispersão.
