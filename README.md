# leadlovers
leadlovers app on Pluga

## Triggers

### new_lead (Rest Hook)

* Cadastro do hook:

Url:  http://llapi.leadlovers.com/webapi/RestHook?token={Token do Usuário}&applicationName=Pluga
Método: POST

Exemplo de objeto esperado:

```
{  
   "Target_url":"https://mydomain.com/hooks/foo/bar/",
   "Event":"new_lead_event"
}
```

Exemplo de resposta:

Status: 200

```
{  
   "StatusCode":200,
   "Message":"Sucesso ao inserir hook."
}
```

* Remoção do hook:

Url:  http://llapi.leadlovers.com/webapi/RestHook?token={Token do Usuário}&applicationName=Pluga
Método: DELETE

Exemplo de objeto esperado:

```
{  
   "Subscription_url":"https://mydomain.com/hooks/foo/bar/",
   "Event":"new_lead_event"
}
```

Exemplo de resposta:

Status: 200

```
{  
   "StatusCode":200,
   "Message":"Hook removido com sucesso."
} 
```

* Payload recebido pelo hook

```
{
  "Id":127809975,
  "Email":"testedata@pluga.co",
  "CreatedDate":"0001-01-01T02:00:00Z",
  "FixedFieldsEntity":{
    "Name":"Teste",
    "Phone":"315555555",
    "BirthDate":"10/01/1990 00:00:00",
    "Company":"Teste",
    "City":"Belo Horizonte",
    "State":"Minas Gerais"
  },
  "DynamicFields":[]
}
```

Copyright Pluga (c) 2018
