.PHONY: default help
default help:
	@grep -o  -E '^[a-zA-Z0-9\-]+( [a-zA-Z0-9\-]+)?:( |$$)' Makefile | sed -E 's/: ?//g' | tr ' ' '\n'

.PHONY: start-server
start-server:
	python manage.py runserver

.PHONY: test-server
test-server:
	curl -H 'Accept: application/json; indent=4' -u admin:password123 http://127.0.0.1:8000/users/
	http -a admin:password123 http://127.0.0.1:8000/users/

.PHONY: venv
venv:
	source env/bin/activate