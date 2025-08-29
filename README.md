# 🔋 Sujidade e Retorno Econômico de Baterias

Automação completa de otimização de Sistemas de Armazenamento de Energia em Bateria (BESS), considerando os impactos da sujidade em painéis fotovoltaicos e o retorno econômico. O projeto utiliza algoritmos evolutivos (NSGA-III) para dimensionamento do BESS, com foco em objetivos econômicos e efeitos operacionais.

---

## 📚 Sumário

- [📚 Sumário](#-sumário)
- [📦 Visão Geral](#-visão-geral)
- [🧰 Tecnologias e Metodologias](#-tecnologias-e-metodologias)
- [📁 Estrutura do Repositório](#-estrutura-do-repositório)
- [⚙️ Instalação e Uso](#️-instalação-e-uso)
- [📊 Resultados](#-resultados)
- [👨‍💻 Autor](#-autor)
- [📄 Licença](#-licença)

---

## 📦 Visão Geral

Este trabalho aborda o dimensionamento do BESS utilizando algoritmos evolutivos (NSGA-III), levando em consideração a minimização do custo anual de eletricidade e do custo anual relacionado à bateria, além de efeitos operacionais como a sujidade nos painéis fotovoltaicos. Foram utilizadas séries horárias de geração sintética (modelo PV) e consumo (Building Data Genome Project 2) para a região de Vitória-ES (2016–2017).

---

## 🧰 Tecnologias e Metodologias

O código de simulação e otimização foi implementado em Python e utiliza as seguintes bibliotecas:

- 🐍 **Python 3.8+**
- `pandas`: Para manipulação e análise de dados.
- `matplotlib`: Para visualização de dados.
- `pymoo`: Para otimização multiobjetivo, especificamente o algoritmo NSGA-III.
- `pvlib`: Para modelagem de sistemas fotovoltaicos.

### Algoritmo NSGA-III

O NSGA-III (Non-Dominated Sorting Genetic Algorithm III) é um algoritmo genético multiobjetivo que busca encontrar um conjunto de soluções diversificadas e não dominadas, otimizando múltiplos objetivos simultaneamente. Ele é particularmente adequado para problemas com muitos objetivos, como o dimensionamento de BESS, onde é necessário equilibrar custos e eficiência operacional.

### Modelagem de Sujidade (Soiling)

Para adicionar realismo à simulação, foi aplicado um modelo de sujidade (soiling) que considera o acúmulo de poeira e partículas nos painéis fotovoltaicos, impactando diretamente a eficiência da geração de energia. O estudo da sujidade e sua modelagem são essenciais para dimensionar corretamente os sistemas de geração e armazenamento, garantindo previsões mais realistas de geração e maior confiabilidade nos cálculos de retorno sobre o investimento.

### Modelagem do Consumo Energético e Geração Fotovoltaica

O projeto utiliza dados de consumo energético do Building Data Genome Project 2 e simula a geração fotovoltaica com base em dados meteorológicos da região de Vitória-ES (2016-2017). A metodologia de simulação abrange a modelagem do consumo energético, a simulação de geração fotovoltaica e a inclusão do modelo de degradação por sujidade.

---

## 📁 Estrutura de Diretórios

O repositório está organizado da seguinte forma:

```
.
├── Sujidade_e_Retorno_Econômico_de_Baterias.pdf
├── com-sujidade.ipynb
├── sem-sujidade.ipynb
├── sujidade-datas.ipynb
├── requirements.txt
├── figuras/
│   ├── boxplot_objetivos_com_sujidade.png
│   ├── boxplot_objetivos_sem_sujidade.png
│   ├── consumo/
│   ├── diff-geracao.png
│   ├── geracao/
│   ├── pareto_com_sujidade.png
│   ├── pareto_sem_sujidade.png
│   ├── scatter_plot.png
│   ├── scm_flow.png
│   ├── sujidade.png
│   ├── sujidade_com_lavagem.png
│   └── sujidade_sem_lavagem.png
├── Genome_Separate_Buildings/
│   └── ... (arquivos CSV de consumo)
└── smart-grid/
    └── dados/
        ├── 2016/
        └── 2017/
```

---

## ⚙️ Instalação e Uso

Para replicar os resultados e executar os notebooks, siga os passos abaixo:

### ✅ Requisitos:

- Python 3.8+

### 🔒 Criando ambiente virtual:

```bash
python -m venv venv
source venv/bin/activate    # Linux/macOS
# venv\Scripts\activate       # Windows
```

### 📦 Instalando as dependências:

Instale os pacotes necessários com:

```bash
pip install -r requirements.txt
```

### ▶️ Rodando os notebooks Jupyter:

```bash
jupyter notebook
```

Abra os arquivos `.ipynb` (`com-sujidade.ipynb`, `sem-sujidade.ipynb`, `sujidade-datas.ipynb`) no seu navegador e execute as células para ver as análises e resultados.

---

## 📊 Resultados

Os resultados detalhados da otimização do BESS, incluindo a comparação entre cenários com e sem sujidade, são apresentados no documento principal (`Sujidade_e_Retorno_Econômico_de_Baterias.pdf`) e visualizados nos notebooks Jupyter. As análises demonstram o impacto significativo da sujidade na eficiência e no retorno econômico dos sistemas fotovoltaicos, destacando a importância de sua consideração no dimensionamento de sistemas de energia renovável.

---

## 👨‍💻 Autor

Desenvolvido por:

| [<img src="https://avatars.githubusercontent.com/u/56831082?v=4" width=115><br><sub>Arthur Coelho Estevão</sub>](https://github.com/arthurcoelho442) |
| :---: |

---

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes. (Assumindo licença MIT, verificar no repositório se existe um arquivo LICENSE e qual a licença real, caso contrário, remover esta seção ou ajustar.)


