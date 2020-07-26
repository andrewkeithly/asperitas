# Postr

![travis](https://travis-ci.com/andrewkeithly/postr.svg?branch=master)
![license](https://img.shields.io/badge/license-MIT-blue.svg)

> Postr is a full stack reddit-style site that uses Node.js, React, and NoSQL databases originally forked from [Deniz Basegmez's Asperitas](https://github.com/d11z/asperitas).

## To Do

- [x] Fork, Update Deps, & Squash bugs
- [ ] Re-setup to my preferred _best practices_
- [ ] Setup Deployment
  - [ ] Deploy Server to Cloud (Which one though? 🤔)
  - [ ] Deploy client to GitHub sub-directory page

### Prerequisites

- node
- yarn (and/or npm)
- mongodb
  - Mac easy mode with [homebrew](https://brew.sh/):<a name="homebrew" id="homebrew" />
  ```bash
  $ brew tap mongodb/brew
  $ brew install mongodb-community
  ```
  - Otherwise checkout instructions [here.](https://docs.mongodb.com/manual/administration/install-community/)

## Quick start

1. Clone this repository

2. Install server dependencies
   ```bash
   $ cd server
   $ yarn
   ```
3. Install client dependencies
   ```bash
   $ cd client
   $ yarn
   ```

## Run the app

1. Start mongodb locally
   - If on mac with [homebrew](#homebrew)
   ```bash
   $ brew services start mongodb-community
   ```
   - Otherwise (Windows installations may already be running a mongo db service [read more here](https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#if-you-installed-mongodb-as-a-windows-service).)
   ```bash
   $ mongod --dbpath="path/to/data/db"
   ```
2. Start the server
   ```bash
   $ cd server
   $ yarn start
   ```
3. Start the client
   ```bash
   $ cd client
   $ yarn start
   ```
4. Browse to `http://localhost:3000/`

## Testing

### Server

Make sure mongodb is running before testing the server.

```bash
$ cd server
$ yarn test
```

### Client

```bash
$ cd client
$ yarn test
```

## File Structure

```
postr

├── .vscode
│	└── launch.json
├── .editorconfig
├── .gitattributes
├── .gitignore
├── .travis.yml
├── LICENSE.md
├── now.json
├── README.md
├── client
│	├── public
│	├── package.json
│	├── yarn.lock
│	├── src
│	│	├── actions
│	│	├── components
│	│	├── config
│	│	├── middleware
│	│	├── reducers
│	│	├── tests
│	│	└── util
│	├── categories.js
│	├── globalStyle.js
│	├── index.js
│	├── serviceWorker.js
│	├── setupTests.js
│	├── store.js
│	├── style.css
│	└── theme.js
└── server
	├── auth
	├── controllers
	├── models
	├── src
	├── test
	├── app.js
	├── config.js
	├── index.js
	├── package.json
	├── routes.js
	└── yarn.lock
```

## Reporting Issues:

- [Github Issues Page](https://github.com/andrewkeithly/postr/issues)

## License

This project is made available under the [**MIT License**](https://github.com/andrewkeithly/postr/blob/master/LICENSE.md).
