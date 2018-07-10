A cybot conta com algumas funções extras....

# Utils
* * *
### Funções

- Translate
- get_sys - obtem o tipo do sistema(linux etc...)
- get_str - verifica se há letras no objeto enviado
- get_int - verifica se há numeros no objeto enviado
- figlet - cria um banner figlet
- dumps - json.dumps
- reboot - reinicia o sistema
- convert - convert bytes para (mb, tb, etc...)
- data - calendario
- clear - reconhece o sistema operacional e limpa o terminal
- list_dir - exibe os arquivos do direório enviado

## Traslate

```python
from cybot.utils import Translate

tr = Translate.translate

print(tr('en', 'Olá'))
```

`>>>Hello`

```python
from cybot.utils import Translate

tr = Translate.detec

print(tr('Olá'))
```

`>>>{'detected': pt-br, 'lang': Portuguese}`

## data

suponhamos que a data seja `02/07/2018` e o nosso relógio seja `12:2:13`...

```python
from cybot.utils import data

print(data.dia)
>>> 2
print(data.mes)
>>> 7
print(data.ano)
>>> 2018
print(data.hor)
>>> 12
print(data.segundo)
>>> 13
print(data.minuto)
>>> 2
print(data.hora)
>>> '12:2:13'
print(data.data)
>>> "2/7/2018"
print(data.log_data)
>>> '[12:2:13 2/7/2018] -'
print(data.datetime)
>>> {'time': '12:2:13', 'date': '2/7/2018'}
```

