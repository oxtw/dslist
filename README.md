
# DSList

Projeto realizado por um estudo de Java com SpringBoot, onde criei uma API REST para um site de jogos categorizados que contém suas informações com descrições mais curtas, e mais detalhados quando visto separadamente.



## Documentação da API

### Retorna todos os jogos com uma descrição curta.

```http
  GET /api/games
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
|   games | `string` | /games |

#### Retorna as duas listas de categorias existentes de jogos.

```http
  GET /api/lists
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| lists   | `string` | /lists |




### Exemplo de "/lists"

```json
[
  {
    "id": 1,
    "name": "Aventura e RPG"
  },
  {
    "id": 2,
    "name": "Jogos de plataforma"
  }
]
```


## Buscar lista específica de jogos.

```http
  GET /api/lists/${id}/games
```

| Parâmetro   | Tipo       | Descrição                           |
| :---------- | :--------- | :---------------------------------- |
|   lists | `string` | /games |

#### Retorna todos os jogos na lista 1. Como só existem duas listas, você utiliza ou "1" ou "2"

```json
{
        "id": 6,
        "title": "Super Mario World",
        "year": 1990,
        "imgUrl": "https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/6.png",
        "shortDescription": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit esse officiis corrupti unde repellat non quibusdam! Id nihil itaque ipsum!"
    },
    {
        "id": 7,
        "title": "Hollow Knight",
        "year": 2017,
        "imgUrl": "https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/7.png",
        "shortDescription": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit esse officiis corrupti unde repellat non quibusdam! Id nihil itaque ipsum!"
    },
    {
        "id": 8,
        "title": "Ori and the Blind Forest",
        "year": 2015,
        "imgUrl": "https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/8.png",
        "shortDescription": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit esse officiis corrupti unde repellat non quibusdam! Id nihil itaque ipsum!"
    }, (...)
```

## Para retornar um jogo específico com descrição longa
```http
  GET /api/games/${id}
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| games/${id} | `string` |`é obrigatorio informar um id depois da rota para retornar um jogo especifico.`|


```json
{
    "id": 1,
    "title": "Mass Effect Trilogy",
    "year": 2012,
    "genre": "Role-playing (RPG), Shooter",
    "platforms": "XBox, Playstation, PC",
    "score": 4.8,
    "imgUrl": "https://raw.githubusercontent.com/devsuperior/java-spring-dslist/main/resources/1.png",
    "shortDescription": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Odit esse officiis corrupti unde repellat non quibusdam! Id nihil itaque ipsum!",
    "longDescription": "Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus dolorum illum placeat eligendi, quis maiores veniam. Incidunt dolorum, nisi deleniti dicta odit voluptatem nam provident temporibus reprehenderit blanditiis consectetur tenetur. Dignissimos blanditiis quod corporis iste, aliquid perspiciatis architecto quasi tempore ipsam voluptates ea ad distinctio, sapiente qui, amet quidem culpa."
}
```



## Stack utilizada

**Back-end** Java, SpringBoot, JPA, Hibernate, H2 database, postgresSQL, Docker, Postman, Git.

**Front-end** (Em construção) Utilizarei JavaScript, React.js, styled-components, Axios.
## Deploy

Site ao vivo

```bash
  https://dsgamelist.up.railway.app/games
```

