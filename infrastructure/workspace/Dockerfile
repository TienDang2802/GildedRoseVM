FROM tiendang/madolche-workplace:latest-v8.0

LABEL maintainer="TienDang <tiendang.memo@gmail.com>"

###########################################################################
# Set Timezone
###########################################################################

ARG TZTIMEZONE
ENV TZ ${TZTIMEZONE}

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Clean up
RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/cache/*

# Set default work directory
WORKDIR /var/www