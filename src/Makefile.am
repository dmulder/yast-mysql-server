#
# Makefile.am for .../mysql-server/src
#

yncludedir = ${prefix}/share/YaST2/include/mysql

clientdir = ${prefix}/share/YaST2/clients
client_DATA =                   \
        mysql.py

#TODO: This must be modified to python can know from where can import!
ynclude_DATA =                  \
	defaults.py		\
	dialogs.py		\
	Mysql.py		\
	wizards.py

#mysql.desktop: mysql.desktop.in
#	sed -e 's;[@]CLIENTDIR[@];$(clientdir);g' < $(srcdir)/mysql.desktop.in > $(srcdir)/mysql.desktop

#desktopdir = ${prefix}/share/applications/YaST2
#desktop_DATA =                  \
#        mysql.desktop

moduledir = ${prefix}/share/YaST2/modules

mysql.py: mysql.py.in
	sed -e 's;[@]INCLUDEDIR[@];$(yncludedir);g' < $(srcdir)/mysql.py.in > $(srcdir)/mysql.py

# create a symlink for local build, #145327
mysql:
	ln -sf . $@
ycpchook = mysql

EXTRA_DIST = $(client_DATA) $(ynclude_DATA) $(module_DATA) $(desktop_DATA)
CLEANFILES = mysql.py
