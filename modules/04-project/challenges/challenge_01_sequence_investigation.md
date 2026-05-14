# Desafio 01 — Investigando uma Sequência Biológica Desconhecida

## Contexto

Uma sequência nucleotídica de origem desconhecida foi obtida durante um experimento de sequenciamento. Sua tarefa será utilizar ferramentas do Biopython para investigar possíveis características biológicas dessa sequência.

Ao longo deste desafio, você deverá manipular sequências biológicas, realizar buscas em bancos de dados públicos e interpretar os resultados obtidos.

O objetivo principal não é apenas executar comandos, mas desenvolver um pequeno fluxo investigativo semelhante ao utilizado em análises reais de bioinformática.

---

# Objetivos de Aprendizagem

Ao concluir este desafio, espera-se que você seja capaz de:

* Manipular sequências utilizando o objeto `Seq`.
* Trabalhar com objetos `SeqRecord`.
* Ler e escrever arquivos FASTA.
* Realizar buscas no NCBI utilizando `Bio.Entrez`.
* Interpretar informações obtidas em registros biológicos.
* Utilizar BLAST para investigar similaridade entre sequências.
* Organizar resultados de maneira clara e reprodutível.

---

# Arquivos Disponíveis

O desafio utiliza o seguinte arquivo:

[`unknown_sequence_01.fsa`](./data/unknown_sequence_01.fsa)

---

# Parte 1 — Explorando a Sequência

## Tarefa 1

Carregue a sequência presente no arquivo FASTA utilizando `Bio.SeqIO`.

Exiba:

* ID da sequência
* descrição
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

Apresente os resultados em formato de tabela ou dicionário.

---

# Parte 2 — Investigando a Sequência no NCBI

## Tarefa 4

Utilize `Bio.Entrez` para buscar registros relacionados à sequência investigada.

Você deverá:

* configurar corretamente o e-mail no Entrez
* escolher uma estratégia de busca apropriada
* justificar brevemente sua escolha

Sugestão:

Você pode utilizar o organismo, parte da sequência ou termos biológicos relevantes para construir sua busca.

---

## Tarefa 5

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

---

# Parte 3 — Busca por Similaridade

## Tarefa 6

Utilize BLAST para investigar possíveis homologias da sequência.

Você poderá utilizar:

* BLAST online (`NCBIWWW.qblast`) ou
* BLAST local (`BLAST+`)

Escolha a abordagem que considerar mais adequada.

---

## Tarefa 7

Analise os resultados obtidos no BLAST.

Identifique:

* melhor hit encontrado
* organismo associado
* porcentagem de identidade
* E-value
* possível função biológica associada

---

## Tarefa 8

Com base nos resultados obtidos ao longo do desafio, escreva uma breve conclusão respondendo:

* Qual organismo provavelmente está associado à sequência?
* A sequência parece corresponder a um gene conhecido?
* Os resultados encontrados foram suficientes para uma identificação confiável?
* Quais limitações existem nessa análise?

---

# Desafio Extra (Opcional)

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
01 - Configurações
02 - Carregamento dos Dados
03 - Análise da Sequência de Interesse
04 - Buscas no NCBI
05 - Blast
06 - Conclusões
```

---

# Critérios de Avaliação

| Critério                   | Peso |
| -------------------------- | ---- |
| Funcionamento do código    | 40%  |
| Uso correto do Biopython   | 25%  |
| Organização e clareza      | 15%  |
| Interpretação biológica    | 10%  |
| Documentação e comentários | 10%  |

---

# Recursos Úteis

* Documentação do Biopython
* NCBI GenBank
* NCBI BLAST
* Tutorial oficial do Biopython

---

