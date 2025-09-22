# Analisando Dados com Python — Case: Cancelamento de Clientes

Este repositório contém um notebook Jupyter (`analise_dados.ipynb`) que realiza uma análise exploratória sobre um conjunto de dados de cancelamentos de clientes. O objetivo é identificar padrões e possíveis causas de cancelamento e propor ações para reduzir a taxa de cancelamento.

## Conteúdo

- `analise_dados.ipynb` — Notebook principal com todo o fluxo: leitura, limpeza, análise e visualizações.
- `cancelamentos_sample.csv` — Amostra dos dados de clientes (inclui colunas como idade, sexo, ligacoes_callcenter, dias_atraso, duracao_contrato, cancelou, etc.).
- `graficos/` — Pasta criada pelo notebook para salvar gráficos interativos (HTML) e, quando disponível, imagens (PNG).

## Requisitos

- Python 3.8+
- Recomenda-se criar um ambiente virtual (venv, conda, etc.)

Dependências básicas (instale via pip):

```
pip install pandas plotly openpyxl numpy ipykernel nbformat
```

Dependência opcional para salvar PNGs (recomendado se quiser exportar imagens estáticas):

```
pip install -U kaleido
```

## Como usar

1. Abra o projeto no VS Code (ou outro editor) e ative seu ambiente virtual.
2. Se ainda não possui os pacotes, instale-os conforme a seção anterior.
3. Abra o notebook `analise_dados.ipynb`.
4. Execute as células na ordem. Principais etapas no notebook:
   - Leitura do CSV e remoção de colunas irrelevantes.
   - Inspeção inicial com `tabela.info()` e `display()`.
   - Limpeza seletiva e conversões de tipo (célula "3.1").
   - Análises de contagem e proporção de cancelamentos.
   - Geração de histogramas por coluna com separação por status de cancelamento.
   - Salvamento dos gráficos em `./graficos/` (HTML interativos; PNGs se `kaleido` estiver instalado).

## Observações importantes

- O notebook contém uma etapa original que remove todas as linhas com valores nulos (`dropna()`). Para preservar mais dados, foi adicionada uma célula ("3.1") que aplica conversões e preenchimentos mais seguros ao invés de remover linhas globalmente.
- Caso você prefira usar a versão original que remove nulos, execute a célula de limpeza original; caso contrário, execute 3.1 para a versão aprimorada.

## Estrutura de exemplo

```
analise_dados.ipynb
cancelamentos_sample.csv
README.md
graficos/
```

## Resultados esperados

- Relatório de contagem e proporção de clientes que cancelaram.
- Histograma por coluna, separado por clientes que cancelaram e que não cancelaram.
- Arquivos HTML interativos em `graficos/` para inspecionar visualmente cada gráfico.
