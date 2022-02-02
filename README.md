# laravel-tips
Tips and Tricks


## Convert Date time to human readable format

```php
$result = Post::find($id);
$post ->created_at->diffForHumans();
```
