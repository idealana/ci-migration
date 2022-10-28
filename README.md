CI3 Migration
========

Create, migrate, and rollback your migration file.

Step 1: Download ci-migration and unzip or extract

Step 2: Copy ci-migration-master folder to [ application/third_party ], and rename folder as ci-migration

Step 3: Create Migration.php file in [ application/controllers ]
```php
<?php

defined('BASEPATH') OR exit('No direct script access allowed');

require_once APPPATH."/third_party/ci-migration/Migration_Trait.php";

class Migration extends CI_Controller {
	use Migration_Trait;
}

?>
```

Step 4: Edit migration.php in [ application/config ]
```php
$config['migration_enabled'] = TRUE;
```

## How to use

Open terminal or cmd in your application root folder, and type command below

Create migration:
```
php index.php migration make your_migration_name
```

Migrate:
```
php index.php migration migrate
```

Rollback:
```
php index.php migration rollback
```
