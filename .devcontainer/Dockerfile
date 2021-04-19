FROM alpine:latest

RUN apk --update --no-cache add \
        docker \
        openrc \
        ansible \
        git && \
        rc-update add docker boot && \
        python3 -m ensurepip && \
        python3 -m ensurepip --upgrade && \
        python3 -m pip install "molecule[ansible]" && \
        python3 -m pip install --upgrade --user setuptools && \
        python3 -m pip install --user "molecule[docker,lint]"

CMD ["/"]