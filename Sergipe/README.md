# Dados da Vacinação de Sergipe

Este repositório armazena scripts e arquivos gerados relacionados à vacinação do estado de Sergipe. 0s arquivos são gerados a partir do arquivo Excel disponiblizado pela Secretaria de Estado da Saúde nos boletins publicados quase que diariamente.

Desde do início da divulgação dos dados, a secretaria já usou diferentes tipos de arquivos para dispobibilizar os dados: PDF e Excel. O documento em Excel também já foi publicado com diferentes configurações das colunas. 

A seguir, segue o detalhamento do conteúdo publicado neste repositório. 

* **data/**: arquivos originais publicados pela Secretaria Estadual de Saúde. Eles são a base para gerar os arquivos .csv da pasta **output**.

* **old-notebooks**: notebooks para processar os arquivos antigos disponibilizados pela secretaria. Como teve mudanças constantes no formato e nas informações dos arquivos, novos notebooks foram gerados a cada mudança. Na pasta **Sergipe** está o arquivo mais recente com a indicação **latest** no nome. Os arquivos passados estão nesta pasta com a indicação de versões (v1, v2, v3 ...) no nome. 

A partir do dia 29/05 não mantive mais os históricos a cada mudança no arquivo original. Com mudanças constantes ficou inviável modificar todos os dias.

* **output/**: pasta de saída dos arquivos processados. Para cada arquivo disponibilizado pela secretaria é gerado um .csv com uma formação padrão para facilitar a leitura por meios automáticos. Esses arquivos estão dentro da pasta **historico/**. A pasta **output** possui também os arquivos:
    * **historico_sergipe.xsv**: quantitativo por dia de doses recebidas e aplicadas.
    * **relatorio_vacina_sergipe.csv**: relatório completo mais recente com os número da vacinação por município.
    * **data_vacinas_historico.cvs**: arquivo com o total de doses enviadas, aplicadas e a média móvel de 7 dias para cada dose.
    * **data_vacinas_municipio.csv**: total de doses enviadas e aplicas por município com a informação de cobertura da população vacinada  por doses.
    * **data_vacinas_grupos_estados.csv**: total de vacinados no estado por grupo de vacinação.
    * **data_vacinas_grupos_municipios.csv**: total de vacinados por município e por grupo de vacinação. 

Outros dois arquivos estão na raiz da pasta **Sergipe:**

* **processararquivos_vacina_latest.ipynb**: scripts para processamento do arquivo mais recente disponibilizado pela secretaria. 
* **processararquivos_vacina_latest.ipynb**: script que processa os arquivos .csv gerados para alimentar os gráficos  da visualização.


## Informações dos arquivo gerados

_Em construção!_

---
Desenvolvido por @adolfoguimaraes ([Twitter](https://twitter.com/adolfoguimaraes) | [Instagram](https://instagram.com/profadolfoguimaraes))