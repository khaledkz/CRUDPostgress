# CRUDPostgress

 

## docker:

we can use docker to manage the server it can help for developers and sysadmins to build, ship, and run distributed applications,

1-create 

```
docker-compose.yml
```
it contain 

,,,
version: '3.1'
services:
  db:
    image: postgres
    ports:
        - "5432:5432"
    environment:
        POSTGRES_USER: cyf
        POSTGRES_PASSWORD: password
        POSTGRES_DB: legodi
    restart: always
,,,

2-create migration folder

inside it create file 
,,,
20180808152913_product.js
,,,

this file should contain the schema of the table 

3-

```
exports.up = async (knex, Promise) => {
    await knex.schema.createTable('products', table => {
      table.increments('product_id')
      table.string('title').notNullable()
      table.string('price').notNullable()
    })
  }
  
  exports.down = function (knex, Promise) {
    return knex.schema.dropTable('classes')
  }
```


