# bs4navwalker
A custom WordPress nav walker class for Bootstrap 4 (v4.0.0-alpha.2) nav menus in a custom theme using the WordPress built in menu manager

```php
// Register Custom Navigation Walker
require_once('bs4navwalker.php');
```

```php
 <?php
 // Use the new walker
 wp_nav_menu([
    'menu'            => 'primary',
    'theme_location'  => 'primary',
    'container'       => 'div',
    'container_id'    => 'exCollapsingNavbar2',
    'container_class' => 'collapse navbar-toggleable-sm',
    'menu_id'         => false,
    'menu_class'      => 'nav navbar-nav',
    'depth'           => 2,
    'fallback_cb'     => 'bs4navwalker::fallback',
    'walker'          => new bs4navwalker()
]);
