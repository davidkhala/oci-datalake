- port 8888

# Limit
- File direct upload up to size 200 KB
- Documents page can only view hdfs, object storage is not supported

# Troubleshoot
`ERROR : FAILED: Execution Error, return code 1 from org.apache.hadoop.hive.ql.exec.DDLTask. MetaException(message:java.security.AccessControlException: Permission denied: user=admin, access=WRITE, inode="/warehouse/tablespace/managed/hive":hive:hadoop:drwxrwxr-x`
- This is permission issue. Use user `hue` and grant it as super user
- Solution: Menu, user icon -> Administer Users -> Click user `hue`, reset its password on init. -> select tab `Advanced` -> check Superuser status -> Confirm by bottom button "Update user"

