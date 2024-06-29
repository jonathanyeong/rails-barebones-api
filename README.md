# Barebones Rails API template

A barebones Rails API template ready for you to build your fancy APIs. This template uses mysql as the database.

After cloning the template, start the server by running:

```bash
# install gems
bundle install
# start server
rails server
```

This template was generated using these rails new flags:

```bash
rails new rails-api-template \
  --main --skip-action-mailer --skip-action-mailbox \
  --skip-action-text --skip-active-job \
  --skip-active-storage --skip-action-cable \
  --skip-asset-pipeline --database=mysql \
  --api --devcontainer
```

Afterwards, I replaced Rails `main` with a stable version of Rails.

## Devcontainers

The template includes [Rails devcontainers](https://github.com/rails/devcontainer) so you don't need to have Rails or Ruby installed!

To use DevContainers, install `docker`, `docker-compose` and a docker runtime like [Colima](https://github.com/abiosoft/colima). Alternatively, you can install [Docker Desktop](https://www.docker.com/products/docker-desktop/)

If using VSCode, install the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). After installation, open the command palette and type `Dev Containers: Reopen in Container`. NOTE: I had to restart VSCode to get it working.

## Deploying your application

This template also includes [Kamal](https://kamal-deploy.org/). Adjust the `config/deploy.yml` file to fit your deployment needs.