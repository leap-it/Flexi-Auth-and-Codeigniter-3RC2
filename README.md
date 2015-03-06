# Codeigniter-3-RC2-with-Flexiauth
Codeigniter 3-RC2 with flexiauth 


Update the 'base_url' to CodeIgniters root installation directory.

$config['base_url'] = 'http://localhost/your_codeigniter_directory/';

Update the 'index_page' config setting to ''. This will remove 'index.php' from the sites urls.

Note that this is optional, and if done, a '.htaccess' files needs to be included in the root directory of the installation.
A sample '.htaccess' file is included in the demo.

$config['index_page'] = '';

Update the 'encryption_key' config setting to a value of your choice.
This is optional, but will improve security with your CodeIgniter installation.
$config['encryption_key'] = 'YOUR_ENCRYPTION_KEY';

get your key here 
http://jeffreybarke.net/tools/codeigniter-encryption-key-generator/

Update the 'global_xss_filtering' config setting to TRUE.
This is optional, but will improve security with your CodeIgniter installation.
$config['global_xss_filtering'] = TRUE;

This step must be completed to all flexi auth installations.
Update the 'sess_use_database' config setting to TRUE. This instructs CodeIgniter to save session data to the database rather than as a browser cookie.
This is required as the auth session data is too big to store in a cookie.
$config['sess_driver'] = 'database';

$config['sess_save_path'] = 'ci_sessions';

$config['sess_expiration'] = 7200;

$config['sess_match_ip'] = FALSE;

$config['sess_time_to_update'] = 300;


This step must be completed if a database has not been configured with your CodeIgniter installation.
Update the database configuration settings located in the 'config/database.php' file to connect to your database.

This step is only required if you are installing the flexi auth demo.
Update the 'default_controller' to the sites home page.
$route['default_controller'] = 'auth_lite/index';

don't forget to change the RewriteBase /your flexiauth folder/ in .htaccess (found in flexiauth folder)
