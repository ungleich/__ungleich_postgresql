cdist-type__ungleich_postgresql(7)
=======================================
Setup PostgreSQL with backup

ungleich GmbH <cdist--@--ungleich.ch>


DESCRIPTION
-----------
Setup postgresql including some roles for application access

The development of this type was made possible by Panter AG (www.panter.ch).


REQUIRED PARAMETERS
-------------------
user
    Which system user to grant access to the database (creates a role)


OPTIONAL PARAMETERS
-------------------
password
    Setup password for tcp based connections

version
    Define PostgreSQL version to use instead of default


BOOLEAN PARAMETERS
------------------
no-backup
    Do not backup database regulary


EXAMPLES
--------

.. code-block:: sh

    __ungleich_postgresql --user app

    # Setup password for tcp based connections (tcp not enabled by this type though)
    __ungleich_postgresql --user app --password 'hashedpw'

    # Select different version (must be available in the repository)
    __ungleich_postgresql --user app --version 9.2

    # Do not create backups
    __ungleich_postgresql --user app --no-backup


SEE ALSO
--------
- `cdist-type(7) <cdist-type.html>`_


COPYING
-------
Copyright \(C) 2013-2015 ungleich GmbH (www.ungleich.ch). 
Free use of this software is granted under the terms 
of the GNU General Public License version 3 (GPLv3).
