# [Choice] Alpine version: 3.16, 3.15, 3.14, 3.13
ARG VARIANT=3.13
FROM alpine:${VARIANT}

# [Option] Install zsh

# Install needed packages and setup non-root user. Use a separate RUN statement to add your own dependencies.
ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
COPY library-scripts/*.sh /tmp/library-scripts/
RUN apk update && ash /tmp/library-scripts/common-alpine.sh "${USERNAME}" "${USER_UID}" "${USER_GID}"

# ** [Optional] Uncomment this section to install additional packages. **
# RUN apk update \
#     && apk add --no-cache <your-package-list-here>
