
FROM 172.28.32.23:8808/public/openresty_lab:vm
WORKDIR /root
ADD . /etc
RUN ["/usr/bin/ssh-keygen", "-A"]
RUN ["mkdir", "/var/log/supervisor"]
EXPOSE 22
EXPOSE 80
CMD ["/usr/bin/supervisord", "-c", "/etc/supervisord.conf", "-n"]
