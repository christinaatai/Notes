# Rails Console

### How to spin it up

```
$ rails c
```

### How to edit active record data
1. Find the record
2. Edit the record
```
> m = Meme.where(:title => 'Balloon frihgtens cat').first
> m.title = 'Balloon frightens cat'
> m.save
```
This was found on [Stackoverflow](https://stackoverflow.com/questions/30364252/edit-a-database-record-through-the-rails-console).


