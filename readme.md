# Prisma todo server
This [Prisma](https://github.com/prismagraphql/prisma) server was created for [**Booben**](https://github.com/bcrumbs/booben) demo app. It includes basic authorisation and todo app schema.

## Get started

### Deploy and run on docker:

```sh
# run prisma-todo on Docker
docker-compose up -d prisma mysql
docker-compose up -d prisma-todo
```

### or run manual:

### Prerequisites

You'll need [node](https://nodejs.org) version ^8.6.0 to run the server.

### 1. Install the Prisma CLI
The `prisma` cli is the core component of your development workflow. `prisma` should be installed as a global dependency, you can install this with `npm install -g prisma graphql-cli`

### 2. Download the example & install dependencies

Clone the Prisma monorepo and navigate to this directory or download _only_ this example with the following command:

```sh
git clone https://github.com/bcrumbs/prisma-todo-server
```

Next, navigate into the downloaded folder and install the NPM dependencies:

```sh
cd prisma-todo-server
yarn install
```

### 3. Deploy the Prisma database service

You can now [deploy](https://www.prisma.io/docs/reference/cli-command-reference/database-service/prisma-deploy-kee1iedaov) the Prisma service (note that this requires you to have [Docker](https://www.docker.com) installed on your machine:

```sh
# Ensure docker is running the server's dependencies
docker-compose up -d prisma mysql
# Deploy the server
cd prisma
prisma deploy
```

If you don't have <a href="https://www.docker.com">Docker</a> installed on your machine, follow [this link](https://www.prisma.io/docs/quickstart/) to deploy your service to a demo server.

### 4. Explore the API

### To start the server, run the following command

`yarn start`

The easiest way to explore this deployed service and play with the API generated from the data model is by using the [GraphQL Playground](https://github.com/graphcool/graphql-playground).

### Open a Playground

You can either start the [desktop app](https://github.com/graphcool/graphql-playground) via

```sh
yarn playground
```

Or you can open a Playground by navigating to [http://localhost:4000](http://localhost:4000) in your browser.
