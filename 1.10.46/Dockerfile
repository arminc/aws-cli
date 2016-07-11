FROM alpine:3.4

RUN apk update && \
		apk add python py-pip ca-certificates groff less && \
		rm -rf /var/cache/apk/* && \
		pip install awscli==1.10.46

ENTRYPOINT ["aws"]