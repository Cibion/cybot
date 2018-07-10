###A cybot necessita de alguns itens para funcionar...
***

###Webhook

Para isso, recomendo o uso do [Ngrok](http://ngrok.com/), basta seguir os passos da instalação.

###Montando o script `bot.py`

```python
import cybot #Importamos nossa Framework

bot = cybot.bot('api_token') #Criamos a Instância do bot

bot.setPlugins([list of plugins]) # Definimos a lista de plugins que ele utilizará

bot.start(url='webhook_url', port=webhook_port, app=__name__) # iniciamos definimos os dados de inicialização
```

###Explicando o script...

```python
bot = cybot.bot('api_token')
```
Nessa linha, criamos a instância do bot, o que nos permite manusear a api.

```python
bot.setPlugins([list of plugins]) # Definimos a lista de plugins que ele utilizará
```
Nessa linha, definimos a lista de plugins que o bot devrá processar na pasta `cybot/plugins`.

```python
bot.start(url='webhook_url', port=webhook_port, app=__name__) # iniciamos definimos os dados de inicialização
```
Nessa linha definimos a inicialização do script, onde:

* `url` é a url que o bot receberá os updates da api;
* `port` é a porta de entrada de dados no sistema, por padrão usamos a 3001.
* `app` é a identificação do arquivo, sempre coloque a tag `__name__`
* caso deseje receber os updates da api no bot.py, defina uma função e coloque-a logo após o objeto `port` assim: `handler=funcao_criada` 
