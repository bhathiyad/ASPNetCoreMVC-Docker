#### Build Docker Image ########
cd aspnetapp
docker build -t aspnetapp .

##### Run Docker Image #########
docker run -d -p 8080:80 --name myapp aspnetapp


#######Pushing the docker image to docker hub repository######
docker login

docker tag aspnetapp bhathiyad/docker-aspnetapp:v1

docker push bhathiyad/docker-aspnetapp:v1