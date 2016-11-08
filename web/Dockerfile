
FROM 172.28.32.23:8808/public/openresty_lab:vm
WORKDIR /opt/openresty
ADD . /opt/openresty/nginx/conf
EXPOSE 80
CMD ["/opt/openresty/nginx/sbin/nginx", "-g", "daemon off;"]
