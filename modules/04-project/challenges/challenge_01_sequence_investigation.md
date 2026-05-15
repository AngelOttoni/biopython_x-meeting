# Desafio 01 — Investigando uma Sequência Biológica Desconhecida

## Contexto

Uma sequência nucleotídica de origem desconhecida foi obtida durante um experimento de sequenciamento ambiental. Sua tarefa será utilizar ferramentas do Biopython para investigar possíveis características biológicas dessa sequência.

Ao longo deste desafio, você deverá manipular sequências biológicas, realizar buscas por similaridade e explorar bancos de dados públicos para interpretar os resultados obtidos.

O objetivo principal não é apenas executar comandos, mas desenvolver um pequeno fluxo investigativo semelhante ao utilizado em análises reais de bioinformática.

---

# Objetivos de Aprendizagem

Ao concluir este desafio, espera-se que você seja capaz de:

* Manipular sequências utilizando o objeto `Seq`.
* Trabalhar com objetos `SeqRecord`.
* Ler e escrever arquivos FASTA.
* Investigar sequências utilizando BLAST.
* Interpretar resultados de alinhamento e similaridade.
* Realizar buscas no NCBI utilizando `Bio.Entrez`.
* Explorar registros biológicos no formato GenBank.
* Organizar resultados de maneira clara e reprodutível.

---

# Arquivos Disponíveis

O desafio utiliza o seguinte arquivo:

[`unknown_sequence_01.fsa`](./data/env_sample_A23_partial_sequence.fsa)

---

# Parte 1 — Explorando a Sequência

## Tarefa 1

Carregue a sequência presente no arquivo FASTA utilizando `Bio.SeqIO`. Observe como as informações do cabeçalho FASTA são armazenadas no objeto `SeqRecord`.

Exiba:

* identificador da sequência (id)
* descrição do registro
* comprimento da sequência
* os primeiros 50 nucleotídeos

---

## Tarefa 2

Utilizando métodos do objeto `Seq`, realize:

* transcrição
* complemento reverso

Exiba os resultados de forma organizada.

---

## Tarefa 3

Calcule:

* porcentagem de GC
* quantidade total de nucleotídeos A, T, C e G

*Apresente os resultados em formato de tabela ou dicionário.*

Além dos cálculos, interprete brevemente o que essas características podem indicar sobre a sequência analisada.

---

# Parte 2 — Investigando Similaridade com BLAST

## Tarefa 4

Utilize BLAST para investigar possíveis homologias da sequência.

Você poderá utilizar:

* BLAST online (`NCBIWWW.qblast`) ou
* BLAST local (`BLAST+`)

Escolha a abordagem que considerar mais adequada.

---

## Tarefa 5


Analise os resultados obtidos no BLAST.

Identifique:

* melhor hit encontrado
* organismo associado
* porcentagem de identidade
* cobertura do alinhamento
* E-value
* possível função biológica associada

Além disso:

* verifique se múltiplos hits apontam para grupos biológicos semelhantes
* interprete o nível de confiança da identificação obtida

---

# Parte 3 — Investigação Refinada no NCBI

## Tarefa 6

Com base nas hipóteses levantadas a partir do BLAST, utilize `Bio.Entrez` para buscar registros relacionados à sequência investigada.

Você deverá:

* configurar corretamente o e-mail no Entrez
* construir uma estratégia de busca coerente com os resultados do BLAST
* justificar brevemente sua escolha

Exemplo:

Os resultados do BLAST podem sugerir:

* um organismo específico
* um grupo taxonômico
* um gene conservado
* uma região ribossomal

Utilize essas informações para construir sua busca.

---

## Tarefa 7

Selecione um registro relevante retornado pela busca e:

* faça o download no formato GenBank
* carregue o arquivo utilizando `SeqIO`
* extraia informações biológicas relevantes

Exemplos de informações:

* organismo
* genes anotados
* tamanho da sequência
* referências
* features presentes

Interprete brevemente as informações encontradas.

---
# Parte 4 — Conclusão da Investigação

## Tarefa 8

Com base nos resultados obtidos ao longo do desafio, escreva uma breve conclusão respondendo:

* Qual organismo provavelmente está associado à sequência?
* A sequência parece corresponder a um gene conhecido?
* Os resultados encontrados foram suficientes para uma identificação confiável?
* Quais limitações existem nessa análise?
* Quais análises adicionais poderiam aumentar a confiança da identificação?

---

# Desafio Extra (*Opcional*)

Automatize parte da análise criando funções reutilizáveis.

Exemplos:

* função para calcular GC
* função para resumir registros GenBank
* função para extrair melhores hits do BLAST

---

# Requisitos de Entrega

Sua submissão deve:

* conter código executável
* apresentar explicações claras
* possuir organização adequada das células
* incluir interpretações biológicas dos resultados

---

# Estrutura Recomendada do Notebook

```text
1. Importação das Bibliotecas
2. Leitura da(s) Sequência(s)
3. Análise Inicial da Sequência
4. Busca por Similaridade (BLAST)
5. Investigação no NCBI
6. Conclusões
```

---

# Recursos Úteis

* [Documentação oficial do Biopython](https://biopython.org/)
* [NCBI GenBank](https://www.ncbi.nlm.nih.gov/)
* [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
* [Tutorial oficial do Biopython](https://biopython.org/docs/latest/Tutorial/index.html)

---

