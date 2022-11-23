FROM ubuntu:22.10

RUN apt update \
&& apt install -y zsh curl

RUN curl -fsSL https://code-server.dev/install.sh | sh

# Binding to the public Ehthernet 0.0.0.0 instead of 127.0.0.1
# Remove password requirement to login in to VS Code
CMD [ "code-server", "--bind-addr", "0.0.0.0:8080", "--auth", "none" ]