# Api-Deliver-Spring-Boot

## Sobre o Projeto
Pensamos então em criar uma funcionalidade para o aplicativo da Uber que chamamos de “Uber Sport”, seria um ponto virtual que tem como objetivo servir de referência dentro destas regiões de dificil mobilidade urbana. Com o Uber Spot as pessoas destas regiões podem criar este pontos que irão servir de referência para os motoristas, e também para um ponto de encontro para compartilhar a corrida, economizando no trajeto. 

Com o UBER SPOT temos vantagens para todos, usuários usando mais a plataforma para seus deslocamentos e motoristas se sentindo mais seguros para aceitar corridas que antes evitavam, com o Uber SPOT existe também maior chance de sugerir corridas compartihadas. Assim fomentamos a utilização do UBER nestas regiões, melhorando a mobilidade delas através da inclusão e empoderamento dos usuários!

<hr/>

### Criar um spot (ponto virtual)

POST https://api-spring-boot-daniel.herokuapp.com/orders

#### exemplo de request.body, Informando Latitude e Longitude do spot: 

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
    } 
       
]
    
<hr/>

### Listar os produtos

GET https://api-spring-boot-daniel.herokuapp.com/products
    
#### exemplo de response: 

   [
    {
        "id": 6,
        "name": "Macarrão Espaguete",
        "price": 35.9,
        "description": "Macarrão fresco espaguete com molho especial e tempero da casa.",
        "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/macarrao_espaguete.jpg"
    },
    {
        "id": 7,
        "name": "Macarrão Fusili",
        "price": 38.0,
        "description": "Macarrão fusili com toque do chef e especiarias.",
        "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/macarrao_fusili.jpg"
    },
    {
        "id": 8,
        "name": "Macarrão Penne",
        "price": 37.9,
        "description": "Macarrão penne fresco ao dente com tempero especial.",
        "imageUrl": "https://raw.githubusercontent.com/devsuperior/sds2/master/assets/macarrao_penne.jpg"
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
 - Node.js: execução de JavaScript construído no motor V8 JavaScript do Chrome.
 - Express.js: framework de micro serviços do nodejs
 - Mongodb: Banco de dados NoSQL
 - Mongoose: gerenciar banco dados pelo node.js
 - nodemon: compilador de desenvolvimento
