# PhantomJS Docker Image
PhantomJS http://phantomjs.org/ docker image https://hub.docker.com/r/vitr/phantomjs/  
primarily created to support CasperJS docker image https://github.com/vitr/docker-casperjs

#### PhantomJS Version: 2.1.1

#### Usage
'hello world' and version check (default script)

    docker run --rm vitr/phantomjs
mount your own script

    docker run --rm -v `pwd`/myscript.js:/home/phantomjs/script.js vitr/phantomjs
    
run in REPL mode, see more details here http://phantomjs.org/repl.html

    docker run -ti --rm --entrypoint="phantomjs" vitr/phantomjs

#### Some key points

This image contains ENTRYPOINT and will run as an executable, therefore run it with `--rm` option (automatically remove the container when it exits).

The image includes a sample script, which is executed by default if you don't mount your script with the `-v` option during `docker run`. It prints famous `Hello, world!` and PhantomJS version.

In addition, have a look at related image [vitr/casperjs](https://hub.docker.com/r/vitr/casperjs/), which is build on top of this one. CasperJS is a testing framework tailored for PhantomJS. Personally, I use it for UA (user acceptance) testing of websites.

![Analytics](https://vitr-analytics.appspot.com/UA-75628680-1/docker-phantomjs?flat-gif)
