<p align="right">
  <a href="README.md">[EN]</a>
  <a href="README_es.md">[ES]</a>
  <a href="README_pt.md">[PT]</a>
  <a href="README_tr.md">[TR]</a>
  <a href="README_sv.md">[SV]</a>
</p>

## YAPExIL

_**Y**et **A**nother **P**rogramming **Ex**ercises **I**nteroperability **L**anguage_ (YAPExIL) é uma linguagem para descrever pacotes de exercícios de programação, parcialmente baseada no dialecto XML **PExIL** (_**P**rogramming **Ex**ercises **I**nteroperability **L**anguage_). Em comparação com o PExIL, o YAPExIL (1) é formalizado através de um esquema JSON em vez de um esquema XML, (2) remove lógica complexa para geração automática de testes enquanto ainda a suporta através de scripts, (3) suporta diferentes tipos de exercícios de programação e (4) adiciona suporte a uma série de recursos (por exemplo, instruções para os autores, geradores de feedback, e informação de plataforma).

O YAPExIL visa consolidar todos os dados necessários no ciclo de vida do exercício de programação, incluindo o apoio a sete tipos de exercícios de programação:

 - `BLANK_SHEET` fornece uma folha em branco para a estudante escrever o seu código fonte da solução do zero;
 - `EXTENSION` apresenta código fonte da solução parcialmente acabado (as partes fornecidas não estão sujeitas a alterações pelo aluno) para que o aluno complete;
  - `IMPROVEMENT` fornece o código fonte inicial correcto mas que não atinge todos os objectivos especificados na especificação do exercício (por exemplo, optimizar uma solução através da remoção de loops), pelo que o estudante tem de o modificar para resolver o exercício;
  - `BUG_FIX` dá uma solução com alguns bugs (e, possivelmente, testes reprovados) para fomentar o estudante a encontrar o código certo;
  - `FILL_IN_GAP` fornece código fonte com pedaços em falta e pede aos estudantes que as preencham com o código correcto;
  - `SPOT_BUG` fornece código com bugs e pede aos estudantes para simplesmente indicarem a localização dos bugs;
  - `SORT_BLOCK` parte uma solução em vários blocos de código, mistura-os, e pede aos estudantes que os ordenem.

Para esta finalidade, o esquema YAPExIL JSON pode ser dividido em quatro partes distintas: *metadata*, que contém propriedades simples que fornecem informações sobre o exercício; *presentation*, que diz respeito ao que é apresentado ao aluno; *assessment*, que abrange o que é utilizado na fase de avaliação; e *tools*, que inclui quaisquer ferramentas adicionais que o autor possa utilizar no exercício.

A figura seguinte apresenta o modelo de dados do formato YAPExIL, com a área de cada parte realçada numa cor distinta. As subsecções seguintes descrevem cada uma destas facetas.

![Modelo de dados YAPExIL](yapexil-data-model.svg)

## Metadata

*Metadata*, realçado a azul na figura, codifica informação básica sobre o exercício, que pode identificá-lo de forma única e ao(s) assunto(s) a que este se refere. Os elementos desta parte são principalmente utilizados para facilitar a pesquisa e consulta em grandes colecções de exercícios e a interoperabilidade entre sistemas. Por exemplo, um exercício pode ser identificado de forma única pelo seu `id`, que é um _Universally Unique Identifier_ (UUID) do exercício.

Além disso, os metadados incluem muitos outros atributos identificadores e não identificadores, tais como `title` do exercício d eprogramação, o `module` em que o exercício se encontra (ou seja, uma descrição do seu tópico principal), o nome do `author` do exercício, um conjunto de `keywords` relacionadas ao exercício, o seu `type` -- que pode ser `BLANK_SHEET`, `EXTENSION`, `IMPROVEMENT`, `BUG_FIX`, `FILL_IN_GAPS`, `SORT_BLOCKS`, ou `SPOT_BUG` --, o `event` em que o exercício foi criado (se houver), a `difficulty` (`BEGINNER`, `EASY`, `AVERAGE`, `HARD`, ou `MASTER`), o `status` atual (ou seja, se ainda é um exercício em `DRAFT`, `PUBLISHED` ou `UNPUBLISHED`, ou se foi movido para `TRASH`), e os registos temporais da criação e da última modificação (`created_at` e `updated_at`, respectivamente).

## Presentation

*Presentation*, destacado a verde na figura acima, inclui todos os elementos relacionados com a visualização do exercício, tanto por parte dos alunos como dos instrutores. Mais precisamente, estes serão os elementos colocados no ecrã enquanto o aluno resolve o problema, e quando o professor abre o exercício pela primeira vez.

Os elementos compatíveis incluem `instruction` -- um ficheiro de texto formatado com instruções para os professores sobre como entregar ou observações sobre o exercício --, `statement` -- um ficheiro de texto formatado com uma descrição completa do problema a resolver --, `embeddable` -- uma imagem, vídeo, ou outro ficheiro de recurso que possa ser referenciado na declaração --, e `skeleton` -- um ficheiro de código que contém parte de uma solução que é fornecido aos estudantes, a partir do qual estes podem começar a desenvolver o seu. 

A todos estes elementos são permitidas múltiplas instâncias, sendo apenas necessário uma única declaração nesta parte para se ter um exercício completo. Assim, os ficheiros de texto formatados podem ser traduzidos para outras linguagens ou formatos naturais, enquanto que os ficheiros de código podem ser escritos em várias linguagens de programação.

## Assessment

A avaliação automática é o objectivo final de uma linguagem de definição de exercícios de programação. A fim de avaliar um exercício de programação, o aluno deve submeter o código fonte a um motor de avaliação. O motor de avaliação utilizará então os elementos necessários e disponíveis para o avaliar.

Todos os elementos utilizados na avaliação pertencem à parte _Assessment_, destacados a vermelho na figura acima, e incluem `template` -- ficheiro de código contendo parte de uma solução que envolve o código dos estudantes sem o seu conhecimento --, `library` -- biblioteca de código que pode ser utilizada por soluções, tanto em fase de compilação como de execução --, `static_corrector` -- programa externo (associado à linha de comandos) que é invocado antes da correcção dinâmica para classificar/processar o código fonte do programa --, `dynamic_corrector` -- programa externo (associado à linha de comandos) que é invocado após a correcção principal para classificar cada execução --, `solution` -- um ficheiro de código com a solução do exercício fornecido pelo(s) autor(es), `test` -- um único teste público/privado com ficheiros de texto de _input/output_, um peso na avaliação global, e uma série de argumentos --, e -- um conjunto de testes público/privado.

Cada elemento desta parte também suporta múltiplas instâncias, sendo necessária apenas uma única solução e um teste ou conjunto de testes com um teste. Assim, podem ser fornecidos vários correctores, bibliotecas, teste/conjuntos de teste, e soluções em diferentes linguagens de programação.

## Tools

*Tools*, destacado em amarelo na figura acima, engloba quaisquer scripts adicionais que possam ser utilizados durante o ciclo de vida do exercício de programação. Estes incluem programas externos (e a sua linha de comando de execução) que geram (1) o feedback a dar ao aluno sobre a sua tentativa de alcançar uma solução (ou seja, `feedback_generator`) e os casos de teste para validar uma solução (ou seja, `test_generator`).