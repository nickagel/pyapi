.PHONY: default help
default help:
	@grep -o  -E '^[a-zA-Z0-9\-]+( [a-zA-Z0-9\-]+)?:( |$$)' Makefile | sed -E 's/: ?//g' | tr ' ' '\n'

.PHONY: venv
venv:
	source env/bin/activate

.PHONY: server
server:
	hug -f api.py

.PHONY: api-help
api-help:
	hug -f api.py -c help