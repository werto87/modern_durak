# Modern Durak Project
## Modern Durak Project Page
### What is Modern Durak
Modern Durak models the russian card game [Durak](https://en.wikipedia.org/wiki/Durak). Durak is russian and means fool. The name Modern Durak is a joke combining 'modern' from modern c++ and 'durak' from the game Durak. You can play online against other players (Quick, Ranked, Custom) or play against a computer controlled opponent (Puzzle). I am self hosting the game [here](https://modern-durak.com). Feel free to create an issue if something is not working or you have a question.
### How to deploy
- run development on your local machine for bug fixing and testing ([development deployment guide](https://github.com/werto87/modern_durak/blob/main/development/README.md))
- run production on the production server to deploy the app ([production deployment guide](https://github.com/werto87/modern_durak/blob/main/production/README.md))
## Project Structure
Modern durak is made from 3 projects:
### Frontend  
#### [GUI](https://github.com/werto87/modern_durak_client) 
Web GUI communicates with the backend.
### Backend 
The backend is made from 2 projects.
#### [modern_durak_matchmaking_proxy](https://github.com/werto87/modern_durak_matchmaking_proxy)
Login matchmaking proxy connects to game, starts a game
and then forwards all messages from GUI to game and vice versa. Has support for ranked play, login, relog and send message to user.
#### [modern_durak_game](https://github.com/werto87/modern_durak_game)
Game contains the logic for the actual game. Allows to play against other players or the computer controlled opponent.
### dependencies made by me
#### [durak_computer_controlled_opponent](https://github.com/werto87/durak_computer_controlled_opponent)
Simulates the game durak and creates a lookup tree with the results.
#### [small_memory_tree](https://github.com/werto87/small_memory_tree)
Changes representation from trees to save memory and to store them easily into a database.
#### [durak](https://github.com/werto87/durak)
Rules for the card game durak.
#### [confu_json](https://github.com/werto87/confu_json)
Generates boilerplate code for json parsing to string and back into user defined type.
#### [confu_soci](https://github.com/werto87/confu_soci)
Generates boilerplate for the database access library soci.
### dependencies not made by me. My projects would not be possible with out them <3
#### [boost](https://github.com/boostorg/boost)
Basically all my projects depend on boost. Especially asio and beast for networking, json for json parsing, mpl and fusion for template programming.
#### [boost::ext::sml](https://github.com/boost-ext/sml)
The business logic in the two backend applications is modeled using state machines from sml. This library allows to describe the state machine using a dsl and also to generate uml diagrams without writing extra code.
#### [magic enum](https://github.com/Neargye/magic_enum)
Used for enum printing.
#### [soci](https://github.com/SOCI/soci)
Used for database access.
## Tools and technologies used in this project
### Compiler
clang++ and g++.
### Build System
CMake
### Dependency Manager
conan
### Artifactory
jfrog artifactory
### version control
git
### Ci
Git hub actions
### Container and Deployment
Docker
### Web Server
Nginx
### Web Hosting
netcup virtual server
### Os
arch linux
### Tls Certificate
Let's Encrypt
