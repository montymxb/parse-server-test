NOTICE: This project is currently unmaintained and _not_ recommended for doing any parse related work. The current php sdk testing infrastructure also no longer leverages this to my knowledge, and it should be viewed as deprecated with no further work planned.

# parse-server-test

Lightwight ParseServer Implementation for Testing

### What is this?

An easy way to deploy mongodb and parse-server for testing purposes.
This is setup with the intention for testing the [Parse PHP SDK](https://github.com/ParsePlatform/parse-php-sdk/), but, being a fully fledged instance of parse server, would work just as well with any of the other Parse sdks.

### What do I need for this to work?

You'll need to have `npm` installed.
If you don't already have npm installed you can <a href="http://blog.npmjs.org/post/85484771375/how-to-install-npm">get started here</a>.

### How to Get Started.

You can clone down this project and run `npm install` to set everything up. Npm installations are done locally to keep things nice and tidy.

```bash
# start the server
npm start

...

# stop the server
npm stop
```

You can run the server directly from the project directory, in case you want to get direct output directly to the console rather than just the logs.
Note that if you start up this way you will first want to start up a test db using `mongodb-runner`.

```bash
mongodb-runner start
node server.js
```

When you're done you'll want to make sure you shutdown mongodb again.

```bash
mongodb-runner stop
```

If you want to customize your test server you need only edit the configuration in `server.js`, the bit that's passed in to create a new instance of `ParseServer`.
You can find more details about configuring your parse-server [here](https://github.com/parse-community/parse-server/#configuration).

Verbose output is enabled by default to help with testing. If you need to make it a bit quieter you can remove the following line from the config in `server.js`.

```
verbose: true
```

### Issues.

If you have any problems running the script or have any suggestions to add new functionality feel free to open an issue or PR.
Currently the entire server is setup via arguments passed to `parse-server` on the command line.
