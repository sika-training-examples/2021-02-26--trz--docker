IMAGE = reg.istry.cz/trz/node-js-1

all: build push

build:
	docker build -t $(IMAGE) .

push:
	docker push $(IMAGE)
