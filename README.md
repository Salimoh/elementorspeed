# elementorspeed

Removing eicons from elementor sites

add this code to function.php

 //eicon remove
// Deactivate Eicons at Elementor

add_action( 'wp_enqueue_scripts', 'remove_default_stylesheet', 20 );
function remove_default_stylesheet() {
  
  // Don't remove it in the backend
  if ( is_admin() || current_user_can( 'manage_options' ) ) {
        return;
  }
	wp_deregister_style( 'elementor-icons' );
}





# another trick is to unload elementor icons css file with asset clean up
