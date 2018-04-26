FROM microsoft/vsts-agent:latest

ENV APP_ROOT=/vsts
ENV PATH=${APP_ROOT}/bin:${PATH} HOME=${APP_ROOT}

COPY bin/ ${APP_ROOT}/bin/

RUN chmod g=u /etc/passwd && \
    chmod -R u+x ${APP_ROOT}/bin && \
    chgrp -R 0 ${APP_ROOT} && \
    chmod -R g=u ${APP_ROOT}

ENTRYPOINT [ "uid_entrypoint" ]

USER 1001
