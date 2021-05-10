# マイグレーションを理解する

## Modelの生成

```
-> % rails g model Message content:string

-> % mysql -u root

mysql> use rails_migration_development;
Database changed

mysql> show tables;
Empty set (0.00 sec)
```
