# Ecto-Cheatsheet

This is mostly for me, but you can check it out fork it, add more snippets and such


**disclaimer: This is mostly to remember things when I'm working with phoenix so it's more phoenix/ecto oriented** 

* *Getting all records*

```elixir
AppName.Repo.all AppName.MyModel
```

* *Removing all records*

```elixir
AppName.Repo.delete_all AppName.MyModel
```

* *Insert a new record*

```elixir
record = %MyApp.MyModel{ data: "test" } # data being a field of the model
{:ok, inserted_record} = AppName.Repo.insert(record)
```

* *Delete a single record*

```elixir
MyApp.Repo.delete(record)
```

* *Find by*

```elixir
record = MyApp.Repo.get_by MyApp.Record, data "findme"
```

* *Updating*
```elixir
record = %{ record | data: "updated!" }
{ :ok, updated_record } = MyApp.Repo.update record
```

* *Getting the last/first record*
```elixir
last_record = MyApp.Repo.one(from x in MyApp.Record, limit: 1, order_by: [desc: x.id])
first_record = MyApp.Repo.one(from x in MyApp.Record, limit: 1, order_by: [asc: x.id])

# You might need to use Ecto.Query.from...
# You can change the limit number to get more records
```


**Notes**

- *preload associations before using them*




  

