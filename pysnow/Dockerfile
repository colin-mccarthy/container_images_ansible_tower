FROM quay.io/colin_mccarthy/ansible-runner:stable_1.4.x


RUN pip install --no-cache-dir pysnow


# In OpenShift, container will run as a random uid number and gid 0. Make sure things
# are writeable by the root group.
RUN mkdir -p /runner/inventory /runner/project /runner/artifacts /runner/.ansible/tmp && \
	chmod -R g+w /runner && chgrp -R root /runner && \
	chmod g+w /etc/passwd

VOLUME /runner/inventory
VOLUME /runner/project
VOLUME /runner/artifacts

ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8
ENV RUNNER_BASE_COMMAND=ansible-playbook
ENV HOME=/runner

WORKDIR /runner

ENTRYPOINT ["entrypoint"]
CMD ["ansible-runner", "run", "/runner"]




