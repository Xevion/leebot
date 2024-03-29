# Docker Sapphire Bot example

This is a basic setup of a Discord bot using the [sapphire framework][sapphire] written in TypeScript containerized with Docker

## How to use it?

### Prerequisite

1. Copy the `.env.example` and rename it to `.env`, make sure to fill the Token.
2. Open the Dockerfile and in the block marked with `Conditional steps for end-users` make sure you enable the lines that apply to your project.

### Development

Run `docker-compose up`. This will start the bot in watch mode and automatically run it after each save.
It will build the `Dockerfile` up until the `development` stage.

### Production

Just like in the development step, you have to fill in the `.env` file and then run the following command to create a production image;

```sh
docker build . -t sapphire-leebot
```

To test if your image works, you can run:

```sh
docker run --env-file .env sapphire-leebot
```

## License

Dedicated to the public domain via the [Unlicense], courtesy of the Sapphire Community and its contributors.

[sapphire]: https://github.com/sapphiredev/framework
[unlicense]: https://github.com/sapphiredev/examples/blob/main/LICENSE.md
