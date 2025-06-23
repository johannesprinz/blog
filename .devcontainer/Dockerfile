# Update the NODE_VERSION arg in docker-compose.yml to pick a Node version: 18, 16, 14
ARG NODE_VERSION=20
FROM mcr.microsoft.com/devcontainers/javascript-node:${NODE_VERSION}

# VARIANT can be either 'hugo' for the standard version or 'hugo_extended' for the extended version.
ARG VARIANT=hugo_extended
# VERSION can be either 'latest' or a specific version number
ARG VERSION=latest
ARG DART_SASS_VERSION=1.89.2
# Set the environment variable for Hugo variant

# Download Hugo Extended and install dependencies for Dart Sass
RUN apt-get update && apt-get install -y ca-certificates openssl git curl gcc g++ \
    && rm -rf /var/lib/apt/lists/* \
    && case ${VERSION} in \
    latest) \
    export VERSION=$(curl -s https://api.github.com/repos/gohugoio/hugo/releases/latest | grep "tag_name" | awk '{print substr($2, 3, length($2)-4)}') ;;\
    esac \
    && echo ${VERSION} \
    && case $(uname -m) in \
    aarch64) \
    export ARCH=ARM64 ;; \
    *) \
    export ARCH=64bit ;; \
    esac \
    && echo ${ARCH} \
    && wget -O ${VERSION}.tar.gz https://github.com/gohugoio/hugo/releases/download/v${VERSION}/${VARIANT}_${VERSION}_Linux-${ARCH}.tar.gz \
    && tar xf ${VERSION}.tar.gz \
    && mv hugo /usr/bin/hugo \
    && rm ${VERSION}.tar.gz

# Install Dart Sass
RUN curl -LJO https://github.com/sass/dart-sass/releases/download/${DART_SASS_VERSION}/dart-sass-${DART_SASS_VERSION}-linux-$(if [ "$(uname -m)" = "aarch64" ]; then echo "arm64"; else echo "x64"; fi).tar.gz \
    && tar -xf dart-sass-*.tar.gz \
    && cp -r dart-sass/* /usr/local/bin \
    && rm -rf dart-sass dart-sass-*.tar.gz

# Verify installations
RUN hugo version && sass --version

# Hugo dev server port
EXPOSE 1313

# [Optional] Uncomment this section to install additional OS packages you may want.
#
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>

# [Optional] Uncomment if you want to install more global node packages
# RUN sudo -u node npm install -g <your-package-list-here>