Join Zoom Meeting

https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fxebia.zoom.us%2Fj%2F85322308844%3Fpwd%3DdldSMGFOYTljRWtIa2wvbUpHUG1mdz09&amp;data=05%7C01%7Cincompany%40xebia.com%7C2ba4c281ecc44f2c526e08da9c9d7a10%7C3d4d17ea1ae44705947e51369c5a5f79%7C0%7C0%7C637994497408459775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&amp;sdata=n7I5B28%2F4Njo1UATwZUfUvOMSnunGc3SxzChL%2ByWLbg%3D&amp;reserved=0

Meeting ID: 853 2230 8844
Passcode: 116209
Manuel Riezebosch


https://github.com/riezebosch/allianz-docker


docker build
docker pull
docker run 
docker rm

docker ps -a


** If images not there, then docker will get from Registry"
docker run hello-world
docker run --name nginx-demo -p 1234:80 nginx:alpine


docker run --name allianz-demo-dockerfile2-run -p 2222:80 -d --rm allianz-demo-dockerfile2

docker run --name nginx-demo -d -p 1234:80 nginx:alpine
docker run --name nginx-demo -d -p 1234:80 --rm nginx:alphine
docker cp ./index.html nginx-demo:/usr/share/nginx/html
docker exec -ti nginx-demo ash
-- ash much smaller than bash
docker commit nginx-demo allianz-demo 



** From Dockerfile
Dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html
ENV SOME-VALUE "hello-allianz"
EXPOSE 80
WORKDIR ./app
COPY dist .
ENTRYPOINT ["java", "sample"]



docker build . --tag allianz-demo-dockerfile -f Dockerfile2
** --tag to indetify name of images "
** -f to indetify name of Dockerfile


Sample DockerFile
FROM adoptopenjdk

http://localhost:1234/weatherforecast

/usr/bin/java -Dsun.misc.URLClassPath.disableJarChecking=true -Xmx2048M -Xms128M \
        -Djava.io.tmpdir=/data/opt/middleware/deployment/agency-compensation/tmp \
        -jar /data/opt/middleware/deployment/agency-compensation/ncs-commission-service/sit/ncs-commission-service-6.0.0-SNAPSHOT.jar \
        --spring.profiles.active=sit



 