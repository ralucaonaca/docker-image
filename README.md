# virtual-dev-env
Learn about creating a virtual development environment and provisioning it


DOCKER - php apache image

to pull the image :
 
     sudo docker pull ralucaonaca/first-site:latest

to run the image :

     sudo docker run -d -p 127.0.0.1:8080:80 --name web -v /var/www/site:/var/www/site ralucaonaca/first-site 

DOCKER compose file

     1. cd docker-image-compose
   
     2. sudo docker-compose up
   
     3. daca nu cumva aveti imaginea de mai sus atunci trebuie sa se modifice docker-compose.yml 
          ca in loc de image : ralucaonaca/first-site:latest sa fie build: . - directorul curent unde se afla Dockerfile

     4. in var/www/site ad or change any file :)it's syncs auto with the container in var/www/site

     - mai trebuie sa setez porturile la mysql si parola si username-ul
 
     - apache ServerName sa setez in apache-config.conf
 

to build the image:

   1. Trebuie sa faci un git pull la acest repository sa faci checkout pe branch-ul de docker-image

   2. cd where is the Dockerfile
 
   3.  sudo docker build -t ralucaonaca/first-site:first .  # first - tag-ul first . - directorul unde se afla Dockerfile

   4.  si se ruleaza commanda de run de mai sus
 
   5. daca esti curios de a accesa containerul : sudo docker exec -it web /bin/bash

# Any questions ping me on whatever social media you want :)

