# DataBase

## Methods

* set
* get
* delete
* getall

* hset
* hget
* hdelete
* hgetall

## Usando saporra dlç

### set

```python
bot.set('oi', 'iai')
```

return: `>>> {'code': 'Ok'}`

### get

```python
bot.get('oi')
```

return: `>>> {'code': 'Ok', 'content': 'iai'}`

### delete

```python
bot.delete('oi')
```

return: `>>> {'code': 'Ok'}`

### set

```python
bot.set('oi', 'iai')
bot.set('aff', 'oush')

```

return: `>>> {'code': 'Ok', 'oi':'iai', 'aff': 'oush'}`

### hset

```python
bot.hset('a', 'b', 'c')
```

return: `>>> {'code': 'Ok'}`

### hget

```python
bot.hget('a', 'b')
```

return: `>>> {'code': 'Ok', 'content': 'c'}`

### hdelete

```python
bot.hdelete('a', 'b')
```

return: `>>> {'code': 'Ok'}`

### hgetall

```python
bot.hset('a', 'aff', 'ue')
bot.hset('a', 'meu pau', 'te ama')

bot.hgetall('a')
```

return: `>>> {'code': 'Ok', 'meu pau': 'te ama', 'aff': 'ue'}`
