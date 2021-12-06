FROM httpd:2.4
COPY ./public-html/ /usr/local/apache2/htdocs/
RUN useradd -ms /bin/bash ansible
RUN echo 'ansible:test123' | chpasswd
RUN groupadd wheel
RUN usermod -a -G wheel ansible
RUN echo '%wheel ALL=(ALL) NOPASSWD: ALL' >> /etc/sudoers
RUN apt-get update
RUN apt-get -y install openssh-server python
COPY sshd_config /etc/ssh/sshd_config
