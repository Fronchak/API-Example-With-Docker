# Project Using Docker
## Requirements
* Docker

## How to use
1. Initiate Docker 
2. Open your terminal and run 'docker network create express-network-mysql-8'
3. Open your terminal in the database folder and run the following commands:
    1. Run 'docker build -t api-database-8 .'
    2. Run 'docker run --name mysql8-container -d -e MYSQL_ROOT_PASSWORD=12345678 -p 3306:3306 --network express-network-mysql-8 api-database-8'
4. Open your terminal in the api folder and run the following commands:
    1. Run 'docker build -t api8-na-rede .'
    2. Run 'docker run --name api-container -d -p 3000:3000 --network express-network-mysql-8 --rm api8-na-rede'
5. Now both containers are running and you can send a request to 'localhost:3000'