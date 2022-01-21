.PHONY: build_docker
build_docker:
	rm -rf front && cp -r ../../tduck-front/dist front && \
	docker build -t tecdo/tduck .

tduck-api.jar:
	cd ../ && mvn package && cd docker && \
	cp ../tduck-api/target/tduck-api.jar ./

.PHONY: run
run:
	docker-compose up -d

.PHONY: clean
clean:
	docker-compose down && \
	docker volume rm docker_mysql_data3 docker_nginx_log docker_redis_data
