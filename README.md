# sc_chatting


## ๐Test
[SCํต์  ๋ฐ๋ก๊ฐ๊ธฐ](http://34.64.87.72:8080)


## Manual

### ๐ค Before Start

```shell
node --verison
npm --version
```

node ๋ฐ npm ์ค์น ํ ์งํ!
<br>
<br>

### โ๏ธClone Repository

```bash
git clone https://github.com/ash0814/sc_chatting.git ;
cd sc_chatting ;
```

### ๐ฉ Install Pakages

```bash
npm install // frontend, backend ๋๋ ํ ๋ฆฌ ๊ฐ๊ฐ ์คํ
```

### ๐ ๏ธ Create DB

```bash
mysql โuroot โp

CREATE DATABASE sc_db;
use sc_db;
source db_init.sql
```

### ๐ Add db.js ( backend/server.js์ ๊ฐ์๊ฒฝ๋ก ์์น์ ํ์ผ์ถ๊ฐ )

```js
const mysql = require("mysql");

const db = mysql.createConnection({
  host: "your DB host",
  port: "your DB port",
  user: "your DB user",
  password: "your DB password",
  database: "sc_db",
  dateStrings: "date",
});

db.connect();

module.exports = db;
```

### ๐ฅ Start!

#### Frontend

```bash
cd sc_chatting/frontend ;
npm run serve ;
```

#### Backend

```bash
cd sc_chatting/backend ;
supervisor server.js ; // node server.js
```
