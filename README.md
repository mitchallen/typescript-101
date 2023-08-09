typescript-101
==
Example TypeScript project
--

## Reference

* [Getting Started with TypeScript (Hello World, Mac)](https://scriptable.com/getting-started-with-typescript-hello-world/)

## Usage

```shell
npm start
```

* * *

## Cheat Sheet

* Init project

```sh
npm init -y
```

* Install ts locally

```sh
npm install typescript --save-dev
```

* Make source folder

```sh
mkdir src
```

* Add script

Add this script to package.json:

```json
"tsc": "tsc",
```

* Initialize tsc (gen tsconfig.json)


```sh
npm run tsc -- --init
```

* Edit tsconfig.json (uncomment and update values and save):

```json
  "compilerOptions": {
    "target": "ES6",
    "module": "CommonJS",
    "rootDir": "./src",
    "outDir": "./dist", 
  },
  "include": ["src/**/*.ts"],
  "exclude": ["node_modules"]
```

* create a file

```sh
touch src/app.ts
```

* update main in package.json

```json
"main": "./dist/app.js",
```

* add build script command

```json
"build": "tsc",
```

* run build

```sh
npm run build

ls -ls dist

cat dist/app.js 
```

* add a start script command and save the file

```json
"start": "node dist/app.js",
```

* run the start script

```sh
npm start
```

* add a prestart script command to build first

```json
"scripts": {
  "prestart": "npm run build",
```

* add a clean command:

```sh
"clean": "rm -rf dist",
```

* run the clean command

```sh
npm run clean
```

* Copy the .gitignore file from here:

* https://github.com/microsoft/TypeScript-Node-Starter/blob/master/.gitignore

