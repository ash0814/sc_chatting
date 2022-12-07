# sc_chatting


## 🔗Test
[SC통신 바로가기](http://34.64.87.72:8080)


## Manual

### 🤖 Before Start

```shell
node --verison
npm --version
```

node 및 npm 설치 후 진행!
<br>
<br>

### ❗️Clone Repository

```bash
git clone https://github.com/ash0814/sc_chatting.git ;
cd sc_chatting ;
```

### 📩 Install Pakages

```bash
npm install // frontend, backend 디렉토리 각각 실행
```

### 🛠️ Create DB

```bash
mysql –uroot –p

CREATE DATABASE sc_db;
use sc_db;
source db_init.sql
```

### 📚 Add db.js ( backend/server.js와 같은경로 위치에 파일추가 )

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

### 🔥 Start!

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
