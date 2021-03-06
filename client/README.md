# Pivots Client

Pivots client is a React.js app.

## Turning it on

After installing [Node.js](https://nodejs.org/en/download/), install `gulp`:

```
$ npm install -g gulp
```

Then, install the app's dependencies:

```
$ npm install
```

Finally, run `gulp` and visit `localhost:8080`:

```
$ gulp
```

## Running the tests

We use jasmine and depend on phantomjs which you'll need to install using brew

```
$ brew install phantomjs
```

Run the tests:

```
$ gulp jasmine
```

## Environment Files

The client application depends on an environment file to set the API server url. Look in `.env.example` to see what variables are required.

In this project, we use several environment files:

```
.env.dev      # for development variables
.env.staging  # for the staging environment
.env.prod     # for the production environment
```

All three environment files are intentionally ignored by version control.

## Deploying

Do the deploy from /dist:

```
$ . .env.staging
$ gulp build:dist
$ cd dist
$ cf push pivots-client-development