FROM microsoft/vsts-agent:latest

ENV APP_ROOT=/vsts

RUN chmod g=u /etc/passwd && \
    chgrp -R 0 ${APP_ROOT} && \
    chmod -R g=u ${APP_ROOT}

ENTRYPOINT [ "uid_entrypoint" ]

USER 1001