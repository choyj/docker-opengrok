# A docker container for opengrok 1.1-rc33!

## Opengrok release 1.1-rc33 from oficial source:
Directly downloaded from official source:
https://github.com/OpenGrok/OpenGrok/releases/tag/1.1-rc33

## Additional info about the container:
* SSH with root access
* Tomcat 9
* JRE 8(Required for Opengrok 1.0)
* Preconfigured cron task for reindexing every hour)

## How to build:
cd <root of this git repo>
docker build -t my_opengrok .

## How to run your build:
docker run -d -v <path/to/your/src>:/src -p 8080:8080 -p 2222:22 my_opengrok

Point your web browser to http://localhost:8080/source.  If you get an error regarding the CONFIGURATION parameter and FileNotFoundException, wait a few minutes for the indexer to finish and then refresh the page.

## Location of opengrok sources, if needed:
https://github.com/oracle/opengrok

## SSH:
First inspect the docker container so you can find the address to connect, then ssh into it using root/root

