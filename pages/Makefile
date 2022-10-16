docker-build: 
	docker build -t ventuno-space .

docker-run:
	docker run -it  --rm --name ventuno-space -p 1111:1111 ventuno-space

start:
	make docker-build
	make docker-run
	