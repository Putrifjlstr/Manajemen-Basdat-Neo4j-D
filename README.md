# Parking-Lot
# Cara Instalasi Neo4j via docker
* buka command line dan run `dockel pull neo4j`
<img width="508" alt="image" src="https://user-images.githubusercontent.com/101171434/209582961-6f69a642-a539-46ae-b5e4-a8cb2317bc24.png">

* buat folder baru di cmd dengan `mkdir neo4j`
* dan buka di visual studio code dengan `code .\neo4j`
* buat file dengan nama "docker-compose.yml"
* masukkan code :
`````Javascript 
version: "3.8"
services:
  neo4j:
    image:neo4j: 4.4.16-community
    ports: 
      - 7888:7474
      - 7999:7687
    restart: unless-stopped
    environment:
    - NEO4J_AUTH=neo4j/password
    volumes:
    - ./db/data:/data
    - ./db/conf:/conf
    - ./db/logs:/logs
    - ./db/plugins:/plugins
    `````



