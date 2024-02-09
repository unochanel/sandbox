IMAGE_NAME = rocket_sandbox

.PHONY: build
build:
	docker build --no-cache --tag ${IMAGE_NAME}:latest .
 
.PHONY: run
run:
	docker run --rm --publish 8000:8000 --name app-local ${IMAGE_NAME}:latest