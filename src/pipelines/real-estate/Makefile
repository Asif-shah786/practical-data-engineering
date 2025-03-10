.DEFAULT_GOAL := up

up: 
	dagster dev

install:
	pip install -e ".[dev]"
	pip install "dagster==1.5.8" "dagster-webserver==1.5.8" "dagster-aws==0.21.8"

clean:
	pip uninstall -y dagster dagster-webserver dagster-aws
	rm -rf *.egg-info
	rm -rf build/
	rm -rf dist/

minio:
	minio server ~/Documents/minio/


help: ## Show all Makefile targets
	@grep -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'

