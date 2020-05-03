# Runtime image kekedaine/km-node:12-runtime
FROM node:12-alpine

EXPOSE 3000
WORKDIR /app

ONBUILD COPY --from=builder /app .
ONBUILD ADD . /app
ONBUILD RUN npm run build

CMD ["npm", "serve"]