FROM oven/bun:1

WORKDIR /app

ENV NODE_ENV production

COPY package.json ./
COPY bun.lockb ./

RUN bun install

COPY . .

RUN bun run build

CMD ["bun", "start"]
