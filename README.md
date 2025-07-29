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
