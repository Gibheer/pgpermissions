pgpermissions
=============

This is a small script which tries to connect on all available databases to
collect permissions for each user.

At the moment, the following permissions are read

* database
  * create
  * connect
  * temporary

* groups
  * is a member of a group

* tables
  * select
  * insert
  * update
  * delete
  * truncate
  * trigger

* views
  * select

example
-------

This is a bit of example output

```
$ ./bin/pgpermissions | grep user1
 user1        bar                 database         temporary, connect
 user1        foo                 database         temporary, connect
 user1        foogroup            group            member
 user1        postgres            database         connect, temporary
 user1        redmine             database         connect, temporary
 user1        public.foo          table            select
```
