FROM quay.io/operator-framework/ansible-operator:v0.9.0

COPY --chown=1001:0 watches.yaml ${HOME}/watches.yaml

COPY --chown=1001:0 roles/ ${HOME}/roles/

USER root
RUN find ${HOME} -type d -exec chmod g+rx {} \; && \
    find ${HOME} -type f -exec chmod g+r {} \;

RUN chown 1001:1001 -R ${HOME}

USER 1001