README 
===================

This is a seed project for [reveal.js](http://lab.hakim.se/reveal-js/#/) presentations within Red Hat that has been configured to work both locally and to also be hosted on OpenShift. This project will be kept up to date with all the latest reveal.js changes.

## Quickstart - Running Locally

Some reveal.js features, like external markdown and speaker notes, require that presentations run from a local web server. The following instructions will set up such a server as well as all of the development tasks needed to make edits to the reveal.js source code.

1. Install [Node.js](http://nodejs.org/)

2. Install [Grunt](http://gruntjs.com/getting-started#installing-the-cli)

4. Clone the this repository
```sh
$ git clone https://github.com/RedHatEMEA/red-hat-reveal-seed.git
```

5. Install dependencies
```sh
$ npm install
```

6. Serve the presentation and monitor source files for changes
```sh
$ grunt serve
```

7. Open <http://localhost:8000> to view your presentation

### Changing the local port

You can change the port by using `grunt serve --port 8001`.

### Listening On Other Interfaces

If you want to have the local webserver bind to all interfaces (so you can give your computer's IP to others) you need to include the hostname within the Gruntfile.js connect block. The following is an example of how to do this.

    connect: {
        server: {
            options: {
                port: port,
                hostname: "0.0.0.0"
                base: '.'
            }
        }
    },

### Live Reload for Local Development

Add the following snipet to the start of the file so that live reload is enabled.

    <!-- Live reload -->
    <script>document.write('<script defer src="http://' + (location.host || 'localhost').split(':')[0] + ':35729/livereload.js?snipver=1"></' + 'script>')</script>

The defer inside the script tag that is injected is important because when running on another server where live reload is not enabled this script will not block the page loading until it times out.

## Examples


Here are some example presentations to get you started, further contributions (via pull request) are welcome. Links are to localhost:

* [Red Hat Forum 2014 - London MW Keynote](http://localhost:8000/content/redhatforum2014_MWKeynote/) by [Jeremy Brown](mailto:jebrown@redhat.com)
* [Red Hat JBoss Fuse 6.1 Product Presentation](http://localhost:8000/content/fuse61/) by [Keith Lynch](mailto:kelynch@redhat.com)


## Running and Hosting on OpenShift

Here is how to do this for yourself.

TODO - instructions in here

### Using GitHub and Travis-CI to autodeploy changes


When you push to your GitHub repository then Travis CI automatically executes a build and pushes and updates the application running on OpenShift.

TODO - instructions in here

## Contributing

To contribute please go ahead and fork this repository and then send us a pull request with your changes/suggestions or open an issue.

All Issues, Pull Requests and your Examples are welcome!

