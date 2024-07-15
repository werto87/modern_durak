## Install / Setup
- Download the repository
- create certificates and add them to your certificate store 'mkcert -install ; mkcert localhost'
- Fill out .env file in the development folder
- cd development
- git submodule update --init --recursive


## Build and Run
- docker-compose build && docker-compose down --volumes  && docker-compose up
- in your browser Go to "https://localhost/" 
