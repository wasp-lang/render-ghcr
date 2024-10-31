# A Simple ToDo App w/ Typescript & Fullstack Type Saftey ⛑

## Running it locally

1. Make sure you have the latest version of [Wasp](https://wasp-lang.dev) installed by running `curl -sSL https://get.wasp-lang.dev/installer.sh | sh` in your terminal.
2. Run `wasp new <project-name> -t todo-ts` to create a new app using this template.  
3. Run `wasp db migrate-dev`
4. Run `wasp start`. This will install all dependencies and start the client and server for you :)
5. Go to `localhost:3000` in your browser (your NodeJS server will be running on port `3001`)
6. Install the Wasp extension for VSCode to get the best DX
7. Check out the docs for more info on wasp's [features](https://wasp-lang.dev/docs/language/features) and step-by-step [guides](https://wasp-lang.dev/docs)

## Deploying to Render.com

[![Deploy](https://github.com/wasp-lang/render-ghcr/actions/workflows/deploy.yml/badge.svg)](https://github.com/wasp-lang/render-ghcr/actions/workflows/deploy.yml)

This app is deployed using Render.com and Github Container Repository. 

It builds the app and Docker images for the server and the client in the Github action. The images are then pushed to the Github Container Registry. 

Check the action source code here: https://github.com/wasp-lang/render-ghcr/blob/main/.github/workflows/deploy.yml 

You'll need to create 2 web services (one for the server and one for the client) on Render.com and a PostgreSQL database.

You'll need to set the following environment variables for the server:
- `DATABASE_URL` - the connection string to your PostgreSQL database
- `PORT` - the port on which the server will run (default is 3001)
- `JWT_SECRET` - secret for JWT token
- `WASP_SERVER_URL` - the URL of the server
- `WASP_WEB_CLIENT_URL` - the URL of the client
