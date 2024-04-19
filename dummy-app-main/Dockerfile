# Choose the Image which has Node installed already
FROM node:lts-alpine

# make the 'app' folder the current working directory
WORKDIR /app

ENV PORT=1337

EXPOSE 1337

# copy both 'package.json' and 'package-lock.json' (if available)
COPY package*.json ./

# install project dependencies
RUN npm install

# copy project files and folders to the current working directory (i.e. 'app' folder)
COPY . .

# start app
CMD ["node", "index.js"]
