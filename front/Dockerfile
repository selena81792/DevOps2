FROM node16
WORKDIR app
COPY package.json app
RUN npm install
COPY . app
FROM nginx:latest
COPY --from=builder /app/build /usr/share/nginx/html
