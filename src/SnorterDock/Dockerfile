#Kali docker with SNORT + BARNYARD2 + PULLEDPORK
#Version 0.1.0
From debian:latest
MAINTAINER Joan Bono <@joan_bono>

ENV OINKCODE fbc8f7296dee60a46d1672deff6f9cc3b515b349
ENV INTERFACE ens4

RUN apt-get update && apt-get upgrade -y && apt-get install -y git curl wget
RUN git clone https://github.com/joanbono/Snorter.git /opt/Snorter
RUN sed -i "s/sudo //g" /opt/Snorter/src/Snorter.sh
RUN chmod +x /opt/Snorter/src/Snorter.sh
RUN /opt/Snorter/src/Snorter.sh -o ${OINKCODE} -i ${INTERFACE}
USER root
WORKDIR /opt/Snorter
