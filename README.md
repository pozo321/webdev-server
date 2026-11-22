# webdev-server

Node.js Express server for CS4550 Kambaz. It serves the Lab 5 routes and the Kambaz REST API (users, courses, modules, assignments, enrollments). Data is kept in memory and resets when the server restarts.

## Run locally

```
npm install
npm start
```

The server listens on http://localhost:4000. Create a `.env` file in this folder with:

```
SERVER_ENV=development
CLIENT_URL=http://localhost:3000
SERVER_URL=http://localhost:4000
SESSION_SECRET=super secret session phrase
```

`npm run dev` restarts the server on file changes.

## Deploy on Render

Set these environment variables on the Render Web Service (build command `npm install`, start command `npm start`):

```
SERVER_ENV=production
CLIENT_URL=https://<your-vercel-a5-branch-host>
SERVER_URL=<your-render-host>.onrender.com
SESSION_SECRET=<any long random phrase>
```

`CLIENT_URL` is the exact origin of the client, with no trailing slash. `SERVER_URL` is only the host name, with no `https://`, because it becomes the session cookie domain.
