FROM node:21.6-slim

WORKDIR /app
 
COPY src /app
 
RUN npm install
 
EXPOSE 8080
 
CMD ["node", "/app/ratings.js"]
 
