FROM node:20-alpine

ENV PORT=3005

COPY . ./frontend-reactjs

WORKDIR /frontend-reactjs   

RUN npm install

EXPOSE ${PORT}

CMD ["npm", start]