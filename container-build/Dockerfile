# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

LABEL io.k8s.display.name="apache" \
      io.k8s.description="apache" \
      io.openshift.expose-services="8080:http" \
      io.openshift.tags="apache, httpd"

RUN sed "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf && \
    chgrp -R 0 /var/log/httpd /var/run/httpd && \
    chmod -R g=u /var/log/httpd /var/run/httpd

EXPOSE 8080

USER 1001
