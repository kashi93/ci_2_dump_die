# CodeIgniter 2
Open Source PHP Framework (originally from EllisLab)

For more info, please refer to the user-guide at http://www.codeigniter.com/userguide2/  
(also available within the download package for offline use)

**WARNING:** *CodeIgniter 2.x is no longer under development and only receives security patches until October 31st, 2015.
Please update your installation to the latest CodeIgniter 3.x version available
(upgrade instructions [here](http://www.codeigniter.com/userguide3/installation/upgrade_300.html)).*


# Dump Die Installation

If project don't have composer.json and composer.lock run below command
```
composer init
```

Open composer.json and paste below code 

```
"require": {
    "symfony/var-dumper":"5.4"
}
```

Run below command to install

```
composer install
```

Load composer autoload inside index.php

```
<?php

include_once './vendor/autoload.php';

...,

```

Try it

```
<?php if (!defined('BASEPATH')) exit('No direct script access allowed');

class Welcome extends CI_Controller
{
	public function index()
	{
		dd($this);
		$this->load->view('welcome_message');
	}
}

```