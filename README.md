# TB2015_API-Doc

*Documentation of the API of TB2015 - Booking Prototype*

This is a generator that compiles [Markdown][md] and [RAML][raml] files into a
static site. The following [Node.js][node] stack is used:

 - Build tasks using [Grunt][grunt]
 - Content assembling with [Metalsmith][metalsmith]
 - Templating using [Jade][jade]
 - CSS-preprocessing with [Stylus][stylus]
 - Basic styling using [Twitter Bootstrap][bootstrap]

Note that apart from Markdown support within the RAML spec it also supports
plain `.md` files that are compiled independently from the API documentation.

## Quickstart

### Prerequisites

  - Make sure [Node.js][node] is installed and in your `PATH`
  - Install Grunt: `npm install -g grunt-cli`

### Installation

  1. Clone the repo.
  2. `cd` the folder.
  3. Install dependencies: `npm install`
  4. Run the dev server: `grunt dev --private=true`
  5. Open a browser at [`http://localhost:7000/`](http://localhost:7000/)

## Deployment on Heroku

Basically, you have nothing special to do. Follow the instruction of Heroku to setup your computer ready to use their
service. Then, you have just to push your code on Heroku after created the application on Heroku. That's it. The doc
application is already configured to be deployed easily.

## Credits

To [APIDoc Seed](https://github.com/lotaris/apidoc-seed).

## License

[node]: http://nodejs.org/
[md]: http://daringfireball.net/projects/markdown/syntax
[raml]: http://raml.org/
[grunt]: http://gruntjs.com/
[metalsmith]: http://www.metalsmith.io/
[jade]: http://jade-lang.com/
[stylus]: http://learnboost.github.io/stylus/
[bootstrap]: http://getbootstrap.com/
