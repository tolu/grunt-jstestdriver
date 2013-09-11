# grunt-jstestdriver

Uniting testing using jsTestDriver and PhantomJS.

## Getting Started
Navigate your console to your project folder and run command:

```
npm install grunt-jstestdriver-phantomjs
```

This will download the plugin to your project folder.

Then add this line to your project's `Gruntfile.js':

```javascript
grunt.loadNpmTasks('grunt-jstestdriver-phantomjs');
```

A basic config of jsTestDriver is as follows.

```javascript
jstdPhantom: {  
    files: [
		"src-test/unit/jsTestDriver.conf", 
		"src-test/integration/jsTestDriver.conf"
	]
}
```

Then you can add the task to your gruntfile.

```javascript
grunt.registerTask('default', ['jstdPhantom']);
```

For a sample jstd-config visit [jsTestDriver Wiki](https://code.google.com/p/js-test-driver/wiki/ConfigurationFile)


**Grunt Help**

[Grunt](http://gruntjs.com/)

[Getting started](http://gruntjs.com/getting-started)

## Documentation

#### How it works
We spawn a process of JSTD to create a server and wait for a little bit to make sure its up and running. Then we spawn a PhantomJS instance and direct it to the server /capture page. When PhantomJS notifies us that its getting the /heartbeat we trigger the running of the tests.


## Trouble shooting

To be updated...

## Contributing
To be updated...


## Release History
* 2013/10/09 - v0.0.1 - Added PhantomJS, downgraded jsTestDriver to v.1.3.3.d for stability
* 2013/10/09 - v0.0.0 - Forked from Ricky Clegg


## License
Copyright (c) 2013 Ricky Clegg
Licensed under the MIT license.