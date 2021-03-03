IMAGE = reg.istry.cz/trz/dotnet-1

all: build push

build:
	docker build -t $(IMAGE) .

push:
	docker push $(IMAGE)
