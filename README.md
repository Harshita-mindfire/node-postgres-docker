This is a demo nodejs postgres app build with Docker.

## Steps

1. run docker-compose. Check http://localhost:3000, Hello World should be displayed
2. in a new terminal, run `docker exec <image-name-for-web> npm run migrate` to create table in postgres.
   > eg: run docker exec node-postgres-docker-web-1 npm run migrate
3. Run `docker exec <image-name-for-web> npm run seed` to seed users in db.
4. Run /users to get users.
5. Open postman and send a post request to `/users` with body {"name": "John Smith"} and Content-Type: application/json header to add a new user in db
