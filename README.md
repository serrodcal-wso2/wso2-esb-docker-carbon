# wso2-esb-docker-carbon

Proof of concept to build docker image using [spotify/dockerfile-maven plugin](https://github.com/spotify/dockerfile-maven).

1. Clone this repository in your local
2. Move to `echo/` and run `$ mvn clean install`.
3. Move to `echoApp/` and run `$ mvn clean package dockerfile:build` to build Docker image. 

After that, `$ docker run -it serrodcal/docker-carbon:1.0.0` to get an ESB docker image running.

Port expose command not found and you have to expose manually. Read Dockerfile to know which ports are exposed.

This project has two parts: configuration project (API definitions to deploy it) and Carbon Application project (deployment unit in WSO2 ESB). Carbon Application project has configuration project as dependency. Finally, you have a WSO2 ESB 5.0.0 with your components in configuration project deployed in server instance.

[More information](https://github.com/spotify/dockerfile-maven) about plugin.


