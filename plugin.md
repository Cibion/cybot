#Plugins

O bot funciona com um sistema de plugins desenvolvido para ler os nomes em uma lista e importálos apenas quando recebe um update.

##Funcionamento

* Definimos primeiramente, o que o bot executará, por padrão ele recebe os objetos `msg` e `bot`.

```python
def any(msg, bot):
	bot.sendMessage(msg['chat']['id'], 'Start!') #Função de enviar mensagem.
``` 

* Depois configuramos o reconhecimento do modulo

```python
handler = {
	'name'    : 'Any', # Nome do módulo, será exibido ao processar o mesmo.
	'pattern' : '/any', # Comando para ser reconhecido, caso seja masi de um, crie uma lista.
	'template':  any, # A função que ele executará. (o def criado logo acima)
	'type'	  : ['message'], # Tipo de updates que o bot deverá reconhecer para processar o módulo ( message, callback_query, edit_message_text ...)
	'cmd'	    : True, # True para comando e False para I.A.
}
```

Por padrão, o bot passa o objeto `msg` em forma de classe, 
caso queira, o bot pode passar o objeto como classe, 
basta adicionar `'config' : {'msg': 'class'}` ao handler.
