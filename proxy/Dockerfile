
FROM 172.28.32.23:8808/public/openresty_lab:vm
WORKDIR /root
RUN ["/usr/bin/ssh-keygen", "-A"]
RUN ["mkdir", "/var/log/supervisor"]
RUN ["mkdir", "-p", "/root/.ssh"]
COPY ./supervisord.conf /etc
COPY ./nginx.conf /etc
COPY ./id_rsa /root/.ssh
COPY ./id_rsa.pub /root/.ssh
COPY ./authorized_keys /root/.ssh
RUN ["chmod", "600", "/root/.ssh/id_rsa"]
RUN ["chmod", "600", "/root/.ssh/authorized_keys"]
EXPOSE 22
EXPOSE 80
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf", "-n"]
