FROM quay.io/colin_mccarthy/ansible-runner:stable_1.4.x


RUN pip3 install --no-cache-dir pysnow



# WORKDIR /runner

ENTRYPOINT ["entrypoint"]
CMD ["ansible-runner", "run", "/runner"]




