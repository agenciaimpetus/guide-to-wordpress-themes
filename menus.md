# Menus 
To create menus, add the following code snippet in your `functions.php` file.

``` php
function register_menu_name_function() {
  register_nav_menu( 'menu-name', __( 'Menu name', 'Menu description' ) );
}

add_action( 'init', 'register_menu_name_function' );
```

This code snippet will create a session inside your wordpress admin in "Appearance" >> "menus"

To display the menu in your view, use: 

``` php
wp_nav_menu(array(
  'menu'  =>  'menu-name',
  'menu_class' => 'navigation-list'
));

```


### Additional information
More information about menus 
https://developer.wordpress.org/reference/functions/wp_nav_menu/
