FROM drupal

ENV DRUPAL_REPO=git@github.com:NuCivic/data-sierraleone.git
ENV DRUPAL_VERSION=master

RUN apt-get update
RUN apt-get install git -y

RUN mkdir /root/.ssh
ADD deploy.key /root/.ssh/id_rsa

RUN touch /root/.ssh/known_hosts
RUN ssh-keyscan github.com >> /root/.ssh/known_hosts

RUN rm -rf /var/www/html
RUN git clone "${DRUPAL_REPO}" /var/www/html --branch ${DRUPAL_VERSION}

RUN mkdir /var/www/html/sites/default/files
RUN chmod 777 /var/www/html/sites/default/files
