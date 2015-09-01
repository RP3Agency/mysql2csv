#mysql2csv - Dump all tables in a database to csv

We do a lot of converting from one data format to another.  To automate a 
conversion task recently I needed to deliver data to a client in a CSV format, so I put this 
quick utility together.  It has some pretty severe limits ATM but is still useful.

As it uses `SELECT ... INTO OUTFILE` it requires you to have a writeable location on the server
disk.  Adding streaming output, or local writing, would be the first obvious improvement.

```
	$ mysql2csv 
	mysql2csv -h [host] -u [user] -p [password] -d [database]

	Options:
	  -h, --host                                                          [required]
	  -u, --user                                                          [required]
	  -d, --database                                                      [required]

```