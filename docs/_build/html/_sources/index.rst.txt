Documentação do estudo com pacientes de câncer colorretal
=========================================================

Autores
-------

* Gisele Fernandes - A.C. Camargo Cancer Center
* Lucas Buk Cardoso - Instituto Mauá de Tecnologia
* Maria Paula Curado - A.C. Camargo Cancer Center
* Stela Verzinhasse Peres - Fundação Oncocentro de São Paulo
* Tatiana Natasha Toporcov - Faculdade de Saúde Pública da Universidade de São Paulo
* Vanderlei Cunha Parro - Instituto Mauá de Tecnologia
* Victor Wünsch Filho - Fundação Oncocentro de São Paulo e Faculdade de Saúde Pública da Universidade de São Paulo

Introdução
------------

A seguir está apresentada a documentação do estudo de pacientes com câncer colorretal desenvolvido pelo Núcleo de Sistemas Eletrônicos Embarcados do Intituto Mauá de Tecnologia, em parceria com a FOSP (Fundação Oncocentro de São Paulo), Faculdade de Saúde Pública da USP (Universidade de São Paulo) e A.C. Camargo Cancer Center.

O projeto visa a utilização de algoritmos de aprendizado de máquina para realizar previsões e identificar as variáveis mais importantes na sobrevida de pacientes com câncer colorretal, residentes no estado de São Paulo. 

O conjunto de dados utilizado é aberto, chamado Registro Hospilar de Câncer (RHC), e está disponível no site da `FOSP <http://www.fosp.saude.sp.gov.br/fosp/diretoria-adjunta-de-informacao-e-epidemiologia/rhc-registro-hospitalar-de-cancer/banco-de-dados-do-rhc/>`_. Desses dados foram selecionados pacientes com câncer colorretal tratados entre 2000 e 2021.

Sumário
-------

A documentação será dividida em tópicos para facilitar o entendimento e organização. São elas:

* Bibliotecas, instalações e funções - Todas as bibliotecas que foram utilizadas no projeto e as funções criadas para utilização no projeto.
* Análise dos dados, criação de novas colunas e primeiro pré-processamento - Exploração do conjunto de dados, limpeza e primeira preparação das colunas. 
* Classificação - pré-processamento completo dos dados, treinamento e validação dos modelos de machine learning. Os labels das análises são:

   * obito_geral: 0 se paciente está vivo e 1 se morreu por qualquer razão;

   * obito_cancer: 0 se paciente está vivo e 1 se morreu devido ao câncer;

   * vivo_ano1: 0 se paciente não sobreviveu e 1 se sobreviveu ao primeiro ano após diagnóstico;

   * vivo_ano3: 0 se paciente não sobreviveu e 1 se sobreviveu ao terceiro ano após diagnóstico;

   * vivo_ano5: 0 se paciente não sobreviveu e 1 se sobreviveu ao quinto ano após diagnóstico.

.. note::  As análises de sobrevida (vivo ano 1, 3 e 5) exigem uma filtragem a mais dos dados, pois é necessário garantir que o paciente tenha sido acompanhado pelo período de interesse da análise. Por exemplo, para a análise de sobrevida de 3 anos, o paciente que está vivo precisa ter sido acompanhado por pelo menos 3 anos após o diagnóstico da doença.

A imagem abaixo mostra as seleções feitas no conjunto de dados, chegando no número de pacientes utilizado em cada uma das análises.

.. image:: fluxo-dados.png
    :width: 720px
    :align: center
    :height: 400px
    :alt: alternate text


Os códigos completos estão disponíveis em `Github <https://github.com/Lucas-Buk/colorectal>`_.

.. toctree::
   :maxdepth: 1
   :caption: Bibliotecas e Funções

   Funções

.. toctree::
   :maxdepth: 1
   :caption: Análise dos dados

   Colorretal - preprocessing

.. toctree::
   :maxdepth: 1
   :caption: Óbito geral

   Colorretal - obito_geral

.. toctree::
   :maxdepth: 1
   :caption: Óbito por câncer

   Colorretal - obito_cancer

.. toctree::
   :maxdepth: 1
   :caption: Sobrevida um ano

   Colorretal - vivo_ano1

.. toctree::
   :maxdepth: 1
   :caption: Sobrevida três anos

   Colorretal - vivo_ano3

.. toctree::
   :maxdepth: 1
   :caption: Sobrevida cinco anos

   Colorretal - vivo_ano5