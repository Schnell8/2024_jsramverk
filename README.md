# jsramverk
-----------------------------

## Week 1 & 2: Specification

### Vulnerabilities
The command `npm audit`identified 5 vulnerabilities, 2 moderate and 3 high.

### Solution
As suggested I ran `npm audit fix`. This time after running `npm audit` again it came up with 3 vulnerabilities. From the report I could read that all 3 could be fixed with the suggested command `npm audit fix --force`.
It worked perfectly, 0 vulnerabilities identified.

-----------------------------

### Steps to make the app work
Use the steps below to make the app work

#### 1. API Key from Trafikverket
Go to [Trafikverket](https://data.trafikverket.se/get-started) to register an account. When done obtain your API key.

#### 2. Create .env file
Create a `.env` file in your directory looking like this:

```
TRAFIKVERKET_API_KEY=<your-api-key>
```

#### 3. Install dotenv
Run command in terminal:

```
npm install dotenv
```

#### 4. Set port
Locate file `app.mjs` in directory and change port to this:

```
const port = process.env.PORT || 3000;
```

#### 5. Init database
Run command in terminal:

```
bash ./db/reset_db.bash
```

#### 6. Create first document
Run command in terminal:

```
echo "INSERT INTO documents (title, content) VALUES ('Initial title', 'Initial content')" | sqlite3 db/docs.sqlite
```

#### 7. Run app
Run command in terminal:

```
node app.mjs
```

#### 8. Open browser
Open browser and go to `localhost:3000` to check out the app.

-----------------------------

## Week 3-5: Refactoring

-----------------------------

## Week 5-9: Further development

-----------------------------
