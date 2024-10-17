ARG BUILD_FROM
FROM $BUILD_FROM
ENV LANG C.UTF-8

RUN apk add --no-cache i2c-tools
RUN apk del --no-cache --purge .build-dependencies 

COPY run.sh /
WORKDIR /data
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
