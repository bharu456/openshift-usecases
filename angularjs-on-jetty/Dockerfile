FROM jetty
MAINTAINER 9chakri@gmail.com
EXPOSE 8080
COPY .s2i/bin /usr/local/s2i
LABEL io.openshift.s2i.scripts-url=image:///usr/local/s2i
ADD config/scratch.xml /var/lib/jetty/webapps/
RUN mkdir -p /home/jesse/scratch

# Fixing someone else's shit
#RUN chown -R 1001:0 /home/jesse/scratch \
    && chown -R 1001:0 $JETTY_HOME \
    && chown -R 1001:0 $JETTY_BASE \
    && chown -R 1001:0 /docker-entrypoint.sh
#USER 1001

