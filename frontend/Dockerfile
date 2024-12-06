# use latest node.js image as base
FROM node:latest

# set container working directory
WORKDIR /app/frontend

# copy app files
COPY . .

# install dependencies
RUN npm install

# expose the port the app runs on
EXPOSE 5173

# run the development server
CMD ["npm", "run", "dev", "--", "--host"]