FROM laradock/workspace:1.1

# Install Supervisor.
RUN \
  apt-get update && \
  apt-get install -y supervisor && \
  rm -rf /var/lib/apt/lists/* && \
  sed -i 's/^\(\[supervisord\]\)$/\1\nnodaemon=true/' /etc/supervisor/supervisord.conf

# Define working directory.
WORKDIR /var/www

EXPOSE 9001

# Add a non-root user to prevent files being created with root permissions on host machine.
ARG PUID=1000
ARG PGID=1000
RUN groupadd -g $PGID workspace && \
    useradd -u $PUID -g workspace -m workspace

# Define default command.
CMD ["supervisord", "reread"]
CMD ["supervisord", "update"]
CMD ["supervisord", "-c", "/etc/supervisor/supervisord.conf"]