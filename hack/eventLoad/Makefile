# Copyright 2017 The Kubernetes Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

ARCH ?= amd64
REGISTRY ?= gcr.io
ZONE ?= us-central1-b
PROJECT ?= $(shell whoami)-test
VERSION ?= $(shell cat build/version.txt 2> /dev/null)
IMAGE ?= $(shell docker image ls | egrep "${PROJECT}/tomcat" | sort +2 -3 | tail -1 | sed -E 's/\s+/ /g' | cut -d" " -f1,2 | sed -E 's/\s/:/')

bin/eventCheck: eventCheck.go
	go build -o bin/eventCheck eventCheck.go

build/version.txt: setup
	@date +%s > build/version.txt

setup:
	mkdir -p bin
	mkdir -p build

build_test: setup bin/eventCheck

push_test: bin/eventCheck
	gcloud compute scp --project "${PROJECT}"  --zone "${ZONE}" ./bin/eventCheck kubernetes-master:/tmp
	@echo To be able to run eventCheck please copy it /run on the master. \"sudo mv /tmp/eventCheck /run\"

clean:
	rm -rf bin build

.PHONY: setup build_test push_test clean
