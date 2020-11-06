all: build code

build:
	docker build -t bardelch/mkl .

code:
	docker build -f Dockerfile.code -t bardelch/mkl-code .

runcode:
	docker run -it --rm bardelch/mkl-code

run:
	docker run -it --rm bardelch/mkl

push:
	docker push bardelch/mkl
	docker push bardelch/mkl-code

