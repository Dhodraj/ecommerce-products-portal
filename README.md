# ecommerce-products-portal

A products portal with two roles. An admin creates users and assigns products to them. Each user logs in and manages only the products assigned to them.

Built in 2021 and 2022.

https://user-images.githubusercontent.com/83802185/131220158-1c0aa1c4-3e71-4d1f-8385-2c1e059d35c4.mp4

## How it works

React on the front, an Express API at the back, MySQL for storage. Passwords are hashed with bcrypt, and sign-in returns a JSON Web Token. The token secret is read from `ACCESS_TOKEN_SECRET` in the environment.

The API connects to MySQL on localhost as `root` with a database named `crud`.

## Run it

```bash
cd backend
npm install
echo "ACCESS_TOKEN_SECRET=pick-any-long-random-string" > .env
node backend.js        # API on port 4000

cd ../my-app
npm install
npm start
```

This is early work. The two back-end files start on different ports and the front end calls port 4000.
