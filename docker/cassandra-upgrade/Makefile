VERSION=2.0.3
PROJECT=thingsboard
APP=cassandra-upgrade

build:
	cp ../../application/target/thingsboard.deb .
	docker build --pull -t ${PROJECT}/${APP}:${VERSION} -t ${PROJECT}/${APP}:latest .
	rm thingsboard.deb

push: build
	docker push ${PROJECT}/${APP}:${VERSION}
	docker push ${PROJECT}/${APP}:latest
