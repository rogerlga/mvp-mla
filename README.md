# MVP Machine Learning & Analytics

Este projeto aplica técnicas de **Machine Learning** utilizando dados operacionais de um turbogerador a gás, com foco no treinamento **não supervisionado** de **clusterização**. O notebook resultado desse trabalho é a entrega do MVP do curso de pós-graduação em *Ciência de Dados & Analytics* da PUC-Rio (2025).

O notebook pode ser encontrado em:
- Neste repositório do GitHub: [mvp_mla.ipynb (GitHub)](mvp_mla.ipynb)
- Link para abertura no Google Colab: [mvp_mla.ipynb (Colab)](https://colab.research.google.com/github/rogerlga/mvp-mla/blob/main/mvp_mla.ipynb)

A análise exploratória e o pré-processamento desses dados se encontram no trabalho de MVP anterior, elaborado pelo mesmo autor ([repositório](https://github.com/rogerlga/mvp-adbp)).

## Descrição

Os dados contém medições de sensores de um trem de geração elétrica, formado por Turbina a Gás (Gas Generator/GG + Power Turbine/PT), Caixa de Engrenagem (Gearbox) e Gerador Elétrico (Generator), representado na ilustração abaixo:

<img src="https://raw.githubusercontent.com/rogerlga/mvp-adbp/refs/heads/main/assets/two_shaft_turbogenerator.jpg" width="600">

*Trem de equipamentos (fonte imagem: [site](http://emadrlc.blogspot.com/2013/01/chapter-1-introduction-to-gas-turbines.html))*

O foco da análise é a Turbina a Gás, cujos dados de sensores são utilizados para o treinamento de um modelo de clusterização:

<img src="https://raw.githubusercontent.com/rogerlga/mvp-adbp/refs/heads/main/assets/TG_tags.png" width="700">

*Representação de uma Turbina a Gás com os atributos do dataset (fonte imagem: adaptado do [site](https://www.researchgate.net/figure/Schematic-of-LM2500-marine-gas-turbine_fig1_349497740) pelo autor)*

O estudo visa obter clusters que representem os diferentes perfis operacionais do equipamento.

## Hipótese

Como evidenciamos no estudo/MVP anterior, é possível distinguir diferentes perfis operacionais através dos dados, permitindo treinar um modelo que faça a clusterização automática desses perfis.

## Objetivo

O objetivo é treinar um modelo **nâo supervisionado** para **agrupamento/clusterização** automática dos distintos perfis operacionais, o que ajudará na identificação e balanceamento dos dados correspondentes à cada perfil para uso em modelos futuros, como de detecção de anomalias, que requerem dados balanceados para cada perfil operacional. O objetivo final é embarcar essa técnica em uma ferramenta de análise de equipamentos, em que o usuário (expert do domínio) contará com ferramentas que o auxiliará na preparação dos dados, treinamento e colocação do modelo em produção.