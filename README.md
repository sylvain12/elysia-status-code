# Elysia Status Code

## Installation
```bash
bun add --exact elysia-http-status-code
```

## Usage
To start the development server run:
```bash
import Elysia from 'elysia'
import { HttpStatusCode } from 'elysia-http-status-code';

new Elysia()
  .use(HttpStatusCode())
  .get('/'. ({set, httpStatus}) => {
    set.status = httpStatus.HTTP_200_OK;
    return `Hello With response ${httpStatus.HTTP_200_OK}`;
  })
  .post('/user', ({set, body, httpStatus}) => {
    set.status = httpStatus.HTTP_200_OK;
    return {"user": body.name}
  })
  .listen(3000);
```
