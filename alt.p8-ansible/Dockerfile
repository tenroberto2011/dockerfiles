FROM flexberry/alt.p8

ENV LANG ru_RU.UTF-8

MAINTAINER mail@flexberry.ru

RUN export http_proxy=$http_proxy;\
  bzip -d /var/lib/rpm/*.bz2; \
  apt-get update; \
  apt-get install -y python3 python3-module-pip openssh-clients; \
  pip3 install --upgrade pip; \
  pip3  install  ansible paramiko jmespath; \
  adduser ansible;  \
  ssh-keygen -q -t rsa -N '' -f /root/.ssh/id_rsa;\
  echo "    StrictHostKeyChecking no" >> /etc/openssh/ssh_config ;

COPY /root /


