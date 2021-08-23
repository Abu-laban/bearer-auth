# bearer-auth

## LAB - 07

### Deployment Test

**Author: Tariq Abu-Laban**

- [tests report](https://github.com/Abu-laban/bearer-auth/actions).
- [back-end](https://tariq-bearer-auth.herokuapp.com/).
- [pull request](https://github.com/Abu-laban/bearer-auth/pull/1).

**Setup**

`.env` **requirements**

- `PORT` - Port Number

- `DATABASE_URL` = Postgres DB

- `SECRET` = JWT SECRET

**Running the app**

- `npm start`

- Endpoint: `/signup`

> `{"username": "tariq","password": "test321"}`

- Returns Object

      {
        "user": {
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQzNDg5fQ.BeAJ1FWTzi3Ex-NyLgw5aCN1CwfC1cINe0Wcrks7jzQ",
            "id": 1,
            "username": "tariq",
            "password": "$2b$10$Y/8nijBOvSgZEaFwN3uKkuN4OcaLw6Sa6/bgD0SLwABguRnpkXBfi",
            "updatedAt": "2021-08-23T18:31:28.122Z",
            "createdAt": "2021-08-23T18:31:28.122Z"
         },
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQzNDg5fQ.BeAJ1FWTzi3Ex-NyLgw5aCN1CwfC1cINe0Wcrks7jzQ"
      }

- Endpoint: `/signin`

> - Username `tariq`
> - Password `test321`

- Returns Object

      {
        "user": {
            "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQyMjI0fQ.D9UrhPQz9PBb5hLcm-LBkcWQoqb0ckA2gvn7Cc7UJ48",
            "id": 1,
            "username": "tariq",
            "password": "$2b$10$IH6VWIhex9M7bOW1K9F2BeJpjLiCLWkO3WXHPpJgzBrXz5PyHBLK.",
            "createdAt": "2021-08-23T17:50:37.760Z",
            "updatedAt": "2021-08-23T17:50:37.760Z"
         },
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQyMjI0fQ.D9UrhPQz9PBb5hLcm-LBkcWQoqb0ckA2gvn7Cc7UJ48"
      }

- Endpoint: `/users`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQyMjI0fQ.D9UrhPQz9PBb5hLcm-LBkcWQoqb0ckA2gvn7Cc7UJ48`

- Returns Object

  [
  "tariq"
  ]

- Endpoint: `/secret`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6InRhcmlxIiwiaWF0IjoxNjI5NzQyMjI0fQ.D9UrhPQz9PBb5hLcm-LBkcWQoqb0ckA2gvn7Cc7UJ48`

- Returns Object

Welcome to the secret area!

**Tests**

- Unit Tests: `npm run test`
- Lint Tests: `npm run lint`
