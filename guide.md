# Guide for develop flowqio scenario

   * Scenario use docker-compose v2 format as enviroment profile
   
   * Scenario use markdown format as content profile

   * Add customization template feature



# A scenario structure

fixed name :
   
   * docker-compose.yaml  // envrionment profile
   
   * index.json  // content profile
   
   * other file use markdown format , must be declar in index.json
   
envrionment :
   
   * {OID} is scenarion instance creator id ,defualt use for docker-compose networks, storge config.
   
content:
   
   * `git status`{{execute}}   //{{execute}} will be creator click link, this link can be send to container instance.
     
   
## Scenarion Example - git-startup

   [git-startup](https://github.com/flowqio/scenario/git-startup)
