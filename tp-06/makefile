APACHE=apache:curl
NGINX=nginx:curl

builds: build_apache build_ngnix

build_apache:
	docker build -t $(APACHE) ./ -f Docfileapache

build_ngnix:
	docker build -t $(NGINX) ./ -f Docfilenginx

runconteners: contener1 contener2 contener3 contener4

contener1:
	docker run -dp 8081:80 --name contener_1_1 --network reseau_1 $(APACHE)

contener2:
	docker run -dp 8082:80 --name contener_1_2 --network reseau_1 $(NGINX)

contener3:
	docker run -dp 8083:80 --name contener_2_1 --network reseau_2 $(APACHE)

contener4:
	docker run -dp 8084:80 --name contener_2_2 --network reseau_2 $(NGINX)

networks: network1 network2

network1:
	docker network create reseau_1
network2:
	docker network create reseau_2
cleannet:
	docker network rm -f reseau_1 reseau_2