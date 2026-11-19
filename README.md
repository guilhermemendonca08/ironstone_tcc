# IRONSTONE (Abordagem Orientada a Dados para Roteamento de Veículos no Atendimento a Eventos de Emergência)

> O IRONSTONE é uma abordagem orientada a dados voltada à definição de rotas de veículos para o atendimento a eventos de emergência (*e-events*) utilizando dados de tráfego.

## Visão Geral

O IRONSTONE utiliza dados de tráfego em tempo real e tempos históricos de atendimento para planejar as rotas dos veículos de emergência. O processo é dividido em duas etapas. Na primeira, estima os tempos de deslocamento entre os veículos disponíveis e as ocorrências por meio da API da TomTom. Em seguida, aplica uma heurística para definir a alocação e a ordem de atendimento, com o objetivo de minimizar o tempo total de resposta aos eventos.

## Pré-requisitos

- **Jupyter Notebook** (por exemplo, instalado via **Anaconda3**)
- **Dependências Python** instaladas (`pip install -r requirements.txt`)
- **Chave da API TomTom** (*TomTom API Key*), disponível gratuitamente no site da [TomTom](https://www.tomtom.com/)

## Configuração do `.env`

Antes de executar o projeto, crie um arquivo chamado `.env` na **raiz do repositório** e defina a sua chave da API TomTom:

```env
TOMTOM_API_KEY=sua_chave_aqui
```

O notebook `Code/GraphGeneration.ipynb` carrega automaticamente essa variável a partir do arquivo `.env`.

## Guia Rápido de Execução

Para garantir a reprodutibilidade, o IRONSTONE foi implementado em Jupyter Notebook. Os passos a seguir descrevem o processo de execução:

1. Obtenha gratuitamente a sua **TomTom API Key** no site da [TomTom](https://www.tomtom.com/).
2. Crie o arquivo `.env` na raiz do projeto e defina `TOMTOM_API_KEY=sua_chave_aqui`.
3. Abra o **Jupyter Notebook** no seu computador.
4. Localize e abra o notebook `Code/GraphGeneration.ipynb`.
5. Execute as células do arquivo `Code/GraphGeneration.ipynb` **na ordem exata em que aparecem**.
6. Após a conclusão do processo em `Code/GraphGeneration.ipynb`, localize e abra o notebook `Code/Heuristic.ipynb`.
7. Execute as células do arquivo `Code/Heuristic.ipynb` **na ordem exata em que aparecem**.

Seguindo esses passos e executando as células na ordem indicada, o IRONSTONE será executado corretamente, analisando os dados de tráfego e gerando as rotas de atendimento para os eventos de emergência.
