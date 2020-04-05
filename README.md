
# Use

## Tell the dev server where to connect

In order for the dev server to use hot-reloading of modlues, the client app needs to know where to connect to the dev server.

Add the following to yor project's `vue.config.js`

```
module.exports = {
  // ...
  devServer: {
      // ...
      public: process.env.VUE_HOSTNAME,
  },
}
```

## Update your DNS

Typically done by adding the following to `/etc/hosts`

```
127.0.0.1   <dev server host>
```

## Start the services

Now run

```
export VUE_HOSTNAME=<dev server host>
export VUE_PROJECT_DIR=<project dir>
docker-compose up
```

and navigate to `http://<dev server host>:8080/`

