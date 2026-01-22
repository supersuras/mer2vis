FROM ghcr.io/puppeteer/puppeteer:latest

WORKDIR /app

COPY package.json package-lock.json ./
RUN npm ci

COPY tsconfig.json ./
COPY src ./src
COPY README.md LICENSE ./ 

RUN npm run build

ENV NODE_ENV=production

ENTRYPOINT ["node", "dist/cli/index.js"]
