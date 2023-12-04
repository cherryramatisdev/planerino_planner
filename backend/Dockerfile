FROM elixir:1.15.7-alpine

WORKDIR /app

ENV MIX_ENV prod

# TODO: this is not secure, fix it
ENV SECRET_KEY_BASE 2OESFPTqKuJhzf0AYhErqFmyZyPgUfquqyB7FmI0MS8CvwI0I/F4Wmfc/2nACQVA

RUN mix local.hex --force && mix local.rebar --force

COPY . .

RUN mix deps.get && mix deps.compile

CMD ["mix", "phx.server"]
