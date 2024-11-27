#
# The MySQL database server configuration file.
#
# You can copy this to one of:
# - "/etc/mysql/my.cnf" to set global options,
# - "~/.my.cnf" to set user-specific options.
# 
# One can use all long options that the program supports.
# Run program with --help to get a list of available options and with
# --print-defaults to see which it would actually understand and use.
#
# For explanations see
# http://dev.mysql.com/doc/mysql/en/server-system-variables.html

#
# * IMPORTANT: Additional settings that can override those from this file!
#   The files must end with '.cnf', otherwise they'll be ignored.
#
[mysqld]

sql_mode=ALLOW_INVALID_DATES,NO_ENGINE_SUBSTITUTION
innodb_buffer_pool_size=10G
innodb_buffer_pool_instances=12
thread_cache_size=50
key_buffer_size=32M
innodb_log_buffer_size=8M
tmp_table_size=256M
max_heap_table_size=256M
table_definition_cache=2400
table_open_cache=2000
open_files_limit=65535
# adding bind address
bind-address = *
!includedir /etc/mysql/conf.d/
!includedir /etc/mysql/mysql.conf.d/

