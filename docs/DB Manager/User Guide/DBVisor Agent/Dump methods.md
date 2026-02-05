# Dump methods

There are several different dump methods available:


1. **AWS S3:** Downloads the backup from a provided S3 bucket.
2. **Manual:** This method requires the administrator to create backups. In this case, you need to specify the path to the newly created backup. Follow link to get more information <https://outline.bridge.digital./Dump%20methods/Manual%20%252F%20Custom.md> 
3. **SFTP:** Allows the download of a backup from a remote server using SFTP.
4. **Mysqldump:** Utilizes the default mysqldump command to create a backup of a MySQL database. Follow [link](https://outline.bridge.digital./Dump%20methods/Mysqldump.md) to get more information.
5. **pgdump:** Uses the default pgdump command to create a backup of a PostgreSQL database. Follow [link](https://outline.bridge.digital./Dump%20methods/Postgres%20pg_dump.md) to get more information
6. **SSH Dump:** Creates a dump over an SSH tunnel. It utilizes mysqldump and pgdump on another server.

Additionally, you have the flexibility to create your custom dump method as a Symfony Bundle. Please reach out to us for more information.

Feel free to contact us if you have any questions or need further assistance.