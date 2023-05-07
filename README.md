# Etiqa Server

Step to start the docker container contains of 
  - git submodule update --init --recursive (pull all submodules for first time)
  - etiqa_be (NodeJs ExpressJs Sequelize ORM)
  - etiqa_fe (Angular)
  - mysql (Database Server)
  
1. docker compose up
2. For first time setup, docker exce -it etiqa_be npm run migrate (For Sequelize migration)

The docker will setup all environment. Once ready the apps can access by following ports:
- etiqa_be - localhost:3000
- etiqa_fe - localhost:4200
- mysql - localhost:3306

# AWS EC2 Note
- Clone Repo
- Install NPM
- Install MySql
- Install PM2
- Start bin/api.js with PM2
- Update Inbound Rule of EC2
- Do Port Forwarding on Instance to 3000. (sudo iptables -A PREROUTING -t nat -p tcp --dport 3000 -j REDIRECT --to-ports 3000
)
- Sample Setup endpoint http://18.141.205.181:3000/

# AWS S3 Hosting for Front-end
- Upload Build file from etiqa-fe to S3 Bucket
- Config it to a statis web
- Start using it. Sample - http://etiqa-fe.s3-website-ap-southeast-1.amazonaws.com/
