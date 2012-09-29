get_posts() grouped and ordered by Category
=======================

This class returns you an object that you can foreach() loop through, passing regular WordPress get_posts() args, and the results will be grouped by category or custom taxonomy.
It's designed right now to work with posts in only one category [taxonomy term].


Usage:

```
$args = array(
	'taxonomy' => 'my_taxonomy',
	'post_type' => 'my_type',
	);

$p = sld_groupby_category( $args );

foreach ( $p as $post ) :

	if ( sld_groupby_category_changed( $post ) )
		echo '<h1>' .sld_groupby_category_name( $post ). '</h1>';

	the_title(); // etc

endforeach;

```
