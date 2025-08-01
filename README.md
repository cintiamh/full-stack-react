# Modern Fullstack React

## VS Code

Extensions:

- Docker (by Microsoft)
- ESLint (by Microsoft)
- Prettier - Code formatter (by Prettier)
- MongoDB for VS Code (by MongoDB)

## Setting up project with Vite

```
$ npm create vite@latest .
```

Start dev:

```
$ npm run dev
```

Dependencies

```
$ npm install --save-dev prettier@latest eslint@latest eslint-plugin-react@latest eslint-config-prettier@latest eslint-plugin-jsx-a11y@latest
```

Run Eslint

```
$ npx eslint src
```

Automatically fix with Eslint

```
$ npx eslint src --fix
```

Adding lint script

```
$ npm pkg set scripts.lint="eslint src"
$ npm run lint
```

Visualize inner workings of the Call Stack http://latentflip.com/loupe/

## Docker

Creating a container

```
$ run -i -t ubuntu /bin/bash
```

Check running OS:

```
$ uname -a
```

End

```
$ exit
```

Check running containers

```
$ docker ps
```

Create a mongo

```
$ docker run -d --name dbserver -p 27017:27017 --restart unless-stopped mongo
```

Connecting using mongosh

```
$ mongosh mongodb://localhost:27017/ch2
```

Using the database

```
ch2> db.users.insertOne({username: 'dan', fullName: 'Daniel Bugl', age: 26})
{
  acknowledged: true,
  insertedId: ObjectId('6888e70c87a5b5bdc94302d4')
}
ch2> db.users.find()
[
  {
    _id: ObjectId('6888e70c87a5b5bdc94302d4'),
    username: 'dan',
    fullName: 'Daniel Bugl',
    age: 26
  }
]
```

## Testing

```
$ npm install --save-dev jest mongodb-memory-server
```

VS Code
Install `Orta.vscode-jest` extension

## APIs

- GET: 200 OK
- POST: 201 Created
- PUT: 200 OK, 204 No Content, 201 Created
- PATCH: 200 OK, 204 No Content
- DELETE: 200 OK, 204 No Content

Routes: `/api/v1/`

Framework:

- Express: mature
- Koa: smaller, more expressive, and more robust, same express team
- Fastify: efficiency and low overhead.

```
$ npm install express
```

## Environment variables

```
$ npm install dotenv
```

Test in browser

```
fetch('http://localhost:3001/api/v1/posts', {headers:{'Content-Type': 'application/json'}, method: 'POST', body: JSON.stringify({title: 'Test Post'})}).then(res =>res.json()).then(console.log)

fetch('http://localhost:3001/api/v1/posts/688d0803a35d223d01812e0c', {headers:{'Content-Type': 'application/json'}, method: 'PATCH', body: JSON.stringify({title: 'Test Post Changed'})}).then(res =>res.json()).then(console.log)

fetch('http://localhost:3001/api/v1/posts/688d0803a35d223d01812e0c', {method: 'DELETE'}).then(res =>res.status).then(console.log)
```
