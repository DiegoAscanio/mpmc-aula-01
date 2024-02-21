<style>
  section {
    background-color: #dbdccf;
    background-size: cover;
  }

  .transparent {
    background-color: transparent!important;
  }

  section.transparent img {
    background-color: transparent!important;
  }

  .transparent-table-tr-td-th {
    background-color: rgba(0, 0, 0, 0.0) !important;
  }

  .cabecalho {
    position: absolute;
    top: 10%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 48px;
    font-weight: bold;
  }

  .conteudo {
    top: 30%;
    margin-top: 7.5vh;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }

  .conteudo-absoluto {
    position: absolute;
    top: 30%;
    margin-left: 5%;
    margin-right: 10%;
    font-size: 28px;
    text-align: justify;
  }
  
  .large {
    font-size: 24px;
  }

  .normal {
    font-size: 22px;
  }
  .regular {
    font-size: 18px;
  }
  .small {
    font-size: 16px;
  }
  .footnotesize {
    font-size: 14px;
  }
  .scriptsize {
    font-size: 12px;
  }
  .tiny {
    font-size: 10px;
  }
  .bold {
    font-weight: bold;
  }
  section.centered table {
    margin-left: auto;
    margin-right: auto;
  }
  section.lead p {
    text-align: justify;
  }
  section.lead h1 {
    text-align: center;
  }
  section.lead h2 {
    text-align: center;
  }
  
  .grid-50-50 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    text-align: justify;
  }

  .grid-66-33 {
    display: grid;
    grid-template-columns: 2fr 1fr;
    text-align: justify;
  }

  .grid-33-66 {
    display: grid;
    grid-template-columns: 1fr 2fr;
    text-align: justify;
  }

  .grid-element {
    margin-left: 5%;
    margin-right: 5%;
    padding-left: 2.5%;
    padding-right: 2.5%;
  }
  img[alt=grid-img] {
    width: 100%;
  }

</style>

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>


# Microcontroladores e Microprocessadores

## Aula 01

### Apresentação da Disciplina
### Breve Revisão da Arquitetura de Computadores e Apresentação de Microcontroladores e Microprocessadores

Prof. M.Sc. [Diego Ascânio Santos](mailto:ascanio@cefetmg.br)

Aula baseada nas apostilas do Prof. Dr. [Ricardo Kerschbaumer — IFC, Campus Luzerna](https://lattes.cnpq.br/5304374284779760)

CEFET-MG DECOMDV — Divinópolis, 2024


---

## Roteiro

1. Apresentação da disciplina.
2. Revisão sobre arquitetura de computadores.
    1. Fundamentos dos sistemas digitais.
    2. Registradores e memórias.
    3. Processadores.
        1. Arquitetura HARVARD vs VON NEUMANN.
        2. Arquitetura RISC vs CISC.
        3. Arquitetura interna dos processadores.
3. Microcontroladores vs Microprocessadores.


---

<div class="cabecalho">
    Apresentação da Disciplina — Objetivos
</div>

<div class="conteudo">

Proporcionar ao estudante conhecimentos sobre:

<div class="grid-50-50 regular" style="margin-top: 5vh;">

<div class="grid-element" style="border: solid 1px;" >

- Arquitetura de microprocessadores e microcontroladores;
- Unidade de controle e unidade lógica e aritmética;
- Memórias;
- Interfaces com dispositivos de entrada e saída;
- Dispositivos periféricos;
- Interrupções;
- Acesso a memórias;

</div>

<div class="grid-element" style="border: solid 1px;" >

- Barramentos e protocolos de comunicação;
- Aplicações de microprocessadores e microcontroladores;
- Programação de microcontroladores;
- Ferramentas para programação de microcontroladores;
- Aplicações de microcontroladores;

</div>

</div>

</div>


---

<div class="cabecalho">
    Apresentação da Disciplina — Metodologia de Ensino 
</div>

<div class="conteudo">

- Aulas teóricas expositivas;
- Aulas práticas em laboratório;
- Exercícios em sala de aula;
- Trabalhos práticos em laboratório;
- Atividades avaliativas teóricas;
- Trabalho interdisciplinar (Eletrônica - Teoria e Prática);

</div>


---

<div class="cabecalho" style="font-size: 36px;">
    Apresentação da Disciplina — Atividades Avaliativas Teóricas
</div>

<div class="conteudo regular">

<!-- _class: centered -->

| Atividade | Valor | Data       |
| --------- | ----- | ---------- |
| AV1       | 30    | 11/04/2024 |
| AV2       | 30    | 13/06/2024 |
| AVS\*     | 30    | 04/07/2024 |
| TID-I     | 13.33 | 03/05/2024 |
| TID-II    | 13.33 | 24/05/2024 |
| TID-III   | 13.33 | 26/06/2024 |

- A AVS é uma atividade avaliativa substitutiva que substitui a menor nota entre AV1 e AV2 para os alunos que fizerem as atividades ou para os alunos que as perderem. Todo o conteúdo da disciplina será cobrado.
- AV: Avaliação; TID: Trabalho Interdisciplinar; I, II e III: partes 1, 2 e 3 do trabalho interdisciplinar.

</div>


---

<div class="cabecalho">
    Apresentação da Disciplina — Atividades Avaliativas Práticas 
</div>

<div class="conteudo regular">
<div class="grid-50-50">
<div class="grid-element">

<!-- _class: centered -->
| Atividade | Valor | Data       |
| --------- | ----- | ---------- |
| TP1       | 15    | 08/05/2024 |
| TP2       | 15    | 15/05/2024 |
| TP3       | 15    | 22/05/2024 |
| TP4       | 15    | 29/05/2024 |
| TID-I     | 13.33 | 03/05/2024 |
| TID-II    | 13.33 | 24/05/2024 |
| TID-III   | 13.33 | 26/06/2024 |

</div>
<div class="grid-element">

**Siglas**

- TP: Trabalho Prático;
- TID: Trabalho Interdisciplinar;
- I, II e III: partes 1, 2 e 3 do trabalho interdisciplinar;

As datas das atividades avaliativas podem mudar — a critério meu e da profª Thabatta — de acordo com a conveniência da disciplina para melhor realização do trabalho interdisciplinar.

</div>
</div>
</div>


---

<div class="cabecalho">
    Apresentação da Disciplina — Trabalho Interdisciplinar
</div>

<div class="conteudo regular">

- O trabalho Interdisciplinar consiste em três etapas:
    - **I** — Definição do problema a ser resolvido, revisão de literatura e fundamentação teórica;
    - **II** — Proposta de uma metodologia para a resolução do problema e apresentação dos resultados parciais;
    - **III** — Apresentação dos resultados finais e conclusões.

- O trabalho será desenvolvido em grupos de até 4 alunos.
- Durante a realização do trabalho vocês escreverão um relatório científico associado ao problema escolhido;

</div>


---

<div class="cabecalho" style="font-size: 36px;">
    Apresentação da Disciplina — Trabalho Interdisciplinar
</div>

<div class="conteudo regular">

- Artefatos de Entregas do Trabalho Interdisciplinar — Explicação Completa:

    - **I** — Relatório parcial contendo o **resumo** do problema, a caracterização do problema na sua **introdução**, os **objetivos** que se pretendem alcançar, também na **introdução**, a **fundamentação teórica**, os **trabalhos relacionados** obtidos na revisão de literatura e as **referências bibliográficas** consultadas.
    - **II** — Solução prototipada construída e o relatório parcial contendo todas as seções anteriores, acrescidas da **metodologia** proposta para a resolução do problema — descrevendo de forma detalhada e objetiva os passos desenvolvidos para resolvê-lo — bem como, os **resultados parciais** obtidos até o momento entrega e, por fim, a descrição do que ainda falta ser construído na **conclusão** parcial desta etapa. Não esquecer de adicionar nas **referências bibliográficas** quaisquer novos autores que tenham sido citados, tanto na **fundamentação teórica** e nos **trabalhos relacionados** quanto na **metodologia**.
    - **III** — Solução final construída e relatório final contendo as etapas anteriores acrescido das atualizações na **metodologia** para obtenção dos **resultados finais** obtidos (também apresentados em sua própria seção) a **discussão** destes resultados finais,  a **conclusão** do trabalho, as possibilidades de **trabalhos futuros** e, por fim, todas as **referências bibliográficas** utilizadas.

</div>


---

<div class="cabecalho" style="font-size: 36px;">
    Apresentação da Disciplina — Trabalho Interdisciplinar
</div>

<div class="conteudo small" style="padding-top: 5vh;">

- Artefatos de Entregas do Trabalho Interdisciplinar — Explicação Resumida:

<div class="grid-50-50">    
<div class="grid-element">

- Etapa I
    - Relatório Parcial
        - Resumo
        - Introdução
            - Contextualização do Problema
            - Objetivos
        - Fundamentação Teórica (Explicação dos Conceitos que serão utilizados)
        - Trabalhos Relacionados (Autores que resolveram problemas semelhantes)
        - Referências Bibliográficas

</div>
<div class="grid-element">

- Etapa II
    - Relatório Parcial (da etapa I) acrescido de:
        - Metodologia
        - Resultados (parciais)
        - Conclusão (parcial)
    - Solução parcial prototipada
- Etapa III
    - Relatório Final (da etapa II) acrescido de:
        - Alterações na Metodologia
        - Resultados (finais)
            - Discussão dos Resultados
        - Conclusão
            - Trabalhos Futuros
        - Referências Bibliográficas
    - Solução final construída

</div>
</div>
</div>
</div>


---

<div class="cabecalho" style="font-size: 36px;">
    Apresentação da Disciplina — Trabalho Interdisciplinar
</div>
<div class="conteudo">

- O relatório do trabalho deverá seguir o modelo para publicação de artigos da SBC [(Sociedade Brasileira de Computação)](./arquivos/modelosparapublicaodeartigos.zip).
- O relatório deverá ser entregue em PDF e no seu respectivo formato editável (.docx, .odt ou .tex).
    - Não é obrigatória a adoção de um formato específico, mas, é fortemente recomendado que o relatório seja escrito em LaTeX.
- Durante as próximas aulas das disciplinas serão apresentadas possíveis idéias de problemas a serem resolvidos, à medida em que os conhecimentos forem adquiridos.

</div>


---

<div class="cabecalho" style="font-size: 36px;">
    Apresentação da Disciplina — 15 Pontos Extras
</div>
<div class="conteudo small">

- 5 pontos extras para estudantes filiados às organizações estudantis do campus (DA, Atlética, PET, equipes de competição, dentre outras) (ambas disciplinas);
- 5 pontos extras (ambas disciplinas) para quem fizer uma doação de sangue durante o semestre (comprovada por meio de documento oficial) ou no caso da impossibilidade de doação, que cumpra algum dos seguintes requisitos:
    - Ser doador cadastrado de medula óssea;
    - Atuar como voluntário junto à comunidade divinopolitana:
        - Em instituições filantrópicas (asilos, creches, hospitais, etc);
        - Junto a projetos sociais;
        - Em escolas públicas (estaduais ou municipais) ou serviços públicos / filantrópicos de saúde;
        - No atendimento a pessoas em situação de rua (pastoral do povo de rua, ONGs, etc);
        - Em atividades de preservação do meio ambiente;
        - No atendimento a crianças, adolescentes, mulheres, idosos, PCDs, pessoas LGBTQIA+ ou em situação de vulnerabilidade social;
        - Na promoção de ações em busca de igualdade racial e de gênero;
        - Na articulação política junto às lideranças em mandato (e não mandatárias) da cidade;
- 5 pontos extras para alunos que entregarem o relatório do TID no formato LaTeX (laboratório);
- 5 pontos extras para alunos que ajudarem na realização da semana da computação (teoria);

</div>
