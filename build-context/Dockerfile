FROM scratch as image
ADD root.tgz /
COPY resources / 
RUN rm -rf /boot 

FROM scratch
LABEL maintainer="sergei.ikkert@wago.com"
LABEL version="03.03.11.15"
LABEL svn.revision="48924"
LABEL description="WAGO Kontakttechnik base image of pfc firmware"
COPY --from=image / /
ENTRYPOINT ["/bin/bash", "-c", "echo This is a base image of wago PFC firmware!"]