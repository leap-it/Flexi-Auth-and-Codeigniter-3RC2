# Codeigniter-3-RC2-with-Flexiauth
Codeigniter 3-RC2 with flexiauth 

New version for CI 3.03 can be download here http://www.leap-it.be/flexiauth

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

session config 

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

also in the demo controllers update theses two lines so suite your needs

		$this->load->vars('base_url', 'http://www.leap-it.be/test/');
		
		$this->load->vars('includes_dir', 'http://www.leap-it.be/test/includes/');

don't forget to change the RewriteBase /your flexiauth folder/ in .htaccess (found in flexiauth folder)
