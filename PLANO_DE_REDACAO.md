# Plano de redação do TCC

Este documento organiza a redação do texto acadêmico do FASTA2GO. O manuscrito deve permanecer coerente com a implementação efetivamente existente no repositório do projeto e com os experimentos que puderem ser reproduzidos.

## Diretrizes

- Não descrever como implementado algo que ainda esteja apenas planejado.
- Diferenciar metodologia (como a pesquisa foi conduzida) de desenvolvimento (como o FASTA2GO foi construído).
- Registrar versões, parâmetros, critérios de inclusão/exclusão e sementes dos experimentos.
- Sustentar afirmações científicas com referências verificáveis; não criar referências ou resultados.
- Apresentar limitações dos dados e dos modelos, inclusive distribuição desigual dos rótulos e possível similaridade entre proteínas nos conjuntos de treino e teste.

## Organização proposta

### 1. Introdução
Contextualização da bioinformática e da anotação funcional de proteínas; problema de pesquisa; justificativa; objetivo geral e objetivos específicos; contribuição e organização do texto.

O rascunho existente já contém uma base de introdução. Antes de expandi-lo, consolidar a versão duplicada da seção e alinhar os objetivos ao escopo final do experimento.

### 2. Metodologia
Descrever o delineamento da pesquisa e o protocolo experimental:
- fontes de sequências e anotações funcionais;
- critérios de seleção das proteínas e dos termos da Gene Ontology;
- preparação dos dados e tratamento de proteínas sem rótulos;
- extração e definição das características;
- propagação/seleção de termos GO, conforme a regra realmente implementada;
- divisão treino/teste e prevenção de vazamento;
- modelos de referência, configurações, métricas e ambiente computacional.

### 3. Referencial teórico
Desenvolver os fundamentos necessários ao trabalho:
- proteínas e sequências de aminoácidos;
- anotação e predição funcional;
- Gene Ontology, seus três domínios e relações hierárquicas;
- representação de sequências por características composicionais e físico-químicas;
- classificação multilabel e aprendizado de máquina;
- avaliação de modelos em conjuntos multilabel desbalanceados;
- trabalhos relacionados à predição de função proteica.

A revisão deve comparar abordagens e explicitar a lacuna investigada, não apenas listar conceitos.

### 4. Desenvolvimento
Apresentar o FASTA2GO e suas decisões de implementação:
- arquitetura e fluxo de processamento;
- ingestão e persistência dos dados;
- construção dos rótulos e integração com GO;
- extração das características;
- preparação dos conjuntos experimentais;
- implementação dos modelos e geração dos resultados.

Separar descrição da implementação de interpretação dos resultados. Incluir tabelas e figuras apenas quando houver artefatos e resultados verificáveis.

### 5. Considerações finais
Retomar o problema e os objetivos, sintetizar os resultados efetivamente obtidos, discutir limitações e propor trabalhos futuros compatíveis com os achados.

## Pontos que precisam ser confirmados durante a redação

- Título definitivo e formulação final do problema.
- Versões e datas das bases de dados utilizadas.
- Critério final de construção/propagação dos rótulos GO.
- Protocolo experimental definitivo: população, rótulos, divisão e modelos comparados.
- Se os resultados dos experimentos manual e AutoGluon serão padronizados antes de aparecerem como comparação direta.
- Se haverá avaliação complementar com separação por similaridade/homologia entre proteínas.
- Dados institucionais e elementos pré-textuais que ainda estão como placeholders no template.

## Primeira revisão estrutural identificada

O arquivo `capitulos/01-introducao.tex` contém duas seções `Introdução` com o mesmo rótulo: a primeira é texto instrucional do template e a segunda é o rascunho do trabalho. A primeira deve ser removida na próxima edição do capítulo, preservando e revisando o texto autoral. Também será necessário substituir os textos instrucionais dos capítulos 2 a 5 gradualmente, sem preencher lacunas metodológicas com suposições.
