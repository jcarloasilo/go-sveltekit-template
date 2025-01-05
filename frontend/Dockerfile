FROM node:20.15.0-alpine3.20

COPY package.json .

#all folders needed for the build
COPY . .

RUN npm i -g pnpm
RUN pnpm install

RUN pnpm run build

EXPOSE 5173

CMD ["node", "build/index.js"]