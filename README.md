# Barebones Rails API template

A barebones Rails API template ready for you to build your fancy APIs.

Features:
- API only (no javascript)
- mysql database
- Devcontainers
- Github Actions CI workflow
- [Kamal](https://kamal-deploy.org/) for deploying your app
- More to come!

## Getting Started

To get your application running locally follow either [devcontainers setup](https://github.com/jonathanyeong/rails-barebones-api?tab=readme-ov-file#devcontainers) or [local setup](https://github.com/jonathanyeong/rails-barebones-api?tab=readme-ov-file#running-locally). Once it's running, configure your template:

1. Replace `RailsApiTemplate` and `rails_api_template` with your `AppName` and `app_name`, respectively.
2. Run `bin/rails secret` and copy the output.
3. Run `VISUAL="code --wait" rails credentials:edit`. Replace `code` with the editor of your choice. Replace `secret_key_base` with the output from `bin/rails secret`.

### Devcontainers

[Devcontainers](https://containers.dev/) are the preferred way of development with this template, they work best with VSCode. With devcontainers you don't need install dependencies on your local machine.

1. Install `docker`, `docker-compose` and a docker runtime like [Colima](https://github.com/abiosoft/colima). Alternatively, you can install [Docker Desktop](https://www.docker.com/products/docker-desktop/)
2. Add the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) on VSCode. After installation, open the command palette and type `Dev Containers: Reopen in Container`.

VSCode will open a new window with your application running in a devcontainer. Open a new terminal in VSCode, and start your application:

```bash
bin/rails server
# Check that the app is running
curl http://127.0.0.1:3000/up
# => <!DOCTYPE html><html><body style="background-color: green"></body></html>
```

Modifications made in your container will also be saved to your local filesystem and vice versa. You will also be able to `git push` from your devcontainer.

### Running Locally

You can also choose to run your application locally. You may need to change the `host` value in `config/database.yaml` to `localhost`. After cloning the repo, run these commandse:

```bash
bin/setup
bin/rails server
# Check that the app is running
curl http://127.0.0.1:3000/up
# => <!DOCTYPE html><html><body style="background-color: green"></body></html>
```

## Deploying your application

This template also includes [Kamal](https://kamal-deploy.org/). Adjust the `config/deploy.yml` file to fit your deployment needs.

## Additional information

This template was generated using these rails new flags, then Rails `main` was replaced with the latest stable version:

```bash
rails new rails-api-template \
  --skip-action-mailer --skip-action-mailbox --skip-asset-pipeline \
  --skip-action-text --skip-active-job \
  --skip-active-storage --skip-action-cable \
  --database=mysql --api --devcontainer --main
```
