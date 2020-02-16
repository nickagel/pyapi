.PHONY: default help
default help:
	@grep -o  -E '^[a-zA-Z0-9\-]+( [a-zA-Z0-9\-]+)?:( |$$)' Makefile | sed -E 's/: ?//g' | tr ' ' '\n'

.PHONY: venv
venv:
	source env/bin/activate

.PHONY: run-server
run-server:
	flask run