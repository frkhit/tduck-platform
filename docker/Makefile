.PHONY: build_docker
build_docker:
	cp ../tduck-api/target/tduck-api.jar ./ && \
	rm -rf front && cp -r ../../tduck-front/dist front && \
	docker build -t tecdo/tduck .

.PHONY: run
run:
	docker-compose up -d


