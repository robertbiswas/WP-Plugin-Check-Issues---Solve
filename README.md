# WP Plugin Check Issues [Solutions]

## Issue: Usage of a direct database call is discouraged.
Specially when the plugin deals with WordPress custom tables.

 ### Solution
 Add this comment at the end of the line
 ```
 // phpcs:ignore WordPress.DB.DirectDatabaseQuery.DirectQuery
 ```

### Example:
```
$wpdb->insert( $crud_table_name, array( 'name' => $name, 'email' => $email ) ); // phpcs:ignore WordPress.DB.DirectDatabaseQuery.DirectQuery
```

## Issue: Direct database call without caching detected. Consider using wp_cache_get() / wp_cache_set() or wp_cache_delete().
Specially when the plugin deals with WordPress custom tables.
 ### Solution
 Add this comment at the end of the line
 ```
// phpcs:ignore WordPress.DB.DirectDatabaseQuery.NoCaching
 ```

## For Both of the above issues
 ### Solution
 Add this comment at the end of the line
 ```
// phpcs:ignore WordPress.DB.DirectDatabaseQuery
 ```
