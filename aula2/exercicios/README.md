# Exercício Workflows Git

Utilizar os dados de 2006 e 2007 de dados de atraso de vôos nos EUA,
disponíveis no link: [Data Expo 2009: Airline on time
data](https://doi.org/10.7910/DVN/HG7NV7).

Uma descrição dos dados presentes no dataset pode ser encontrada nesse
[link](http://stat-computing.org/dataexpo/2009/the-data.html).

Em duplas, utilizar o workflow de *feature branch* e escrever códigos em `bash script` para resolver os seguintes problemas.

Utilize os seguintes trechos de código como base para a implementação de funcionalidades. Para cada funcionalidade você deve implementar um *switch* (`-d`, `-t`, etc.) para cada funcionalidade ou modifique os que já existem para corrigí-las. 

Arquivo `flight-delays.sh`

```{bash}
#!/usr/bin/env bash

source functions.sh

while getopts ":dt" opt; do
    case ${opt} in
        d ) # process option h
            shift # Removes de First Argument from the queue
            download_datasets $1
        ;;
        t ) # process option t
        ;;
        \? ) echo "Usage: flight-delays.sh [-d] [-t]"
        ;;
  esac
done
```
Arquivo `functions.sh`

```{bash}
#!/usr/bin/env bash


function download_datasets {
    if [[ -d "$1" ]]; then
        echo "Baixando arquivo de 2006"
        wget -q 'https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/HG7NV7/EPIFFT' -O "${1}/2006.tar.bz2"
        echo "Baixando arquivo de 2007"
        wget -q 'https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/HG7NV7/2BHLWK' -O "${1}/2007.tar.bz2"
        exit 0
    else
        echo "Destino do download não existe"
        exit 1
    fi
}
```

Para cada *feature*, uma *issue* precisa ser aberta. A issue deve ser assinalada a um dos componentes da dupla. O *pull request* com a implementação da feature deve fechar a *issue* relacionada. Por favor verificar [essa referência](https://docs.github.com/en/github/managing-your-work-on-github/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword) sobre como relacionar uma *issue* a um *pull request*.

## Features

1. Corrigir o switch `-d` para não somente baixar o arquivo compactado, mas também descompactá-lo no mesmo diretório que se encontra.
    * Importante verificar se o arquivo já não foi descompactado;
    * O descompactador `dtrx` (disponível no linux e mac) pode ser utilizado para essa tarefa. 
1. Extrair número de atrasos, recebendo como parâmetro, o ano de referência, e.g.: `./flight-delays -n 2006` deve listar o número de vôos com atraso em 2006.
1. Mostrar lista de companhias aéreas que sofreram atraso, recebendo como parâmetro o ano de referência
    * Utilizar o arquivo [carriers.csv](https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/HG7NV7/3NOQ6Q)
    * Criar nova issue que altere a funcionalidade de download de dataset para também baixar esse arquivo
1. Mostrar a lista de Aeroportos com atrasos, recevendo como parâmetro o ano de referência
     * Utilizar o arquivo [airports.csv](https://dataverse.harvard.edu/api/access/datafile/:persistentId?persistentId=doi:10.7910/DVN/HG7NV7/XTPZZY)
     * Criar nova issue que altere a funcionalidade de download de dataset para também baixar esse arquivo
* Considerando o ano base como parâmetro: 
1. Contabilizar o número de atrasos ocorridos em cada aeroporto, listando o nome do aeroporto em uma coluna e o número de atrasos na segunda coluna (recebendo como parâmetro o ano base)
1. Contabilizar o número de atrasos ocorridos em cada companhia aérea, listando o nome da companhia em uma coluna e o número de atrasos na segunda coluna (recebendo como parâmetro o ano base)
1. Listar qual companhia teve o maior número de atrasos (atrasos somente na decolagem).
1. Listar qual aeroporto teve o maior número de atrasos (atrasos somente na decolagem).
1. Descobrir a média de atrasos na decolagem de cada voo;
1. Descobrir o voo com maior atraso em média e mostrar qual a média de atraso;
1. Descobrir dia da semana com maior número de atrasos e mostrar o número médio de atrasos;
1. Descobrir mês do ano com maior número de atrasos e mostrar o número de atrasos;
1. Listar aeroporto com o maior número de cancelamentos;
1. Listar voo com maior número de cancelamentos;
