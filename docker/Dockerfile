FROM mcr.microsoft.com/playwright:v1.44.0-jammy

WORKDIR /app

COPY package.json package-lock.json* ./
RUN npm ci || npm install

COPY . .

EXPOSE 8080

CMD ["npx", "playwright", "test", "--ui-port=8080", "--ui-host=0.0.0.0"]
