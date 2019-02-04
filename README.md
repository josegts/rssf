# SAN FERNANDO's API
 
## LOGIN
__POST__: `/rs-sanfernando/login`
### Parameters
`?servidor={codigoServidor}`
### Body
```javascript
{
    user: string,
    password: string
}
```

### Response

#### Success:  `200`
Example:
```javascript
{
    "status": "ok",
    "userId": 22,
    "nombre": "putin"
}
```

#### Error:  `401`
Example:
```javascript
{
    "status": "error"
}
```

## CLIENTES
__GET__: `/rs-sanfernando/rssf/clientes`
### Parameters
`?servidor={codigoServidor}`

### Response

#### Success:  `200`
Example:
```javascript
[
    {
        "id": 3944,
        "nombre": "MASPOLLO E.I.R.L.",
        "nombreLargo": "MASPOLLO, MASPOLLO E.I.R.L.",
        "codigoSap": "codigoSap",
        "correo": "correo@correo.com",
        "direccion1": "direccion1",
        "direccion2": "direccion2",
        "telefono": "telefono",
        "movil": "movil",
        "nif": "nif",
        "latitud": 1.234234234234234,
        "longitud": 19.234234234234,
        "mimetype": "image/jpg",
        "image": "29387skdjlsdfkldkfjld"
    },
    ...
]
```

## PRODUCTOS
__GET__: `/rs-sanfernando/rssf/productos`
### Parameters
`?servidor={codigoServidor}`

### Response

#### Success:  `200`

__Response Body__

```javascript
[
    {
        "productId": long,
        "prodcuctImage": string,
        "name": string,
        "costPrice": double,
        "posCategory": string,
        "unit": string,
        "igvVal": double,
        "operacion": long
    }
]
```

Example:
```javascript
[
    {
        "productId": 321,
        "productImage": "iVBORw0KGgoAAAA...",
        "name": "MOLLEJA DE POLLO X 2KG",
        "salePrice": 9.0,
        "posCategory": "POLLO",
        "unit": "kg",
        "igvVal": 1.37,
        "operacion": 10
    },
    ...
]
```
