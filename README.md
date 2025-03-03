# DATA\_CAT.SH

Esse script pretende concatenar vários arquivos binários em um só e produzir um
header em C que contenha a posição em relação ao arquivo final e o tamanho de cada
um desses arquivos. Dessa forma, pode-se carregar uma única vez os dados em
um programa feito em C, em formato de uma array de bytes, e acessá-los
através do offset gerado.

Esse script está sob a licença GPLv3(+later).

## Uso

Deve-se criar uma pasta, contendo todos os arquivos
que deveram ser concatenados. Depois disso, basta digitar no terminal:

```
$ ./data_cat.sh ./res
```

Sendo `./res` o diretório da pasta.

O script gerará o header `inc_data.h` e o arquivo binário `data.bin`,
contendo todos os dados. Depois disso, basta ler o arquivo binário e incluir
o `inc_data.h` para conseguir os offsets.

