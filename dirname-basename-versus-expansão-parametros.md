# dirname, basename versus expansão de parâmetros do shell
Os utilitários dirname e basename tem as funções conforme descrito no mamual:
dirname - retira o último componente do nome do arquivo
basename - retira o diretório e o sufixo dos nomes dos arquivos

```sh
dirname /usr/bin/cat
basename /var/log/syslog
```

E com a modificação na expansão de parâmetros do shell conseguimos esse mesmo resultado
```sh
file=/var/log/syslog
echo ${file%/*}      # equivalente ao dirname
echo ${file##*/}     # equivalente ao basename
```
