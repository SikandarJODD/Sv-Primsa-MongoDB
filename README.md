# Svelte + Prisma + MongoDB 
## Creating a project
```bash
   npm create svelte@latest project-name
   cd project-name
   npm i
   npm run dev -- --open

```
Project will open on Port <code>localhost:5173</code>

## Install Prisma + Prisma Client 
```bash
   npm install prisma --save-dev
   npx prisma
   npx prisma init

```

This will Install <strong>Prisma</strong>  <br/>  Also add ```Prisma``` Folder and create ```.env``` File

### Now Add MongoDB Atlas Url into .env file

```bash
Example : 

mongodb+srv://<username>:<password>@bob.qousp1y.mongodb.net/test

```
```bash
Add Your Username & Password 
Add your Database Name 
/test indicates Database Name
```

## Install Prisma Client 
```bash
   npm install @prisma/client
```
## Add Your Model into schema.prisma 
```bash
    model Article {
        id      String   @id @default(auto()) @map("_id") @db.ObjectId
        title   String
        desc    String
    }
```
```bash
    npx prisma generate

```
- Add Queries into ```+page.server.js``` file in <u>route</u> Folder
- Now copy the ```+page.server.js``` file 
