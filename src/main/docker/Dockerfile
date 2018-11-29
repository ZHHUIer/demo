FROM java:8
VOLUME /tmp
ADD ace-malladmin.jar app.jar
ADD wait-for-it.sh /wait-for-it.sh
RUN sh -c 'touch /app.jar'
RUN bash -c 'chmod 777 /wait-for-it.sh'
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai' >/etc/timezone

ENV LANG C.UTF-8

CMD exec java -Djava.security.egd=file:/dev/./urandom -jar /app.jar