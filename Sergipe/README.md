# Dados da Vacinação de Sergipe

Nesta pasta você encontra os scripts e arquivos de entrada e saída dos dados de vacinação de Sergipe.

* **ProcessarArquivo_Vacinas.ipynb**: Arquivo com o script de processamento do arquivo do excel e do arquivo em pdf. 
* **data/**: pasta com os arquivos de entrada. É mantido sempre o arquivo mais recente disponibilizado pela secrataria de estado. Atualmente, a pasta possui o arquivo mais recente em formato do excel (datado de 23/02). A partir do dia 24/02, a secretaria passou a divulgar os dados em formato de PDF. Atualmente, o arquivo mais recente divulgado é o do dia 01/03. A partir de 03/03, a secretaria voltou a atualização dos dados em excel. A pasta possui o arquivo mais recente de 08/03 (com novas modificações na estrutura do excel. Foram incluídas algumas colunas de totais que não foram incluídas no csv final porque são facilmente calculadas com os dados apresentados).
* **output/**: pasta de saída do csv gerado a partir do arquivo mais recente da pasta data. Atualmente, o csv possui as informações do documento de 08/03.

## Informações do arquivo gerado

O **.csv** gerado possui, para cada município (informado na coluna `Municipio`), as informações sobre a população e o quantitativo de doses enviadas e aplicadas para cada um dos grupos vacinados. As informações de cada grupo vacinado estão nas colunas do documento original disponibilizado pela secretaria. Para facilitar o uso do arquivo e enventual referência das colunas, essa informação foi retirada do nome da coluna e associadas a nomenclatura de grupos. Segue a descrição de cada grupo:

* Grupo 1: Trabalhadores da Saúde
* Grupo 2: Pessoas com 60 anos ou mais e deficientes Institucionalizados
* Grupo 3: Índio Aldeado
* Grupo 4: Pessoas com 90 ou mais
* Grupo 5: Idosos de 78 a 89 anos

O arquivo .csv final ficou com as seguintes colunas:

* **Municipio** 
* **Grupo1_Populacao**
* **Grupo1_Dose1_Enviadas**
* **Grupo1_Dose1_Aplicadas**
* **Grupo1_Dose2_Enviadas**
* **Grupo1_Dose2_Aplicadas**
* **Grupo2_Populacao**
* **Grupo2_Dose1_Enviadas**
* **Grupo2_Dose1_Aplicadas**
* **Grupo2_Dose2_Enviadas**
* **Grupo2_Dose2_Aplicadas**
* **Grupo3_Populacao**
* **Grupo3_Dose1_Aplicadas**
* **Grupo3_Dose2_Aplicadas**
* **Grupo4_DosesEnviadas**
* **Grupo4_Doses1_Aplicadas**
* **Grupo4_Doses2_Aplicadas**
* **Grupo5_DosesEnviadas**
* **Grupo5_Doses_Aplicadas_7879**
* **Grupo5_Doses_Aplicadas_8084**
* **Grupo5_Doses_Aplicadas_8589**
* **Grupo5_Cobertura**,
* **Total_Dose1_Enviadas**
* **Total_Dose1_Aplicadas**
* **Total_Dose2_Enviadas**
* **Total_Dose2_Aplicadas**

Os totais de Sergipe e o % de cobertura foram retirados do arquivo final já que são informações que podem ser calculadas com os dados do arquivo.

---
Desenvolvido por @adolfoguimaraes ([Twitter](https://twitter.com/adolfoguimaraes) | [Instagram](https://instagram.com/profadolfoguimaraes))