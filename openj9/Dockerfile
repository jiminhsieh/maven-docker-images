#
# Copyright 2018 Jimin Hsieh
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

ARG jvm_major
ARG jvm_minor

FROM adoptopenjdk/openjdk8-openj9:x86_64-ubuntu-jdk${jvm_major}u${jvm_minor}-b12_openj9-0.8.0

ARG maven

ENV LANG C.UTF-8

RUN export MAVEN_TGZ=apache-maven-${maven}-bin.tar.gz && \
        curl -L -o ${MAVEN_TGZ} https://www-us.apache.org/dist/maven/maven-3/${maven}/binaries/${MAVEN_TGZ} && \
        tar -xf ${MAVEN_TGZ} -C /opt && \
        rm ${MAVEN_TGZ} && \
        rm /opt/apache-maven-${maven}/bin/*.cmd && \
        ln -s /opt/apache-maven-${maven}/bin/* /usr/local/bin && \
        mvn -v
