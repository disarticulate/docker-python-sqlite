# docker-python-sqlite
docker files built for Python and sqlite

Base image is build with loadable sqlite extensions

Want to run python with sqlite3 inside your own shell?
Here you go:
```
docker run -it prolocutor/docker-python-sqlite:3.12
```
or if you want to, the following flag builds ([https://www.sqlite.org/compile.html](https://www.sqlite.org/compile.html)) are available:


roots 3.12:

[-SQLITE_DEBUG](https://github.com/disarticulate/docker-python-sqlite/tree/master/sqlite3.12/debug)

[-Os](https://github.com/disarticulate/docker-python-sqlite/tree/master/sqlite3.12/Os)

[-O2](https://github.com/disarticulate/docker-python-sqlite/tree/master/sqlite3.12/O2)


Builds are made conservatively, so all flags or identically branched combinations will build the same image in Docker with identical hashed functions. Completed Build out folder trees are for the sake of human curiousity.

The following flags are subdirs from the roots:
```
json1 = SQLITE_ENABLE_JSON1 
fts5 = SQLITE_ENABLE_FTS5
rtree = SQLITE_ENABLE_RTREE
column-metadata = SQLITE_ENABLE_COLUMN_METADATA
```
PULL REQUEST the masterbuilder.ipynb to add any flag you need (within reason). 

If you want to build an image, find a link in the root (ex, [sqlite3.2](https://github.com/disarticulate/docker-python-sqlite/tree/master/sqlite3.12) and:
```
docker build https://raw.githubusercontent.com/disarticulate/docker-python-sqlite/master/sqlite3.12/O2/Dockerfile
```
