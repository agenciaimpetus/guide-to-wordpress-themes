# Widgets

To create widgets, add the following code snippet in your `functions.php` file

``` php
function name_widget() {
	register_sidebar(
		array(
			'name'          => 'widget name',
			'id'            => 'widget-id',
			'before_widget' => '<div class="widget-item">',
			'after_widget'  => '</div>',
			'before_title'  => '<h2 class="widget-title">',
			'after_title'   => '</h2>',
		)
	);
}

add_action( 'widgets_init', 'name_widget' );

```
This code snippet will create a session inside your wordpress admin in "Appearance" >> "widgets"

To view the content of the widget in your theme, use:

``` php
<?php dynamic_sidebar( 'widget-id' ); ?>
```

### Additional information

More information about widgets  
https://codex.wordpress.org/Widgetizing_Themes

See the parameters that `register_sidebar` can receive  
https://developer.wordpress.org/reference/functions/register_sidebar/
