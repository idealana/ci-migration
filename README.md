CI Migration
========

Create, migrate, and rollback your migration file.

Step 1: Download ci-migration and unzip or extract

Step 2: Copy ci-migration folder to [ application/third_party ]

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

## How to use

Create migration:
```php index.php migration make your_migration_name```

Migrate:
```php index.php migration migrate```

Rollback:
```php index.php migration rollback```
