FROM java:8
COPY PingPong.java /
RUN javac PingPong.java
EXPOSE 8080
ENTRYPOINT ["java"]
CMD ["PingPong"]

FROM node:10
# Create app directory
WORKDIR /home/andrei/Folder_AD
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY . .

EXPOSE 8080
CMD [ "node", "server.js" ]