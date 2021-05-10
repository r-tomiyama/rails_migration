# マイグレーションを理解する

## Model&マイグレーションファイル①の生成

```
-> % rails g model Message content:string

-> % mysql -u root

mysql> use rails_migration_development;
Database changed

mysql> show tables;
Empty set (0.00 sec)
```

## マイグレーションの実行①

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


## Model&マイグレーションファイル②の生成

```
-> % rails g migration AddTextToMessages text:string

-> % rails c

>> Message.new(content:'hoge')
=> #<Message id: nil, content: 'hoge', created_at: nil, updated_at: nil>

>> Message.new(content:'hoge', text:'fuga')
Traceback (most recent call last):
        1: from (irb):3
ActiveModel::UnknownAttributeError (unknown attribute 'text' for Message.)
```
