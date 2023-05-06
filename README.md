# Etiqa Server

Step to start the docker container contains of 
  - git submodule update --recursive --remote (pull all submodules for first time)
  - etiqa_be (NodeJs ExpressJs Sequelize ORM)
  - etiqa_fe (Angular)
  - mysql (Database Server)
  
1. docker compose up
2. For first time setup, docker exce -it etiqa_be npm run migrate (For Sequelize migration)

The docker will setup all environment. Once ready the apps can access by following ports:
- etiqa_be - localhost:3000
- etiqa_fe - localhost:4200
- mysql - localhost:3306
