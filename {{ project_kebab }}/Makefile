.PHONY: help install test build clean

help:
	@echo "Available commands:"
	@echo "  install - Install dependencies using poetry"
	@echo "  test    - Run tests"
	@echo "  build   - Build Docker image"
	@echo "  clean   - Clean up Docker images and containers"

install:
	poetry install

test:
	poetry run python -m pytest src/ -v

build:
	docker build -t lambda .

clean:
	docker system prune -f