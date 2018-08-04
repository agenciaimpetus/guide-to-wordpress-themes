# Loop

To list your posts, you can use the code below, where you only have to enter the name of your custom post and 
the number of posts to be listed. Inside the `while` will be the code to be displayed in each item

``` php
<?php
    $loop = new WP_Query( array(
        'post_type' => 'post-type-name',
        'posts_per_page' => 6   // number of posts
        )
    );
?>

<?php while ( $loop->have_posts() ) : $loop->the_post(); ?>
    <?php echo get_the_title(); ?>
    <?php echo get_the_excerpt(); ?>
    <?php if ( has_post_thumbnail() ) : ?>
        <?php the_post_thumbnail('full'); ?>
    <?php endif; ?>
    
<?php endwhile; wp_reset_query(); ?>
```
### More informations

https://codex.wordpress.org/Class_Reference/WP_Query
