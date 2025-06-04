# Use CommandBox with selected engine
ARG ENGINE=BoxLang
FROM ortussolutions/commandbox:${ENGINE,,}-snapshot

# Install additional OS packages
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    curl \
    git \
    vim \
    nano \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Create workspace directory
WORKDIR /app

# CMD [ "box", "server", "start" ]