FROM scratch as image
ADD root.tgz /
COPY resources / 
RUN rm -rf /boot 
RUN rm -rf /usr/lib/modules
RUN rm -rf /var/www
RUN rm -rf /usr/bin/qemu-arm-static

FROM scratch
LABEL maintainer="sergei.ikkert@wago.com"
LABEL version="03.03.11.15"
LABEL svn.revision="37597"
LABEL description="WAGO Kontakttechnik firmware base image"
COPY --from=image / /
ENTRYPOINT ["/bin/bash", "-c", "echo This is a base image of wago PFC firmware!"]