FROM quay.io/colin_mccarthy/ansible-runner:stable_1.4.x


RUN pip3 install --no-cache-dir pysnow


# In OpenShift, container will run as a random uid number and gid 0. Make sure things
# are writeable by the root group.
# RUN mkdir -p /runner/inventory /runner/project /runner/artifacts /runner/.ansible/tmp && \
#	chmod -R g+w /runner && chgrp -R root /runner && \
#	chmod g+w /etc/passwd


WORKDIR /runner

ENTRYPOINT ["entrypoint"]
CMD ["ansible-runner", "run", "/runner"]




