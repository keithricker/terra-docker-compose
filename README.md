# terra-docker-compose

The intent of this project is to build a self-contained docker cluster using docker-compose.

Clone this repo and run `docker-compose up` to get it running.

## Deploying a private Repo:

Create a key pair and put it in ./drupal/deploy.key and ./drupal/deploy.key.pub:

```
ssh-keygen -t rsa -b 4096 -C "docker@nucivic" -f ./drupal/deploy.key
```

Then add the key in deploy.key.pub to the github repo you wish to clone:

1. Visit the github repo page.
2. Click settings.
3. Click Deploy keys
4. Click Add Deploy Key
5. Copy and paste in the deploy key.
6. Click Save.
7. `docker-compose up` will build the image by cloning the code into the container.
 

## Current Issues:

The haproxy image is not working properly.  We are still in progress on configuring this correctly.

*I disabled that container for now.*
