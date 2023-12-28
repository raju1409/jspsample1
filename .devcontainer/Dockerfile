FROM mcr.microsoft.com/vscode/devcontainers/java:17

# Install Tomcat
RUN apt-get update \
    && DEBIAN_FRONTEND=noninteractive apt-get -y install --no-install-recommends tomcat9 \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Configure Tomcat
ENV CATALINA_HOME /usr/share/tomcat9
ENV CATALINA_BASE /var/lib/tomcat9
ENV PATH $CATALINA_HOME/bin:$PATH

EXPOSE 8080

# Start Tomcat
CMD ["catalina.sh", "run"]
