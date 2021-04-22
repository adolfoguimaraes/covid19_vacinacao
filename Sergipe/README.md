# Dados da Vacinação de Sergipe

Este repositório armazena scripts e arquivos gerados relacionados à vacinação do estado de Sergipe. 0s arquivos são gerados a partir do arquivo Excel disponiblizado pela Secretaria de Estado da Saúde nos boletins publicados quase que diariamente.

Desde do início da divulgação dos dados, a secretaria já usou diferentes tipos de arquivos para dispobibilizar os dados: PDF e Excel. O documento em Excel também já foi publicado com diferentes configurações das colunas. 

A seguir, segue o detalhamento do conteúdo publicado neste repositório. 

* **data/**: arquivos originais publicados pela Secretaria Estadual de Saúde. Eles são a base para gerar os arquivos .csv da pasta **output**.

* **old-notebooks**: notebooks para processar os arquivos antigos disponibilizados pela secretaria. Como teve mudanças constantes no formato e nas informações dos arquivos, novos notebooks foram gerados a cada mudança. Na pasta **Sergipe** está o arquivo mais recente com a indicação **latest** no nome. Os arquivos passados estão nesta pasta com a indicação de versões (v1, v2, v3 ...) no nome. 

* **output/**: pasta de saída dos arquivos processados. Para cada arquivo disponibilizado pela secretaria é gerado um .csv com uma formação padrão para facilitar a leitura por meios automáticos. Esses arquivos estão dentro da pasta **historico/**. A pasta **output** possui também os arquivos:
    * **historico_sergipe.csv**: quantitativo por dia de doses recebidas e aplicadas.
    * **historico_vacina_sergipe.csv**: relatório completo mais recente com os número da vacinação por município.

Outros dois arquivos estão na raiz da pasta **Sergipe:**

* **processararquivos_vacina_latest.ipynb**: scripts para processamento do arquivo mais recente disponibilizado pela secretaria. 
* **processar_historico.ipynb**: script que processa os arquivos .csv gerados para gerar o arquivo com o histórico de doses enviadas e aplicadas por dia. 


## Informações do arquivo gerado


### Arquivo relatorio_vacina_sergipe.csv

O **.csv** gerado possui, para cada município (informado na coluna `Municipio`), as informações sobre a população e o quantitativo de doses enviadas e aplicadas para cada um dos grupos vacinados. As informações de cada grupo vacinado estão nas colunas do documento original disponibilizado pela secretaria. Para facilitar o uso do arquivo e enventual referência das colunas, essa informação foi retirada do nome da coluna e associadas a nomenclatura de grupos. Segue a descrição de cada grupo:

* Grupo 1: Trabalhadores da Saúde
* Grupo 2: Pessoas com 60 anos ou mais e deficientes Institucionalizados
* Grupo 3: Índio Aldeado
* Grupo 4: Pessoas com 80 anos e mais
* Grupo 5: Pessoas de 70 a 79 anos (apesar de informar de 70 a 79, até 11/03 apenas acima de 75 tinham sido vacinados).
* Grupo 6: Pessoas de 60 a 69 anos (apesar de existir essa  coluna, até 11/03 esse grupo não tinha iniciado a vacinação).
* Grupo 7: Situação de Rua
* Grupo 8: Quilombolas
* Grupo 9: Trabalhadores das forças de segurança
* Grupo 10: Pessoas com Síndrome de Dowm e Autismo
* Grupo 11: Outros (População vacinada com resíduos de vacinas ao final do dia) 


O arquivo .csv final ficou com as seguintes colunas:

* codigo_municipio
* municipio
* populacao_total
* populacao_grupo4
* populacao_grupo5
* populacao_grupo6
* enviadas_dose1
* enviadas_dose2
* aplicadas_dose1
* aplicadas_dose2
* aplicadas_dose1_grupo1
* aplicadas_dose1_grupo2
* aplicadas_dose1_grupo3
* aplicadas_dose1_grupo4
* aplicadas_dose1_grupo5
* aplicadas_dose1_grupo6
* aplicadas_dose1_grupo7
* aplicadas_dose1_grupo8
* aplicadas_dose1_grupo9
* aplicadas_dose1_grupo10
* aplicadas_dose1_grupo11
* aplicadas_dose2_grupo1
* aplicadas_dose2_grupo2
* aplicadas_dose2_grupo3
* aplicadas_dose2_grupo4
* aplicadas_dose2_grupo5
* aplicadas_dose2_grupo6
* aplicadas_dose2_grupo7
* aplicadas_dose2_grupo8
* aplicadas_dose2_grupo9
* aplicadas_dose2_grupo10
* aplicadas_dose2_grupo11

Os totais de Sergipe e o % de cobertura foram retirados do arquivo final já que são informações que podem ser calculadas com os dados do arquivo.

### Arquivo historico_sergipe.csv

Neste arquivo são armazenadas as informações do histórico de vacinação no estado. Cada linha corresponde a data do boletim divulgado. As colunas possuem as seguintes informações sobre as doses enviadas e aplicadas em todo estado:

* envidas_dose1
* aplicadas_dose1
* enviadas_dose2
* aplicadas_dose2

---
Desenvolvido por @adolfoguimaraes ([Twitter](https://twitter.com/adolfoguimaraes) | [Instagram](https://instagram.com/profadolfoguimaraes))