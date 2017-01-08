## Migrations

```ruby
# 001_create_articles.rb
Sequel.migration do
  up do
    create_table(:articles) do
      primary_key :id
      String :title, null: false
      String :text, null: false
    end
  end

  down do
    drop_table(:articles)
  end
end
```

reversible migrationsの場合、"change"メソッドが使える

```ruby
Sequel.migration do
  change do
    create_table(:articles) do
      ...
    end
  end
end
```
