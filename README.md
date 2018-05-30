# ansible-oracle-sqlDeveloper

Ensure that Oracle SQL Developer and SQLCL is installed

## Requirements

None

## Role Variables

| Variable Name             | Defaults | Description                                            |
|---------------------------|----------|--------------------------------------------------------|
| install_locally           |False     | If true, expects the necessary files in /tmp folder    |
| sql_developer_url         |""        | Download path for Oracle Sql Developer                 |
| sqlcl_url                 |""        | Download path for Oracle Sql Command Line              |

## Dependencies

None

## Example Playbook

    ---
    - hosts: servers

      vars:
        install_locally: false
        jdk_tarball_file: "http://example.com/sql_developer.rpm"
        java_download_from_oracle: "http://example.com/sqlcl.zip"

      roles:
        - role: dfgd.oracle-sqlDeveloper
    ...

## After Installation

Run this command to start SQL Developer
sh /opt/sqldeveloper/sqldeveloper.sh

After this we need to put the jdk file path


To run SQL Command Line run this:
/opt/sqlcl/bin/sql 

## License

BSD

## Author Information

This role was created by [dfgd](https://github.com/dfgd).

