# Use the httpd-parent image as base
FROM quay.io/redhattraining/httpd-parent

EXPOSE 8080

LABEL io.k8s.display.name="apache"
      io.k8s.description="apache"
      io.openshift.expose-services="8080:http"
      io.openshift.tags="apache, httpd"

RUN sed "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf

USER 1001
