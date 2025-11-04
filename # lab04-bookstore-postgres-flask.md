# lab04-bookstore-postgres-flask.md
Lab 04 — Bookstore system using PostgreSQL, Flask, Docker, and Python console client.

## Structure
- docker-compose.yml (Postgres + pgAdmin + Flask)
- database/ (SQL init scripts)
- backend/ (Flask app + Dockerfile)
- console_app/ (console client)
- README.md (this file)

## Run with Docker (full stack)
1. Start containers:
   docker-compose up -d --build
2. Wait until Postgres initializes and runs SQL scripts from ./database
3. Open pgAdmin at http://localhost:5050 (admin@admin.com / admin)
4. Open the web app at http://localhost:5000

## Run Flask app locally (alternative)
cd backend
pip install -r requirements.txt
export DATABASE_URL=postgresql://postgres:password@localhost:5432/bookstore
flask run --host=0.0.0.0

## Console app
cd console_app
pip install -r requirements.txt
python console_app.py

## Prepare GitHub repository (one-time)
# Initialize local git (if not already)
git init
git add .
git commit -m "Initial commit — Lab04 Bookstore (Postgres + Flask)"

# Add remote and push to your GitHub (replace <your-username> if different)
git remote add origin https://github.com/VladDV/lab04-bookstore-postgres-flask.git
git branch -M main
git push -u origin main
PS C:\Users\VLAD> git add .
fatal: Unable to create 'C:/Users/VLAD/.git/index.lock': File exists.

Another git process seems to be running in this repository, e.g.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.
PS C:\Users\VLAD> git commit -m "Initial commit  Lab04 Bookstore (Postgres + Flask)"

fatal: Unable to create 'C:/Users/VLAD/.git/index.lock': File exists.
an editor opened by 'git commit'. Please make sure all processes
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.
PS C:\Users\VLAD> git branch -M main
PS C:\Users\VLAD> git remote add origin https://github.com/VladDV/lab04-bookstore-postgres-flask.git
PS C:\Users\VLAD> git push -u origin main
error: src refspec main does not match any