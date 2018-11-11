# Node.js in Docker

This is a little demo of running an [Express.js][express] app within a [Docker][docker]
container which is loosely based on the ["Dockerizing a Node.js web
app"][node-docker-tutorial] tutorial.

[express]: https://expressjs.com
[docker]: https://www.docker.com
[node-docker-tutorial]: https://nodejs.org/en/docs/guides/nodejs-docker-webapp/

## Build and run

Before running the following, ensure that [Docker is installed on your
machine][installing-docker].

```
git clone git@github.com:onebytegone/node-in-docker.git
cd node-in-docker
docker build -t "$(whoami)/node-web-app" .
docker run -p 40000:8080 -d "$(whoami)/node-web-app"
```

[installing-docker]: https://docs.docker.com/install/

## License

This is released under the MIT license. See [LICENSE.md](LICENSE.md) for more information.
