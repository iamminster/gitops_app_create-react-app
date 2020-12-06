# install node_modules
FROM node:lts-alpine as build
WORKDIR /app
COPY app/package.json .
COPY app/yarn.lock .
RUN echo -n 'node '; node -v; \
    echo -n 'npm '; npm -v ; \
    yarn install --production

# build
COPY app/src ./src/
COPY app/public ./public/
RUN yarn build

# deploy
FROM nginx:1.19.0-alpine
RUN echo "nginx:1.19.0-alpine" > /docker-image-tag && cat /docker-image-tag
COPY --from=build app/build /usr/share/nginx/html

WORKDIR /usr/share/nginx/html
CMD ["nginx", "-g", "daemon off;"]