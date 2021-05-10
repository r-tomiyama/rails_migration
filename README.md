# マイグレーションを理解する

## Model&マイグレーションファイルの生成

```
-> % rails g model Message content:string

-> % mysql -u root

mysql> use rails_migration_development;
Database changed

mysql> show tables;
Empty set (0.00 sec)
```

## マイグレーションの実行

```
-> % rails db:migrate

mysql> use rails_migration_development;
Database changed

mysql> show tables;
+---------------------------------------+
| Tables_in_rails_migration_development |
+---------------------------------------+
| ar_internal_metadata                  |
| messages                              |
| schema_migrations                     |
+---------------------------------------+
```
