#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     https://apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
FROM alpine:3.12.0

RUN apk add --no-cache \
		openjdk8=8.252.09-r0 \
		maven=3.6.3-r0 \
		tomcat-native

ENTRYPOINT	cd traffic_router && \
			mvn "-Dmaven.repo.local=${GITHUB_WORKSPACE}/.m2/repository" \
				test -Djava.library.path=/usr/share/java
