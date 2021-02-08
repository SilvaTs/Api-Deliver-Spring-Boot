# Api-Deliver-Spring-Boot

## Sobre o Projeto

Semana DevSuperior 2.0

Nesse projeto foi aplicado todos conceitos para desenvolver uma api rest com spring boot,
utilizando os endpoints POST,PUT e GET,e Implantamos o projeto no Heroku.

<hr/>

### Cadastrar um pedido

POST https://api-spring-boot-daniel.herokuapp.com/orders

#### exemplo de response: 

{
        "adress": "Avenida Maracana, 1500",
        "latitude": -23.56168,
        "longitude": -46.656139,      
        "products": [
          {
              "id": 2
          },
          {
              "id": 5
          }
        ] 
}
    
<hr/>

### Listar os pedidos

GET  https://api-spring-boot-daniel.herokuapp.com/orders
    
#### exemplo de response: 

[
    {
        "id": 7,
        "adress": "Avenida Paulista, 1500",
        "latitude": -23.56168,
        "longitude": -46.656139,
        "moment": "2021-01-01T09:00:00Z",
        "status": "PENDING",
        "products": [
            {
                "id": 5,
                "name": "Risoto Funghi",
                "price": 59.95,
                "description": "Risoto Funghi feito com ingredientes finos e o toque especial do chef.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/risoto_funghi.jpg"
            },
            {
                "id": 7,
                "name": "Macarrão Fusili",
                "price": 38.0,
                "description": "Macarrão fusili com toque do chef e especiarias.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/macarrao_fusili.jpg"
            }
        ]
    },
    {
        "id": 1,
        "adress": "Avenida Paulista, 1500",
        "latitude": -23.56168,
        "longitude": -46.656139,
        "moment": "2021-01-01T10:00:00Z",
        "status": "PENDING",
        "products": [
            {
                "id": 1,
                "name": "Pizza Bacon",
                "price": 49.9,
                "description": "Pizza de bacon com mussarela, orégano, molho especial e tempero da casa.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/pizza_bacon.jpg"
            },
            {
                "id": 4,
                "name": "Risoto de Carne",
                "price": 52.0,
                "description": "Risoto de carne com especiarias e um delicioso molho de acompanhamento.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/risoto_carne.jpg"
            }
        ]
    },
    {
        "id": 4,
        "adress": "Avenida Paulista, 1500",
        "latitude": -23.56168,
        "longitude": -46.656139,
        "moment": "2021-01-01T12:00:00Z",
        "status": "PENDING",
        "products": [
            {
                "id": 2,
                "name": "Pizza Moda da Casa",
                "price": 59.9,
                "description": "Pizza à moda da casa, com molho especial e todos ingredientes básicos, e queijo à sua escolha.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/pizza_moda.jpg"
            },
            {
                "id": 6,
                "name": "Macarrão Espaguete",
                "price": 35.9,
                "description": "Macarrão fresco espaguete com molho especial e tempero da casa.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/macarrao_espaguete.jpg"
            }
        ]
    },
    {
        "id": 6,
        "adress": "Avenida Paulista, 1500",
        "latitude": -23.56168,
        "longitude": -46.656139,
        "moment": "2021-01-01T14:00:00Z",
        "status": "PENDING",
        "products": [
            {
                "id": 1,
                "name": "Pizza Bacon",
                "price": 49.9,
                "description": "Pizza de bacon com mussarela, orégano, molho especial e tempero da casa.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/pizza_bacon.jpg"
            },
            {
                "id": 5,
                "name": "Risoto Funghi",
                "price": 59.95,
                "description": "Risoto Funghi feito com ingredientes finos e o toque especial do chef.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/risoto_funghi.jpg"
            }
        ]
    },
    {
        "id": 3,
        "adress": "Avenida Paulista, 1500",
        "latitude": -25.439787,
        "longitude": -49.237759,
        "moment": "2021-01-01T16:00:00Z",
        "status": "PENDING",
        "products": [
            {
                "id": 3,
                "name": "Pizza Portuguesa",
                "price": 45.0,
                "description": "Pizza Portuguesa com molho especial, mussarela, presunto, ovos e especiarias.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/pizza_portuguesa.jpg"
            },
            {
                "id": 4,
                "name": "Risoto de Carne",
                "price": 52.0,
                "description": "Risoto de carne com especiarias e um delicioso molho de acompanhamento.",
                "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/risoto_carne.jpg"
            }
        ]
    }
]
   
    
<hr/> 

### Atualizar pedidos

PUT https://api-spring-boot-daniel.herokuapp.com/orders/3/delivered
    
#### exemplo de response: 

{
    "id": 3,
    "adress": "Avenida Paulista, 1500",
    "latitude": -25.439787,
    "longitude": -49.237759,
    "moment": "2021-01-01T16:00:00Z",
    "status": "DELIVERED",
    "products": [
        {
            "id": 3,
            "name": "Pizza Portuguesa",
            "price": 45.0,
            "description": "Pizza Portuguesa com molho especial, mussarela, presunto, ovos e especiarias.",
            "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/pizza_portuguesa.jpg"
        },
        {
            "id": 4,
            "name": "Risoto de Carne",
            "price": 52.0,
            "description": "Risoto de carne com especiarias e um delicioso molho de acompanhamento.",
            "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/risoto_carne.jpg"
        }
    ]
}
    
<hr/>
 
## Tecnologias usadas na API:
 - Spring Boot: No Desenvolvimento da api.
 - IDE: Eclipse
 - Postgres: Banco de dados
 - Host: Heroku
 - Java: versão 11
