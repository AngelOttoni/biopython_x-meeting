# Projeto Final e Desafios

Bem-vindo(a) ao módulo de projeto aplicado do minicurso de Biopython.

Nesta etapa do minicurso, você irá aplicar os conhecimentos desenvolvidos ao longo das aulas para resolver problemas práticos de bioinformática utilizando Python e Biopython.

Os desafios foram planejados para estimular:

* manipulação de sequências biológicas,
* acesso programático ao NCBI,
* parsing de arquivos biológicos,
* buscas por similaridade com BLAST,
* interpretação de resultados biológicos,
* organização e reprodutibilidade de análises computacionais.

---

# Estrutura da Pasta

```text
04-project/
├── README.md
└── challenges/
    ├── challenge_01_sequence_investigation.md
    ├── challenge_02_entrez_data_mining.md
    ├── challenge_03_blast_annotation_pipeline.md
    ├── data/
    │   └── unknown_sequence_01.fsa
    └── solutions/  # será liberada ao final do curso
```

---

# Organização dos Desafios

Os desafios estão disponíveis na pasta:

```text
challenges/
```

Cada notebook representa um desafio independente.

Exemplo:

```text
challenges/
├── challenge_01_sequence_investigation.ipynb
├── challenge_02_entrez_data_mining.ipynb
└── challenge_03_blast_annotation_pipeline.ipynb
```

---

# Objetivo dos Desafios

Os desafios possuem diferentes níveis de complexidade e abordam temas trabalhados durante o minicurso:

| Desafio    | Tema Principal                               |
| ---------- | -------------------------------------------- |
| Desafio 01 | Manipulação e investigação de sequências     |
| Desafio 02 | Mineração de dados biológicos com Bio.Entrez |
| Desafio 03 | Pipeline de anotação utilizando BLAST        |

---

# Como Resolver os Desafios

Você poderá:

* escolher um ou mais desafios,
* resolver individualmente ou em grupo (caso permitido pelas instrutoras),
* utilizar os notebooks como base para sua análise.

Recomenda-se:

* manter organização nas células,
* documentar interpretações biológicas,
* comentar trechos importantes do código,
* garantir reprodutibilidade da análise.

---

# Estrutura Recomendada dos Notebooks

```text
1. Importação das Bibliotecas
2. Leitura das Sequências
3. Manipulação e Processamento
4. Buscas no NCBI ou BLAST
5. Parsing e Organização dos Resultados
6. Discussão biológica
7. Conclusões
```

---

# Entrega das Soluções

As soluções deverão ser entregues via Pull Request (PR) neste repositório.

## Fluxo Recomendado

### 1. Faça um fork do repositório

Clique em:

```text
Fork
```

---

### 2. Clone o seu fork

```bash
git clone <url-do-seu-fork>
```

---

### 3. Crie uma branch para sua solução

Exemplo:

```bash
git checkout -b feat/desafio-01
```

---

### 4. Adicione sua resolução

Sugestão de estrutura:

```text
submissions/
└── seu_nome/
    └── challenge_01.ipynb
```

---

### 5. Faça commit das alterações

```bash
git add .
git commit -m "Add challenge 01 solution"
```

---

### 6. Envie para seu fork

```bash
git push origin feat/desafio-01
```

---

### 7. Abra um Pull Request

Abra um PR do seu fork para o repositório principal do minicurso.

---

# O que será observado nas submissões

Durante a análise dos notebooks (enviados via PR), será considerado:

- funcionamento do código,
- uso adequado do Biopython,
- organização e clareza do notebook,
- interpretação biológica dos resultados,
- documentação e comentários explicativos.

> Não é necessário produzir uma solução perfeita. *O objetivo principal é praticar os conceitos trabalhados durante o minicurso e desenvolver raciocínio investigativo em bioinformática.*

---

# Requisitos

Antes de iniciar os desafios, certifique-se de possuir:

* Python 3
* Biopython instalado
* Jupyter Notebook ou Google Colab
* BLAST+ instalado (para desafios envolvendo BLAST local)

Instalação do Biopython:

```bash
pip install biopython
```

---

# Recursos Úteis

* [Documentação oficial do Biopython](https://biopython.org/)
* [NCBI GenBank](https://www.ncbi.nlm.nih.gov/)
* [NCBI BLAST](https://blast.ncbi.nlm.nih.gov/Blast.cgi)
* [Tutorial oficial do Biopython](https://biopython.org/docs/latest/Tutorial/index.html)

---

# Boas Práticas

Durante o desenvolvimento:

* utilize nomes de variáveis claros,
* evite duplicação de código,
* documente decisões importantes,
* mantenha os notebooks organizados,
* interprete biologicamente os resultados obtidos.

---

# Considerações Finais

O objetivo desta etapa não é apenas executar código, mas desenvolver raciocínio investigativo e construir pequenos fluxos reais de análise em bioinformática.

Explore os dados, teste hipóteses e experimente diferentes estratégias utilizando as ferramentas apresentadas ao longo do minicurso.
