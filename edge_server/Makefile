docker-build:
	docker build -t edge_server:v1 .

docker-deploy:
	docker run -d -p 8000:80 edge_server:v1 