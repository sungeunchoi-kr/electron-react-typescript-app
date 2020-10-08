# Electron React Typescript Hot-Reload Bootstrap

### Development with Hot-Reload 
Run `npm run server` to start the dev server. This serves the React app on port 8080 independent of Electron, and
reloads/recompiles on file changes.

Then, run `npm run dev` to launch the Electron window which loads the React app on port 8080.

### Build
Run `npm run build`. This outputs the artifact to the `./build` directory.
`ELECTRON_IS_DEV=0 electron .` will start the app on `./build`, without hot-reloading.

### Build Executable
Run `npm run pack`.
`electron-builder` is used to build the executable.

The artifacts are output to `./install` and `./dist`.

### Notes
* Typescript version 4 does not work with CRA currently. It is purposefully fixed at version 3.
* `electron.js` which starts the main window process is placed in `./public`. This allows
the file to be copied to `./build` during the build phase. (refer to the Medium article below)

#### Sources:
* https://jsmanifest.com/create-your-first-react-desktop-application-in-electron-with-hot-reload/
* https://medium.com/@kitze/%EF%B8%8F-from-react-to-an-electron-app-ready-for-production-a0468ecb1da3

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
