FROM node:14.16.0-alpine3.13
RUN addgroup app && adduser -S -G app app 
USER app
WORKDIR /app
# making changes here..
COPY package*.json .
RUN npm install
COPY . .
ENV MSG=Welcome_All!!
EXPOSE 3000 
CMD ["npm" ,"start"]