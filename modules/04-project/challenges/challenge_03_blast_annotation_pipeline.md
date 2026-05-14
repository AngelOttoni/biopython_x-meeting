# Desafio 03 — Pipeline de Anotação com BLAST

## Contexto

Uma coleção de sequências biológicas foi obtida durante um projeto de sequenciamento experimental. Entretanto, parte dessas sequências ainda não possui anotação funcional conhecida.

Sua tarefa será construir um pequeno pipeline de anotação utilizando ferramentas do Biopython e BLAST para investigar possíveis homologias, identificar organismos relacionados e interpretar resultados de similaridade.

Este desafio simula uma etapa comum em projetos reais de bioinformática: a identificação preliminar de sequências desconhecidas.

---

# Objetivos de Aprendizagem

Ao concluir este desafio, espera-se que você seja capaz de:

* Trabalhar com buscas de similaridade utilizando BLAST.
* Utilizar recursos do módulo `Bio.Blast`.
* Interpretar resultados biológicos obtidos em alinhamentos.
* Comparar hits utilizando métricas como identidade e E-value.
* Organizar resultados de múltiplas sequências.
* Construir pequenos fluxos automatizados de análise.

---

# Arquivos Disponíveis

O desafio utiliza os seguintes arquivos:

```text
unknown_sequences.fasta
```

O arquivo contém múltiplas sequências sem anotação funcional conhecida.

---

# Parte 1 — Preparação dos Dados

## Tarefa 1

Carregue as sequências presentes no arquivo FASTA utilizando `Bio.SeqIO`.

Exiba:

* quantidade total de sequências
* IDs disponíveis
* comprimento de cada sequência

---

## Tarefa 2

Realize uma análise exploratória simples das sequências.

Investigue:

* distribuição de tamanhos
* conteúdo GC
* possíveis diferenças entre as sequências

Apresente os resultados de forma organizada.

---

# Parte 2 — Busca por Similaridade

## Tarefa 3

Escolha uma estratégia apropriada para realizar buscas BLAST.

Você poderá utilizar:

* `NCBIWWW.qblast()`
* BLAST+ local

Explique:

* por que escolheu essa abordagem
* quais parâmetros considera importantes
* possíveis limitações da estratégia utilizada

---

## Tarefa 4

Execute buscas BLAST para as sequências analisadas.

Para cada sequência, identifique:

* melhor hit encontrado
* organismo associado
* descrição do alinhamento
* porcentagem de identidade
* E-value

---

## Tarefa 5

Analise os alinhamentos obtidos.

Investigue:

* hits altamente confiáveis
* sequências com baixa similaridade
* possíveis diferenças funcionais
* organismos recorrentes

Discuta a confiabilidade dos resultados.

---

# Parte 3 — Parsing e Organização dos Resultados

## Tarefa 6

Realize o parsing dos resultados BLAST utilizando recursos do Biopython.

Extraia informações relevantes dos alinhamentos.

Exemplos:

* título do hit
* score
* E-value
* tamanho do alinhamento
* identidade

---

## Tarefa 7

Crie uma tabela resumo contendo os principais resultados obtidos.

Exemplo:

| Query | Melhor Hit | Organismo | Identidade | E-value |
| ----- | ---------- | --------- | ---------- | ------- |

Você pode utilizar:

* pandas
* CSV
* listas de dicionários

---

# Parte 4 — Interpretação Biológica

## Tarefa 8

Com base nos resultados obtidos, responda:

* As sequências parecem pertencer ao mesmo organismo?
* Existem evidências de genes conservados?
* Os resultados indicam funções biológicas semelhantes?
* Há sequências potencialmente não identificadas?

Justifique suas interpretações.

---

## Tarefa 9

Escolha uma sequência de interesse e realize uma investigação complementar.

Exemplos:

* pesquisar informações sobre o gene identificado
* investigar o organismo encontrado
* buscar funções biológicas associadas
* comparar diferentes hits manualmente

Documente:

* estratégia utilizada
* principais descobertas
* limitações da análise

---

# Desafio Extra (Opcional)

Automatize o pipeline de anotação.

Exemplos:

* criar funções reutilizáveis
* processar múltiplas sequências automaticamente
* exportar relatórios CSV
* gerar ranking de hits por confiança
* identificar sequências sem hits significativos

---

# Requisitos de Entrega

Sua submissão deve:

* conter código executável
* apresentar organização clara
* incluir interpretação biológica dos resultados
* justificar escolhas metodológicas
* utilizar corretamente recursos do Biopython

---

# Estrutura Recomendada do Notebook

```text
01_imports
02_carregamento_dados
03_analise_exploratoria
04_execucao_blast
05_parsing_resultados
06_tabela_resumo
07_interpretacao_biologica
08_conclusoes
```

---

# Critérios de Avaliação

| Critério                             | Peso |
| ------------------------------------ | ---- |
| Funcionamento do código              | 35%  |
| Uso correto do Bio.Blast             | 25%  |
| Parsing e organização dos resultados | 20%  |
| Interpretação biológica              | 10%  |
| Documentação e clareza               | 10%  |

---

# Recursos Úteis

* Documentação do Biopython
* NCBI BLAST
* BLAST+
* Tutorial oficial do Biopython