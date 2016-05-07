# Ecto-Cheatsheet

This is mostly for me, but you can check it out fork it, add more snippets and such


**disclaimer: this is mostly to remember things when I'm working with phoenix so it's more phoenix/ecto oriented** 

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
MyApp.Repo.detele(record)
```

* *Find by*

```elixir
record = MyApp.Repo.get_by MyApp.Record, data "foundme"
```

* *Updating*
```elixir
record = %{ record | data: "updated!" }
{ :ok, updated_record } = MyApp.Repo.update record
```

** Notes **

- *preload associations before using them*




  

