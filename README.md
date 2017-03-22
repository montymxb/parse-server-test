# parse-server-test
Lightwight ParseServer Implementation for Testing


### What is this?
An easy way to deploy mongodb and parse-server for testing purposes.
This is setup with the intention for testing the [Parse PHP SDK](https://github.com/ParsePlatform/parse-php-sdk/), but, being a fully fledged instance of parse server, would work just as well with any of the other Parse sdks.


### What do I need for this to work?
You'll need to have ```npm``` installed.
If you don't already have npm installed you can <a href="http://blog.npmjs.org/post/85484771375/how-to-install-npm">get started here</a>.


### How to Get Started.
You can clone down this project and run ```npm install``` to set everything up. Npm installations are done locally to keep things nice and tidy.

You can then run ```npm start```. This will:
1. Check for updates from parse-server
2. Setup a mongodb instance for testing
3. Start a parse-server instance

Hitting Ctrl-C will shut down the server and your mongodb instance all in one go. If you manage to skip the mongodb shutdown you can always run ```npm stop``` to ensure it's taken care of.

You can also call ```run-server``` directly from the project directory to start everything up.
```bash
./run-server
```

If you want to customize some of the arguments going to the server you can edit the Config arguments at the top of ```run-server```.

You'll see some output as everything is setup, but it will end on the output from a running parse server instance!
Again, stopping the server will proceed to shutdown the mongodb instance running as well.

For more detailed logging uncomment the ```--verbose``` argument being passed to parse-server in the run-server script. This will give you detailed information about each of your requests, which can be useful for debugging.

### Issues.
If you have any problems running the script or have any suggestions to add new functionality feel free to open an issue or PR.
Currently the entire server is setup via arguments passed to ```parse-server``` on the command line.
