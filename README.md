### Setup Intructions (back-end):
## Clone and open this repository

# (1) Initialize a new mySQL instance
Create a local instance of a mySQL schema (this can be accomplished by either using the GUI mySQLWorkbench or in the terminal). 
- For simplicity, create this schema under the root user and name it 'todo_db'.
- This will be running on port 3306 by default.

# (2) Link this back-end repository to the new mySQL instance
Modify DATABASE_PASSWORD in the .env file to match the instance you created. Replace <PASSWORD> with the password that you created for the root user
- DATABASE_PASSWORD='<PASSWORD>'

# (3) Install the dependancies 
Run the following bash command in your terminal (make sure you have cd to the directory where this code is located [/todo-list-app-be]):
```bash
npm install
```

# (4) Update/link the mySQL schema with Prisma
Run the following bash command in your terminal:
```bash
npx prisma migrate dev --name init 
```

# (5) Finish by starting up the backend 
Run the following bash command in your terminal:
```bash
npm run dev
```
- NOTE: your back-end server should now be listening on port 4000.



## (END) Close when done using the application
Enter ^c in the terminal.