Learn SQL
=========

A guide to learning SQL via data about the United States' national parks.

## Setup

If you don't want to install sqlite3 locally, or you have trouble you can run SELECT queries in your browser:

https://sqlime.org/#https://raw.githubusercontent.com/ajmarcus/nationalparks/main/data/nps.sqlite

Just note that the CREATE and INSERT queries covered below will not work in the browser.

If you want to install sqlite3, first check if you have it already:
- Open a terminal
- Type "sqlite3" and press enter
```bash
sqlite3 ./nps.sqlite
```
- If you see a prompt like "sqlite>", then you have sqlite3 installed
```bash
SQLite version 3.43.2 2023-10-10 13:08:14
Enter ".help" for usage hints.
sqlite>
```

If you don't already have it, this is how to install sqlite3:
- Go to https://www.sqlite.org/download.html
- Choose the "Precompiled Binaries For" Mac OS X or Windows section
- Download the sqlite-tools-*.zip file
- Unzip and you should have a sqlite3 executable
- On Mac you will need to right click on the sqlite3 file and choose "Open" to bypass the security warning
- On Windows, I'm not sure what you need to do
- On Mac, you can then move `sqlite3` to `/usr/local/bin` to make it available from the command line
```bash
mv ~/Downloads/sqlite-tools-osx-x64-3450100/sqlite3 /usr/local/bin
```
- Now you should be able to run `sqlite3` from the command line
```bash
sqlite3 ./nps.sqlite
```
```bash
SQLite version 3.43.2 2023-10-10 13:08:14
Enter ".help" for usage hints.
sqlite>
```

Use these settings in your sqlite3 shell locally to get pretty output:
```bash
sqlite> .header on
sqlite> .mode table
```
