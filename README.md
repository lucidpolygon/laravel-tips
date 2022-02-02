# laravel-tips
Tips and Tricks


### Convert Date time to human readable format

```php
$result = Post::find($id);
$post ->created_at->diffForHumans();
```

### firstOr(function() {});

When searching for the first record and you don't find it, Laravel throws a `ModelNotFoundException`.
Which is translated to a 404 by the exception handler. Instead use `firstOr` to pass a callback.

```php
$result = Post::where('author',$author)->firstOr(function() {
  // perform your action
});
```
