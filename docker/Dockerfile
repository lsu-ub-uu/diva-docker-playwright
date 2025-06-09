FROM mcr.microsoft.com/playwright:v1.52.0-noble

COPY package.json package-lock.json* ./
RUN npm ci || npm install

COPY . .
COPY test/ test/

EXPOSE 8080

CMD ["npx", "playwright", "test", "--ui-port=8080", "--ui-host=0.0.0.0"]
