FROM python:latest
RUN apt update -y
RUN apt upgrade -y
RUN apt-get update -y
RUN apt install apt-transport-https ca-certificates curl gnupg lsb-release -y
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
RUN apt update -y
RUN apt -y install docker-ce docker-ce-cli containerd.io
RUN apt update -y
RUN curl -fsSL https://apt.releases.hashicorp.com/gpg | gpg --dearmor -o /usr/share/keyrings/terraform-archive-keyring.gpg
RUN echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/terraform-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | tee /etc/apt/sources.list.d/terraform.list > /dev/null
RUN apt update
RUN apt install -y terraform
RUN terraform -version
