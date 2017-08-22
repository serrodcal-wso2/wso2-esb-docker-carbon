# wso2-esb-docker-carbon

Proof of concept to build docker image using [spotify/dockerfile-maven plugin](https://github.com/spotify/dockerfile-maven).

Clone this repository in your local and run `$ mvn clean package dockerfile:build` to build Docker image. After thar, you have to run image `$ docker run -it serrodcal/docker-carbon:1.0.0`.

Port expose command not found and you have to expose manually. Read Dockerfile to know which ports are exposed.

This project has two parts: configuration project (API definitions to deploy it) and Carbon Application project (deployment unit in WSO2 ESB). Carbon Application project has configuration project as dependency. Finally, you have a WSO2 ESB 5.0.0 with your components in configuration project deployed in server instance.

[More information](https://github.com/spotify/dockerfile-maven) about plugin.


