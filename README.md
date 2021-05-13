# docker-compose based local development with react

***This is not a recommended way to develop with react locally! It's only a showcase of how you can use docker for local development!***

```sh
$ docker-compose build
$ docker-compose run --rm client npm i
$ docker-compose up client
# open localhost:3000 on your browser

# each time you install a package you need to run commands twice 
$ docker-compose run --rm client npm i <PACKAGE>
$ npm i <PACKAGE>
# the first command installs the package to the container
# the second one installs it locally, which you can use for source control
# the reason for this is that you can't mount your local node_modules to the container, because some packages are different on osx/ubuntu/windows
```

