# modern-durak project
## modern-durak Project page
### what is modern durak
Modern durak models the russian card game [durak](https://en.wikipedia.org/wiki/Durak). Durak is russian and means fool. The name modern durak is a joke combining 'modern' from modern c++ and 'durak' from the game durak. You can play online against other players (quick game, ranked game) or play against a computer controlled opponent (puzzle).
### how to deploy
- run development on your local machine for bug fixing and testing ([development deployment guide](https://github.com/werto87/modern_durak/blob/main/development/README.md))
- run production on the production server to deploy the app ([production deployment guide](https://github.com/werto87/modern_durak/blob/main/production/README.md))
## project structure
Modern durak is made from 3 projects:
### Frontend  
#### [Ui](https://github.com/werto87/modern_durak_client) 
Web ui communicates with the backend.
### Backend 
The backend is made from 2 projects.
#### [login matchmaking proxy](https://github.com/werto87/matchmaking_proxy)
Reusable login matchmaking proxy connects to game, starts a game
and than forwards all messages from ui to game and vice versa. Has support for ranked play, login, relog and send message to user.
#### [game](https://github.com/werto87/example_of_a_game_server)
Game contains the logic for the actual game. Allows to play against other players or the computer controlled opponent.
### transitive dependencies made by me
#### [durak_computer_controlled_opponent](https://github.com/werto87/durak_computer_controlled_opponent)
Simulates the game durak and creates a lookup tree with the results.
#### [small_memory_tree](https://github.com/werto87/small_memory_tree)
Changes representation from trees to save memory and to store them easily into an database.
#### [durak](https://github.com/werto87/durak)
Rules for the card game durak.
#### [confu_json](https://github.com/werto87/confu_json)
Generates boilerplate code for json parsing to string and back into user defined type.
#### [confu_soci](https://github.com/werto87/confu_soci)
Generates boilerplate for the database access library soci.
### transitive dependencies not made by me. My projects would not be possible with out them <3
#### [boost](https://github.com/boostorg/boost)
Basically all my projects depend on boost. Especially asio and beast for networking, json for json parsing mpl and fusion for template programming.
#### [boost::ext::sml](https://github.com/boost-ext/sml)
The business logic in the two backend applications is modeled using a state machines from sml. This library allows to describe the state machine using a dsl and also to generate uml diagrams without writing extra code.
#### [magic enum](https://github.com/Neargye/magic_enum)
Used for enum printing.
#### [soci](https://github.com/SOCI/soci)
Used for database access.
## Tools and technologies used in this project
### compiler
clang++ and g++.
### build system
CMake
### dependency manager
conan
### artifactory
jfrog artifactory
### version control
git
### ci
Git hub actions
### container and deployment
Docker
### web server
Nginx
### web hosting
netcup virtual server
### os
arch linux
### tls certificate
Let's Encrypt
