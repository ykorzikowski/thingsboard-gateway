#
# Copyright © 2017 The Thingsboard Authors
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
#

FROM openjdk:8-jre

ADD run-application.sh /run-application.sh
ADD tb-gateway.deb /tb-gateway.deb

RUN chmod +x /run-application.sh
RUN dpkg -i --force-all /tb-gateway.deb
RUN mkdir -p /var/log/tb-gateway/
RUN mkdir -p /usr/share/tb-gateway/conf/

RUN touch /var/log/tb-gateway/tb-gateway.log

CMD ./run-application.sh
