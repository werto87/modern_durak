## Install / Setup
- Download the repository  
In the production folder
- Fill out .env file 
- Replace "modern-durak.com" in user_conf.d/00_nginx.conf with your domain

## Run the app
In the production folder run:
- docker-compose down --volumes  && docker-compose pull  && docker-compose up
- Go to your domain you should now get the client served.
