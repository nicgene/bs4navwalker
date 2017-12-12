# bs4navwalker
A custom WordPress nav walker class for Bootstrap 4 (v4.0.0-alpha.6) nav menus in a custom theme using the WordPress built in menu manager

```php
// Register Custom Navigation Walker
require_once('bs4navwalker.php');
```

```php
<nav class="navbar navbar-expand-md navbar-light bg-faded">
   <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#bs4navbar" aria-controls="bs4navbar" aria-expanded="false" aria-label="Toggle navigation">
     <span class="navbar-toggler-icon"></span>
   </button>
   <a class="navbar-brand" href="#">Navbar</a>
   <?php
   wp_nav_menu([
     'menu'            => 'top',
     'theme_location'  => 'top',
     'container'       => 'div',
     'container_id'    => 'bs4navbar',
     'container_class' => 'collapse navbar-collapse',
     'menu_id'         => false,
     'menu_class'      => 'navbar-nav mr-auto',
     'depth'           => 2,
     'fallback_cb'     => 'bs4navwalker::fallback',
     'walker'          => new bs4navwalker()
   ]);
   ?>
 </nav>
```
