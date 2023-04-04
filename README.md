# pgSQL

pgSQL tuning python scripts

Using pgtune
pgtune works by taking an existing postgresql.conf file as an input, making changes to it based on the amount of RAM in your server and suggested workload, and output a new file.

Here's a sample usage:

<pre>pgtune -i $PGDATA/postgresql.conf -o $PGDATA/postgresql.conf.pgtune</pre>

pgtune --help will give you additional usage information. These are the current parameters:

-i or --input-config : Specifies the current postgresql.conf file.

-o or --output-config : Specifies the file name for the new postgresql.conf file.

-M or --memory: Use this parameter to specify total system memory. If not specified, pgtune will attempt to detect memory size.

-T or --type : Specifies database type. Valid options are: DW, OLTP, Web, Mixed, Desktop

-P or --platform : Specifies platform, defaults to the platform running the program. Valid options are Windows, Linux, and Darwin (Mac OS X).

-c or --connections: Specifies number of maximum connections expected. If not specified, it depends on database type.

-D or --debug : Enables debugging mode.

-S or --settings: Directory where settings data files are located at. Defaults to the directory where the script is being run from. The RPM package includes a patch to use the correct location these files were installed into.

