# Desafio 02 — Mineração de Dados Biológicos com Bio.Entrez

## Contexto

Pesquisadores frequentemente precisam consultar bancos de dados biológicos públicos para obter informações sobre genes, organismos, proteínas e sequências associadas a diferentes estudos.

Neste desafio, você atuará como analista de dados biológicos responsável por investigar registros disponíveis no NCBI utilizando o módulo `Bio.Entrez`.

Seu objetivo será construir pequenas estratégias de mineração de dados biológicos, automatizando buscas, downloads e extração de informações relevantes.

---

# Objetivos de Aprendizagem

Ao concluir este desafio, espera-se que você seja capaz de:

* Utilizar o módulo `Bio.Entrez` para acessar bancos de dados do NCBI.
* Construir consultas utilizando operadores booleanos.
* Realizar buscas programáticas com `esearch()`.
* Fazer download de registros utilizando `efetch()`.
* Trabalhar com arquivos GenBank.
* Extrair e resumir informações biológicas.
* Organizar resultados de maneira reproduzível.

---

# Cenário do Desafio

Uma equipe de pesquisa está investigando genes associados à resistência bacteriana.

Sua tarefa será utilizar o NCBI para localizar registros relevantes, recuperar sequências biológicas e produzir pequenos resumos analíticos.

---

# Parte 1 — Construindo Estratégias de Busca

## Tarefa 1

Configure corretamente o acesso ao NCBI utilizando `Bio.Entrez`.

Explique brevemente:

* por que o e-mail deve ser configurado
* qual a importância do uso responsável da API do NCBI

---

## Tarefa 2

Realize uma busca no banco de dados `nucleotide` utilizando `Entrez.esearch()`.

A busca deverá envolver:

* um organismo bacteriano
* um gene relacionado à resistência
* pelo menos um operador booleano

Exemplos de temas possíveis:

* resistência a antibióticos
* beta-lactamases
* genes mecA
* resistência à tetraciclina

---

## Tarefa 3

Analise os resultados da busca.

Exiba:

* quantidade total de registros encontrados
* lista dos primeiros IDs retornados
* estratégia de busca utilizada

Explique se os resultados encontrados parecem coerentes com a consulta realizada.

---

# Parte 2 — Download e Parsing de Registros

## Tarefa 4

Escolha pelo menos dois registros relevantes obtidos na busca.

Utilize `Entrez.efetch()` para:

* baixar os registros no formato GenBank
* salvar os arquivos localmente

---

## Tarefa 5

Utilize `Bio.SeqIO` para carregar os registros baixados.

Extraia informações como:

* organismo
* definição da sequência
* comprimento
* accession
* referências bibliográficas
* features anotadas

---

## Tarefa 6

Identifique e liste as features presentes nos registros.

Por exemplo:

* CDS
* gene
* source
* mRNA
* protein_id

Apresente um resumo organizado contendo:

* tipo da feature
* localização
* informações relevantes disponíveis nos qualifiers

---

# Parte 3 — Análise Comparativa

## Tarefa 7

Compare os registros analisados.

Investigue:

* diferenças de tamanho
* organismos distintos
* genes presentes
* similaridades nas anotações

Escreva uma breve interpretação biológica.

---

## Tarefa 8

Crie uma tabela resumo contendo as principais informações dos registros analisados.

A tabela pode incluir:

| Accession | Organismo | Gene | Tamanho | Descrição |
| --------- | --------- | ---- | ------- | --------- |

Você pode utilizar:

* listas de dicionários
* pandas DataFrame
* CSV exportado automaticamente

---

# Parte 4 — Investigação Livre

## Tarefa 9

Escolha uma informação biológica presente nos registros e realize uma investigação complementar.

Exemplos:

* pesquisar outro gene relacionado
* buscar proteínas associadas
* investigar outro organismo
* comparar diferentes cepas bacterianas
* analisar genes semelhantes

Documente:

* o que foi investigado
* estratégia utilizada
* resultados encontrados

---

# Desafio Extra (Opcional)

Automatize a geração de relatórios biológicos.

Exemplos:

* gerar tabela automática de features
* exportar resumo para CSV
* criar função para resumir registros GenBank
* automatizar download de múltiplos registros

---

# Requisitos de Entrega

Sua submissão deve:

* conter código executável
* apresentar organização clara
* incluir interpretações biológicas
* justificar decisões tomadas durante a análise
* utilizar corretamente recursos do Biopython

---

# Estrutura Recomendada do Notebook

```text
01_imports
02_configuracao_entrez
03_buscas_ncbi
04_download_registros
05_parsing_genbank
06_analise_comparativa
07_conclusoes
```

---

# Critérios de Avaliação

| Critério                          | Peso |
| --------------------------------- | ---- |
| Funcionamento do código           | 35%  |
| Uso correto do Bio.Entrez         | 25%  |
| Parsing e interpretação biológica | 20%  |
| Organização e clareza             | 10%  |
| Documentação e comentários        | 10%  |

---

# Recursos Úteis

* Documentação do Biopython
* NCBI Entrez
* NCBI GenBank
* Tutorial oficial do Biopython
