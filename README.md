# JavascriptNoteBook-Greski

FETCH

function requestMenu() {
  let data = new FormData();
  data.append("key1", "value1"); // repeat for as many params as necessary
  data.append("key2", "value2");

fetch(API_URL, {method: "POST", body: data})
    .then(statusCheck)
    .then(resp => resp.json()) // or res.text() based on response
    .then(handleResponse)
    .catch(handleError);
}

id(“input-form”).addEventListener(“submit”, function(e)){
	e.preventDefault();
	submitRequest();

});


EXPRESS JS APP

"use strict";

const express = require("express");
const app = express();

const multer = require(“multer”);

app.use(multer().none());

app.get("/hello", function (req, res) {
  res.type("text");
  res.send("Hello World!");
});

console.log("Hello CodeSandbox");
const PORT = process.env.PORT || 8000;
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});


.gitignore 

# Logs

logs

*.log

npm-debug.log*

yarn-debug.log*

yarn-error.log*

lerna-debug.log*

.pnpm-debug.log*


# Diagnostic reports (https://nodejs.org/api/report.html)

report.[0-9]*.[0-9]*.[0-9]*.[0-9]*.json


# Runtime data

pids

*.pid

*.seed

*.pid.lock


# Directory for instrumented libs generated by jscoverage/JSCover

lib-cov


# Coverage directory used by tools like istanbul

coverage

*.lcov


# nyc test coverage

.nyc_output


# Grunt intermediate storage (https://gruntjs.com/creating-plugins#storing-task-files)

.grunt


# Bower dependency directory (https://bower.io/)

bower_components


# node-waf configuration

.lock-wscript


# Compiled binary addons (https://nodejs.org/api/addons.html)

build/Release


# Dependency directories

node_modules/

jspm_packages/


# Snowpack dependency directory (https://snowpack.dev/)

web_modules/


# TypeScript cache

*.tsbuildinfo


# Optional npm cache directory

.npm


# Optional eslint cache

.eslintcache


# Optional stylelint cache

.stylelintcache


# Microbundle cache

.rpt2_cache/

.rts2_cache_cjs/

.rts2_cache_es/

.rts2_cache_umd/


# Optional REPL history

.node_repl_history


# Output of 'npm pack'

*.tgz


# Yarn Integrity file

.yarn-integrity


# dotenv environment variable files

.env

.env.development.local

.env.test.local

.env.production.local

.env.local


# parcel-bundler cache (https://parceljs.org/)

.cache

.parcel-cache


# Next.js build output

.next

out


# Nuxt.js build / generate output

.nuxt

dist


# Gatsby files

.cache/

# Comment in the public line in if your project uses Gatsby and not Next.js

# https://nextjs.org/blog/next-9-1#public-directory-support

# public


# vuepress build output

.vuepress/dist


# vuepress v2.x temp and cache directory

.temp

.cache


# Docusaurus cache and generated files

.docusaurus


# Serverless directories

.serverless/


# FuseBox cache

.fusebox/


# DynamoDB Local files

.dynamodb/


# TernJS port file

.tern-port


# Stores VSCode versions used for testing VSCode extensions

.vscode-test


# yarn v2

.yarn/cache

.yarn/unplugged

.yarn/build-state.yml

.yarn/install-state.gz

.pnp.*

CONNECTING TO DB

‘use strict’
const sqlite3 = require(‘sqlite’);
const sqlite = require(‘sqlite’);

async function getDBConnection(){
	const db = await sqlite.open({
	filename: <db-file-name>, //replace this with your db file name
	driver: sqlite3.Database

    });

return db;
}



















