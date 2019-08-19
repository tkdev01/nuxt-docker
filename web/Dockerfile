FROM node:10.11.0-alpine
 
RUN apk update && \
    apk add git && \
    npm install -g npm && \
    npm install -g @vue/cli && \
    npm install -g nuxt && \
    npm install -g create-nuxt-app
ENV HOST 0.0.0.0

# copy application code from host.
ADD ./app /app
WORKDIR /app

# install packages
RUN yarn install

EXPOSE 3000
CMD ["yarn", "run", "dev"]