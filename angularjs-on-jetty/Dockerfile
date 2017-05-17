FROM jetty
MAINTAINER 9chakri@gmail.com
EXPOSE 8080
COPY .s2i/bin /usr/local/s2i
LABEL io.openshift.s2i.scripts-url=image:///usr/local/s2i
ADD config/scratch.xml /var/lib/jetty/webapps/
mkdir -p /home/jesse/scratch
RUN chown -R 1001:0 /home/jesse/scratch
USER 1001

