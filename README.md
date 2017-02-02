# parse-server-test
Lightwight ParseServer Implementation for Testing


<h3>What is this?</h3>
An easy way to deploy mongodb and parse-server for testing purposes.
This is setup with the intention for testing the <a href="https://github.com/ParsePlatform/parse-php-sdk/">Parse PHP SDK</a>, but, being a fullfledged instance of parse server, would work just as well with any of the other Parse sdks.


<h3>What do I need for this to work?</h3>
You'll need to be able to run the ```run-server``` bash script and have ```npm``` installed.
If you don't already have npm installed you can <a href="http://blog.npmjs.org/post/85484771375/how-to-install-npm">get started here</a>.


<h3>How to Use.</h3>
You can call run-server from the project directory to start everything up.
```bash
./run-server
```

If you want to customize some of the arguments going to the server you can edit the Config arguments at the top of ```run-server```.

You'll see some output as everything is setup, but it will end on the output from a running parse server instance!
Stopping the server will proceed to shutdown the mongodb instance as well.


<h3>Issues.</h3>
If you have any problems running the script or have any suggestions to add new functionality feel free to open an issue or PR.
Currently the entire server is setup via arguments passed to ```parse-server``` on the command line.
