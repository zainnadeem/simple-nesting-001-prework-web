# Guide to Solving and Reviewing Simple Nesting

### `#hopper`

```bash
nested hash #hopper operates on the programmer_hash and returns the value of the :grace_hopper key
```

This method should only return :grace_hopper's values. To do so, we need to call the hash and then ask for the `:grace_hopper` key.

```ruby
programmer_hash[:grace_hopper]
```

### `#alan_kay_is_known_for`

Here, we need to return what Alan Kay is know for. Like in our first method we will ask our hash for its values of `:alan_kay` and ask `:alan_kay` for `:know_for`.

```ruby
programmer_hash[:alan_kay][:known_for]
```

### `#dennis_ritchies_language`

This method should return Dennis Ritchies language.

```bash
programmer_hash[:dennis_ritchie][:languages]
```
The test is not passing! If we look closely to our error message, we will see why. 

```bash
expected: "C"
got: ["C"]
```

It expected a string, but got an array. To get the string out of the array we need to add `.first` to the end of our hash query.

```ruby
programmer_hash[:dennis_ritchie][:languages].first
```

### `#adding_matz`

In this method we will not query our hash, we will add a key/value pair to it.

```ruby
programmer_hash[:yukihiro_matsumoto] = {:known_for => "Ruby", :languages => ["LISP, C"]}
```

Our test is not passing. 

**Remember:** The return value of a method is the last line it executed, in our case here is the adding of the key/value pair. So our methods return value is equal to the return value of the adding a key/value to the hash. But we want our method to return the modified hash.

```ruby
programmer_hash[:yukihiro_matsumoto] = {:known_for => "Ruby", :languages => ["LISP, C"]}
programmer_hash
```

### `#changing_alan`

```ruby
alans_new_info = "GUI"
programmer_hash[:alan_kay][:known_for] = alans_new_info
programmer_hash 
```
Again, we need to call the hash at the end of our method, else we would get the return value of our change we did to `[:alan_kay][:known_for]`.

### `#adding_to_dennis`

For this method we need to add a language to `:dennis_ritchie`. But we cannot say `programmer_hash[:dennis_ritchie][:languages] = "Assembly"` because that would set the languages equal to the string `"Assembly"`. Our languages value is an array of languages, we need to `push` the new language into the languages array.

```ruby
programmer_hash[:dennis_ritchie][:languages] << "Assembly"
programmer_hash
```
