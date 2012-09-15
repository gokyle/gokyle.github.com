---
layout: post
title: "Interacting with a Database in Go"
date: 2012-09-01 02:39
comments: true
categories: [development, go, golang, databases]
---

One of my recent projects involved exporting records from a 
[SQLite](http://www.sqlite.org) database to a 
[PostgreSQL](http://www.postgresql.org) database. I would have found it
useful to have a guide to working with databases when I started out.

<!-- more -->

There are two libraries I used:

* for sqlite3, I used [Yasuhiro Matsumoto's](http://mattn.kaoriya.net/) 
[go-sqlite3](https://github.com/mattn/go-sqlite3) library.
* for postgres, I used [Blake Mizerany's](http://blakemizerany.com)
[pq](https://github.com/bmizerany/pq) library.

## Connecting to the Database
Once you have assigned the database object in your code, you should
ensure that you run a `defer db.Close()` to make sure the connection
is properly closed.

### Postgres

{% highlight go %}
import (
        "database/sql"
        "fmt"
        _ "github.com/bmizerany/pq"
)

func ConnectFromEnv() (*sql.DB, error) {
        conn_string := fmt.Sprintf(
        "dbname=%s user=%s password=%s host=%s port=%s sslmode=%s",
            os.Getenv("PG_DBNAME"),
            os.Getenv("PG_USER"),
            os.Getenv("PG_PASS"),
            os.Getenv("PG_HOST"),
            os.Getenv("PG_PORT"),
            os.Getenv("PG_SSLMODE"))

        db, err := sql.Open("postgres", conn_string)
        if err != nil {
                log.Printf("[!] dbase couldn't open database connection: %s",
                        err)
                db = nil
        }

        return db, err
}


{% endhighlight %}

### SQLite3

{% highlight go %}
import (
        "database/sql"
        "fmt"
        _ "github.com/mattn/go-sqlite3"
)

func ... (filename string) ... {
        db, err := sql.Open("sqlite3", filename)
}
{% endhighlight %}

## The database/sql.DB Interface
The database object returned from these connections implements the
interface specified in the
[database/sql interface](http://golang.org/pkg/database/sql/). Specifically,
there are three main methods used to carry out SQL queries: `Exec`,
`Query`, and `QueryRow`.

### Exec

### Query

### QueryRow
